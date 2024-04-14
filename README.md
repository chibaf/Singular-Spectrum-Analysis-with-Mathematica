# Singular-Spectrum-Analysis-with-Mathematica

ref:
Singular Spectrum Analysis for Time Series (SpringerBriefs in Statistics) 
 Nina Golyandina, Anatoly Zhigljavsky, 2020

Singular Spectrum Analysis with Mathematica



Singular Spectrum Analysis

In[34]:= len = 200

Out[34]= 200

In[35]:= a1 = Table[N[2*i/len], {i, len}];

In[36]:= Export["~/ssa_20211008/graph1.csv", a1, "CSV"]

Out[36]= "~/ssa_20211008/graph1.csv"

In[37]:= ListPlot[a1, Joined -> True]

Out[37]= \!\(\*
GraphicsBox[{{}, {{{}, {}, 
 


In[38]:= a2 = Table[0.5*Sin[2 Pi (20*i/len)], {i, len}];

In[39]:= Export["~/ssa_20211008/graph2.csv", a2, "CSV"]

Out[39]= "~/ssa_20211008/graph2.csv"

In[40]:= ListPlot[a2, Joined -> True, PlotRange -> {-1, 1}]

Out[40]= \!\(\*
GraphicsBox[{{}, {{{}, {}, 


In[41]:= c = a1 + a2;

In[42]:= Export["~/ssa_20211008/graph3.csv", c, "CSV"]

Out[42]= "~/ssa_20211008/graph3.csv"

In[43]:= ListPlot[c, Joined -> True]

Out[43]= \!\(\*
GraphicsBox[{{}, {{{}, {}, 


In[44]:= c[[1]]

Out[44]= 0.303893

In[45]:= Length[c]

Out[45]= 200

Out[96]= 200

Out[95]= 0

In[46]:= Dimensions[c]

Out[46]= {200}

Out[97]= {200}

In[47]:= m = Length[c]

Out[47]= 200

In[48]:= n = Floor[m/2]

Out[48]= 100

In[49]:= m - n + 1

Out[49]= 101

In[50]:= % + n

Out[50]= 201

In[51]:= x = N[Table[c[[i + j - 1]], {i, m - n + 1}, {j, n}]];

In[52]:= Dimensions[x]

Out[52]= {101, 100}

In[53]:= ?SingularValueDecomposition

Out[53]= InformationData[


In[54]:= uu = SingularValueDecomposition[x];

In[55]:= Dimensions[uu]

Out[55]= {3}

In[56]:= u = uu[[1]];

In[57]:= w = uu[[2]];

In[58]:= v = uu[[3]];

In[59]:= Dimensions[u]

Out[59]= {101, 101}

In[60]:= Dimensions[w]

Out[60]= {101, 100}

In[61]:= Dimensions[v]

Out[61]= {100, 100}

In[62]:= ListLogPlot[Table[w[[i, i]], {i, n}], Joined -> True, PlotRange -> All, 
 Axes -> False, Frame -> True]

Out[62]= \!\(\*
GraphicsBox[{{}, {{{}, {}, 


In[63]:= sn[xx_] := Module[{i, j, k, n, n1, x, sum}, x = {};
  {n1, n} = Dimensions[xx];
  j = 0; sum = 0;
  Do[Do[If[k <= n, sum = sum + xx[[i - k + 1, k]]; j = j + 1], {k, i}];
   x = Append[x, sum/j]; sum = 0; j = 0, {i, n1}];
  j = 0; sum = 0;
       Do[Do[
    If[k <= n1, sum = sum + xx[[n1 - k + 1, k + i - 1]]; j = j + 1], {k, 
     n - i + 1}];
   x = Append[x, sum/j]; sum = 0; j = 0, {i, 2, n}];
  Return[x]]

0

trend and steady

In[67]:= xx = Sum[w[[i, i]] Outer[Times, Transpose[u][[i]], Transpose[v][[i]]], {i, 
    1}];

In[68]:= y1 = sn[xx];

In[69]:= ListPlot[y1, Joined -> True, PlotRange -> All]

Out[69]= \!\(\*
GraphicsBox[{{}, {{{}, {}, 


In[121]:= xx = Sum[w[[i, i]] Outer[Times, Transpose[u][[i]], Transpose[v][[i]]], {i, 
    3}];

In[122]:= y1 = sn[xx];

In[123]:= ListPlot[y1, Joined -> True]

Out[123]= \!\(\*
GraphicsBox[{{}, {{{}, {}, 


In[124]:= xx = Sum[w[[i, i]] Outer[Times, Transpose[u][[i]], Transpose[v][[i]]], {i, 2, 
    40}];

In[125]:= y1 = sn[xx];

In[126]:= ListPlot[y1, Joined -> True]

Out[126]= \!\(\*
GraphicsBox[{{}, {{{}, {}, 


nl = {{1, 2}, {1, 3}, {1, 4}, {1, 5}, {2, 3}, {2, 4}, {2, 5}, {3, 4}, {3, 5}, {4, 5}}

{{1, 2}, {1, 3}, {1, 4}, {1, 5}, {2, 3}, {2, 4}, {2, 5}, {3, 4}, {3, 5}, {4, 5}}

Length[nl]

10

e = Table[Table[y1[[nl[[i, 1]]]].RotateLeft[y1[[nl[[i, 2]]]], k], {k, 0, Length[y1[[1]]]}]/Length[y1[[1]]], {i, 10}];

mx = Table[Max[e[[i]]], {i, Length[e]}]

{0.0034118, 0.00169974, 0.0040271, 0.00480403, 0.00241246, 0.00589803, 0.0076644, 0.00332483, 0.0041586, 0.00897104}

mn = Table[Min[e[[i]]], {i, Length[e]}]

{-0.00341771, -0.00201093, -0.00489775, -0.00717114, -0.00222704, -0.00447804, -0.00881531, -0.00401223, -0.00477609, -0.0100329}

Table[ListPlot[e[[k]], Joined -> True], {k, 10}]

{,,,,,,,,,}

z = Table[0, {10}]

{0, 0, 0, 0, 0, 0, 0, 0, 0, 0}

Do[Do[If[e[[k, i]] == mx[[k]], z[[k]] = i], {i, Length[e[[1]]]}], {k, 10}]

z

{15, 24, 78, 164, 70, 61, 137, 85, 17, 174}![image](https://user-images.githubusercontent.com/1296728/168692588-3c7ede1b-0c4f-4ed5-b840-691476e907ca.png)
