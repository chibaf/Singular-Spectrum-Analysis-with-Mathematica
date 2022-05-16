# Singular-Spectrum-Analysis-with-Mathematica
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
{RGBColor[0.368417, 0.506779, 0.709798], PointSize[0.009166666666666668], 
       AbsoluteThickness[1.6], LineBox[CompressedData["
1:eJw10jlsHFUcwOEnKpSKwgUFCgtCyCCEgHCD8ctp5/aub3ttz95LRWhDMwWp
09BAgVZKGhpLSEgECaGBgAgoQdzmZs0NCRAOh/vI7n6zUhR9efnPm/d+c1X1
gVLjkhDCqYt/en8PfudHHxpaHVs//PCof4gDP8KXxhObj5wtnnicL7N+nIfi
Y4/2fk/w5f7/Kl8RzxV7//IkF8w/xVfHTWvHDo1sepqv8bxn+Np4XfnoCxvD
z/Kw5z/H18fjF6fXjmV8g/2e5xvjlv7vJN9k/xf55nhyY/jiDi/xLd7nZd4S
S/0NT/Gt3u8Vvi2uH+498FW+3fue5jvig73XO3SG7/T+r/FdcfD363y38+S+
J473N3iD73W+3COxt1v56Jt8n/O+xaOxf5y13NH53x44jfHK3utsfsf6VvfB
6dbY7P/etb7N/axZ3xZ7Txta5bDdfb1nfXu80HvcBocd7u996zti/3pGPrC+
031yujP2X+/Ih9Z3ud+PrO+KZ073fhzG3PfH1sdi/7hDn1gfd/+cjsf+48qf
Wt+tR9f6bufhsEeffH2P8+Xre/Vat77XeTns0y9f3+f8n1nfryen+91Hvn5A
38+tH3A/HA7qna8fdF9fWJ/Qn+OE++N0wvfw5cDZhPvkUPR9cCy636/MF30v
nBXdN4eS7+dr8yX3z2nJ98RZSY9vzE/qwXFSD04n9eBsUo9vzU/pwXFKD06n
9PjO/JQeHKb14Ditx1nz03pwNq0Hhxk9zpmf0YPTGT04m9Hje/OzenCc1YPT
WT1+MD+rB4c5PTjO6fGj+Tk9OJvTg8O8HufNzzsPp/P6cDbvfBwW9MrnF5w3
n1/QL59fcP6fzC/qyXHRfXC6qC9ni+4nny/rnc+X3dfP5sv6c1Z2fxyWfA8c
l9xnPr/k+8jnl9zvL+aXfS8cl903p8u+H86W3X8+v+J7yudX9PjV/IoenK3o
wSHRgwuJHhwTPThJ9Mifn+ixMXAn0YOzRA/uJnpwqOjBhYoeHCt6XLB/RQ9O
K3pwp6IHZxU9uFvRg0NVj9/sX9WDY1UPTqp6cFrVgztVPTir6vG7/at6cKjp
wYWaHhxrenBS04PTmh7cqenxh/1renC3pgeHuh5cqOvBsa4HJ3U9/rR/XQ/u
1PXgrK4Hd+t6cGjowYWGHn/Zv6EHJw09OG3owZ2GHpw19OBuQ4+/7d/UgwtN
PTg29eCkqQenTT2409SDs6Ye/9i/qQeHlh5caOnBsaUHJy09OG3p8a/9W3pw
1tKDuy09OLT14EJbD45tPf6zf1sPTtt6cKetB2dtPbjb1oPD/XqE+D/oL9lk

"]]}}, 
{RGBColor[0.368417, 0.506779, 0.709798], PointSize[0.009166666666666668], 
      AbsoluteThickness[1.6]}, {
{RGBColor[0.368417, 0.506779, 0.709798], PointSize[0.009166666666666668], 
       AbsoluteThickness[1.6]}, {}}, {
{RGBColor[0.368417, 0.506779, 0.709798], PointSize[0.009166666666666668], 
       AbsoluteThickness[1.6]}, {}}}, {{}, {}}},
AspectRatio->0.6180339887498948,
Axes->{True, True},
AxesLabel->{None, None},
AxesOrigin->{0., 0},
DisplayFunction->Identity,
Frame->{{False, False}, {False, False}},
FrameLabel->{{None, None}, {None, None}},
FrameTicks->{{Automatic, Automatic}, {Automatic, Automatic}},
GridLines->{None, None},
GridLinesStyle->Directive[
GrayLevel[0.5, 0.4]],
Method->{"OptimizePlotMarkers" -> True, 
     "CoordinatesToolOptions" -> {"DisplayFunction" -> ({
(Identity[#]& )[
Part[#, 1]], 
(Identity[#]& )[
Part[#, 2]]}& ), "CopiedValueFunction" -> ({
(Identity[#]& )[
Part[#, 1]], 
(Identity[#]& )[
Part[#, 2]]}& )}},
PlotRange->{{0., 200.}, {0, 2.}},
PlotRangeClipping->True,
PlotRangePadding->{{
Scaled[0.02], 
Scaled[0.02]}, {
Scaled[0.02], 
Scaled[0.05]}},
Ticks->{Automatic, Automatic}]\)

In[38]:= a2 = Table[0.5*Sin[2 Pi (20*i/len)], {i, len}];

In[39]:= Export["~/ssa_20211008/graph2.csv", a2, "CSV"]

Out[39]= "~/ssa_20211008/graph2.csv"

In[40]:= ListPlot[a2, Joined -> True, PlotRange -> {-1, 1}]

Out[40]= \!\(\*
GraphicsBox[{{}, {{{}, {}, 
{RGBColor[0.368417, 0.506779, 0.709798], PointSize[0.009166666666666668], 
       AbsoluteThickness[1.6], LineBox[CompressedData["
1:eJxdkklOG1EURZ+iDBhFkZIBAwaVRlGEEIL0CUn8AdM3sY0bXDb2r9bFiBHz
v5TaCX/IDIkFoFpCdkBAmEjvWELWwdf3Xd+6r+KzVvZERC7v/u7fH15/a6Pw
/Ombq+va9B/mtl1/8ezsZsoz4OdG618aUa/Zx88vHnju8ftTDsCvoX8Lv3e4
9x555sEL0C/Cbwn3lpHnA/gj9J/g9xn3viDPV/A36L/D7wfurSDPT/Av6H/D
r4Z7RudxYFnVercKvzV9z60hz7pmt458de3n6si3gXxg2US+TeTbQr4t5NtG
vm3k20G+HeTbRT6w7CHfHvLtI98+8h0g3wHyHSLfIfL9QT6wNLTeNODX0Pd8
A/mamk0Tv6ep/XwT+Vo6jwG7ltb7Fvo70vfMEfoCe+ilrf1MG8+rrfN4sHTQ
Xwf9ddBfB/110V8X/XXRXxf99dAf2PXQXw/9HaO/Y/QH9tBLH/310V8f/YEl
RH8h+gvRX4j+BuhvgP4G6G+A/oboD+yG6G+I/k7Q3wn6A3voZYT+RuhvhP7A
MkZ/Y/Q3Rn9j9Gc1Bxa/x2o/a5HP6jwl2ENfwU8ifS+I8DzBFnoXab8ywvOK
dJ4KLLHWBzGeR6zv2RjPF1xC7+FX4Z4kOk8ANonW20T7uUTfKxPsDVxBL6n2
C1LsKdV5LNhBX8LPp/pelWJ/GfaXYX+Z9rMZ9pdhf2APfQU/ybG/HPsDW+hd
rv3KHPvLsT+wTLC/ifYzE+xvgv2BS+g9/CrckwL7A5sC+yu0nyuwvwL7A1fQ
y+l/v3/i8uLs
"]]}}, 
{RGBColor[0.368417, 0.506779, 0.709798], PointSize[0.009166666666666668], 
      AbsoluteThickness[1.6]}, {
{RGBColor[0.368417, 0.506779, 0.709798], PointSize[0.009166666666666668], 
       AbsoluteThickness[1.6]}, {}}, {
{RGBColor[0.368417, 0.506779, 0.709798], PointSize[0.009166666666666668], 
       AbsoluteThickness[1.6]}, {}}}, {{}, {}}},
AspectRatio->0.6180339887498948,
Axes->{True, True},
AxesLabel->{None, None},
AxesOrigin->{0., 0},
DisplayFunction->Identity,
Frame->{{False, False}, {False, False}},
FrameLabel->{{None, None}, {None, None}},
FrameTicks->{{Automatic, Automatic}, {Automatic, Automatic}},
GridLines->{None, None},
GridLinesStyle->Directive[
GrayLevel[0.5, 0.4]],
Method->{"OptimizePlotMarkers" -> True, 
     "CoordinatesToolOptions" -> {"DisplayFunction" -> ({
(Identity[#]& )[
Part[#, 1]], 
(Identity[#]& )[
Part[#, 2]]}& ), "CopiedValueFunction" -> ({
(Identity[#]& )[
Part[#, 1]], 
(Identity[#]& )[
Part[#, 2]]}& )}},
PlotRange->{{0., 200.}, {-1, 1}},
PlotRangeClipping->True,
PlotRangePadding->{{
Scaled[0.02], 
Scaled[0.02]}, {0, 0}},
Ticks->{Automatic, Automatic}]\)

In[41]:= c = a1 + a2;

In[42]:= Export["~/ssa_20211008/graph3.csv", c, "CSV"]

Out[42]= "~/ssa_20211008/graph3.csv"

In[43]:= ListPlot[c, Joined -> True]

Out[43]= \!\(\*
GraphicsBox[{{}, {{{}, {}, 
{RGBColor[0.368417, 0.506779, 0.709798], PointSize[0.009166666666666668], 
       AbsoluteThickness[1.6], LineBox[CompressedData["
1:eJw1lQlQVdcdxi9aRYslFKsVgvFZGdwghkXcED5kURRk37f34G1MDBbcosVy
q4mpRm2CGYLgjM9GLKZ0YNQQMAYuVYkKmECIiuDwigtBISJSQ1CklfedO8O8
+fif/zn3fb//d97cjM1RugmSJF35/9+rT8sz4Deh8YztSO73fvwH1nrXzb9Q
1UU9BduiXxaFuJmp7dDv9LZbftoP1L9D8dFXz2nqWbB9Z+ph94HmOot2wnso
bHQdaqdWwfxtQn1shNB/wLKrRRHzHa5RO3O/Gu7nAqO7wzZ1ezv1AsRdt1/7
se1d6kUo2+felKcW2hUxe1uO3L/UQf0mPMefi9Rvwd/kU6+dV8/z3PHG7SW6
hkPfU3tgV9Zg0uPeVmpPtA1/av1F0XlqL77fVe63FD2Nde/cnSP88cYBq+Bd
l/wfUC9DZ412rOKI0MtxZ+j10dIZ/6FeAcvnd9Qr8V1YXUt60gmetwrZPQWj
dRuFPz5wmTyr97fWV6lXQx5/gc3Uvvy+gqcfHMcGTTOjhT/A1147//Xz1l6L
loHX+j/1uNtALfnDbkH4W+3r7rHuD/34c4P1NagcrKnM6qtkfQ0Clx7UPJj4
Fc8PwLncwuUHtlZbtBwA9cqSxX8urmZ/IP0jTzkQGz1c2kL2CX+CMGAoNy8q
62M9CGtUjbqZI9RSMAKT92ROy+thPRjNTa+eTtbXwqVhYalVwGXW10I5vzC/
6eR2vt86INvD7llELuvr8CKruNvGUfAMIQ/ylEPwF12i9e4a4c96OJd0TU/r
eMz6enz1avuZA6xvwI7DXxT6VTxkfQO/r+Adil0hz5f3WLewHoq+0VMtoUuE
P2HIU46NlNWeZz0M2pKz8ZuetrK+kXzJU96Ic0UHV1b2CX/Csdiw/7N1Hzxh
PRwxF2fpfSuppQh8Xv/j1dzufotGBP0TvCNgrtAcD8u+adFKBBo2mJZuuXeF
/ZGwdXt9/VzXa+yPxDUrx9rWRMEzkvNCnkokhu53VT15TfgThcvSvNXdqqfs
j8JPKWfGboZQy1HIHjn0svUA1ytR5PEj+6MRPPPKpHNtd9gfjZCD3lamW/RH
jkb/iy02O/I4/0o0PIyy8wpF3Gcx5EGeiMHh/J0RH54WfsUgrfjCjT+dH2J/
DD54tuFozl1qKRZTPplftMl5kP2x5PGI/bGI8/2996HZ3eyPRcXgMcNkP3F/
xSE683bOnW5qxCHUsOVy+HTBM448yFOJw3yH6Q+dA+iPFI9hz7g/zoh5xv54
zP3ovofNbmo5Hn93q3efXMv1Sjx5/MT+BOzPWZ+lRNxnfwJmJE68vqmU/sgJ
6NSq+k44c/6VBOQXnxreEyzymUge5INEKGfK99Z20h85EQXNj6dW9P/M/kTm
Y5j9SfD5JqnxePx/2Z/E78v95CR8fXL3sad7yVtJQm2XV3HvJHF/JcOuKHrO
D/HUSMbZ5vbFVTvFfZZMvuSpJCMpNHh2wnb6I6XAdTwfv7A/hfmgllPQph7S
rnjC9UoK/SNvKRWPb1Z+6/IleSMVA/bGZqcV9EdOxZrGfVFTPhTzn4r70m/S
e8tFPtM4L2L+05gP+iOnMR/P2Z/GfFBL6cwH1yOdPIT/6Zhnc29C0kPyVtLh
HFwiRWwS95ca21/WvL+qllqlhoMXCpzMvM+gJg/up1YzH8IfNdLH8/HCok1q
/HU8H9SKmvkYsWizmjzIW9LA9bhNSYMt+ag0SNh53XPvcfoDDcrc+6uzn1Cr
NTh1tqb7H/tFPjXkQT4mDVzG8yH80jAfL3m+hvmgljKYD65XZZAH5xUZuLS8
1EtdRt7qDBwotzJUtYr7PsPy82HPeTVlAGHRef7zRN4yyIN8zBnMB/2RMpmP
MZ6fiTuf+OmjbCRLHzKZj1Gen0keYj4ykdbqe/0Xf/IxZaJrs2Pz0B4x75mY
0nT6bw//SW3OxO0HfTM6Loj7S0se5KnSMh/0B1oUnr0UefIi30etxeeaaZ5z
blHLWuaD601a8iBvRYvht28ZjnSQt1mLd6ee0x92EveXDid0AQvfC6JW6ZAr
76vYGifuMx15kI9ah5HBzR3D1uJ8HTLkj9/I+cjKok067HizfezRSWpFh2Wj
wflZQVxv1pGH8F+Pgkm5Vm7byFulh/1nYdKCKvoDPVaNdf57dpeYfz2mOapC
bAe4XtaTh5h/Pb6p8ym73MbzFD2WhKU9Wp06gefrEfi8tKk6h1oy4FfXpod6
2/N9VQbyIG8YmA/yURtQ7tNztD5c3O8GtBVtT/nyXTH/BuaD6xUDeYj5N+DI
wanbCk7wPMmIFw6Lq3+9aCLPN8LuSu7R932pYURLoXnWxC6uVxvJg/MqG5kP
8jYZEXRD9kzuFfe9kfkQ829kPsT9lcX3kPA/MvrPoQ==
"]]}}, 
{RGBColor[0.368417, 0.506779, 0.709798], PointSize[0.009166666666666668], 
      AbsoluteThickness[1.6]}, {
{RGBColor[0.368417, 0.506779, 0.709798], PointSize[0.009166666666666668], 
       AbsoluteThickness[1.6]}, {}}, {
{RGBColor[0.368417, 0.506779, 0.709798], PointSize[0.009166666666666668], 
       AbsoluteThickness[1.6]}, {}}}, {{}, {}}},
AspectRatio->0.6180339887498948,
Axes->{True, True},
AxesLabel->{None, None},
AxesOrigin->{0., 0},
DisplayFunction->Identity,
Frame->{{False, False}, {False, False}},
FrameLabel->{{None, None}, {None, None}},
FrameTicks->{{Automatic, Automatic}, {Automatic, Automatic}},
GridLines->{None, None},
GridLinesStyle->Directive[
GrayLevel[0.5, 0.4]],
Method->{"OptimizePlotMarkers" -> True, 
     "CoordinatesToolOptions" -> {"DisplayFunction" -> ({
(Identity[#]& )[
Part[#, 1]], 
(Identity[#]& )[
Part[#, 2]]}& ), "CopiedValueFunction" -> ({
(Identity[#]& )[
Part[#, 1]], 
(Identity[#]& )[
Part[#, 2]]}& )}},
PlotRange->{{0., 200.}, {-0.40552825814757676`, 2.4055282581475765`}},
PlotRangeClipping->True,
PlotRangePadding->{{
Scaled[0.02], 
Scaled[0.02]}, {
Scaled[0.05], 
Scaled[0.05]}},
Ticks->{Automatic, Automatic}]\)

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
Association[
 "ObjectType" -> "Symbol", 
  "Usage" -> "\!\(\*RowBox[{\"SingularValueDecomposition\", \"[\", \
StyleBox[\"m\", \"TI\"], \"]\"}]\) gives the singular value decomposition for \
a numerical matrix \!\(\*StyleBox[\"m\", \"TI\"]\) as a list of matrices \!\(\
\*RowBox[{\"{\", RowBox[{StyleBox[\"u\", \"TI\"], \",\", StyleBox[\"w\", \"TI\
\"], \",\", StyleBox[\"v\", \"TI\"]}], \"}\"}]\), where \!\(\*StyleBox[\"w\", \
\"TI\"]\) is a diagonal matrix and \!\(\*StyleBox[\"m\", \"TI\"]\) can be \
written as \!\(\*RowBox[{StyleBox[\"u\", \"TI\"], \".\", StyleBox[\"w\", \"TI\
\"], \".\", RowBox[{\"Conjugate\", \"[\", RowBox[{\"Transpose\", \"[\", \
StyleBox[\"v\", \"TI\"], \"]\"}], \"]\"}]}]\). \n\
\!\(\*RowBox[{\"SingularValueDecomposition\", \"[\", RowBox[{\"{\", \
RowBox[{StyleBox[\"m\", \"TI\"], \",\", StyleBox[\"a\", \"TI\"]}], \"}\"}], \
\"]\"}]\) gives the generalized singular value decomposition of \
\!\(\*StyleBox[\"m\", \"TI\"]\) with respect to \!\(\*StyleBox[\"a\", \"TI\"]\
\). \n\!\(\*RowBox[{\"SingularValueDecomposition\", \"[\", \
RowBox[{StyleBox[\"m\", \"TI\"], \",\", StyleBox[\"k\", \"TI\"]}], \"]\"}]\) \
gives the singular value decomposition associated with the \!\(\*StyleBox[\"k\
\", \"TI\"]\) largest singular values of \!\(\*StyleBox[\"m\", \"TI\"]\). \n\
\!\(\*RowBox[{\"SingularValueDecomposition\", \"[\", RowBox[{StyleBox[\"m\", \
\"TI\"], \",\", RowBox[{\"UpTo\", \"[\", StyleBox[\"k\", \"TI\"], \"]\"}]}], \
\"]\"}]\) gives the decomposition for the \!\(\*StyleBox[\"k\", \"TI\"]\) \
largest singular values, or as many as are available. \n\
\!\(\*RowBox[{\"SingularValueDecomposition\", \"[\", RowBox[{RowBox[{\"{\", \
RowBox[{StyleBox[\"m\", \"TI\"], \",\", StyleBox[\"a\", \"TI\"]}], \"}\"}], \
\",\", StyleBox[\"k\", \"TI\"]}], \"]\"}]\) gives the generalized singular \
value decomposition associated with the \!\(\*StyleBox[\"k\", \"TI\"]\) \
largest singular values.", 
  "Documentation" -> Association[
   "Local" -> "paclet:ref/SingularValueDecomposition", 
    "Web" -> "http://reference.wolfram.com/language/ref/\
SingularValueDecomposition.html"], "OwnValues" -> None, "UpValues" -> None, 
  "DownValues" -> None, "SubValues" -> None, "DefaultValues" -> None, 
  "NValues" -> None, "FormatValues" -> None, 
  "Options" -> {Cubics -> False, Method -> Automatic, Quartics -> False, 
    Tolerance -> Automatic}, "Attributes" -> {Protected}, 
  "FullName" -> "System`SingularValueDecomposition"], False]

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
{RGBColor[0.368417, 0.506779, 0.709798], PointSize[0.012833333333333334`], 
       AbsoluteThickness[1.6], 
       LineBox[{{1., 4.6895665325705655`}, {2., 3.228808143890601}, {3., 
        3.219508365751631}, {4., 2.0489903635096143`}}]}}, 
{RGBColor[0.368417, 0.506779, 0.709798], PointSize[0.012833333333333334`], 
      AbsoluteThickness[1.6]}, {
{RGBColor[0.368417, 0.506779, 0.709798], PointSize[0.012833333333333334`], 
       AbsoluteThickness[1.6]}, {}}, {
{RGBColor[0.368417, 0.506779, 0.709798], PointSize[0.012833333333333334`], 
       AbsoluteThickness[1.6]}, {}}}, {{}, {}}},
AspectRatio->0.6180339887498948,
Axes->{False, False},
AxesLabel->{None, None},
AxesOrigin->{0.9375000000000003, 1.8423502929319653`},
DisplayFunction->Identity,
Frame->{{True, True}, {True, True}},
FrameLabel->{{None, None}, {None, None}},
FrameTicks->FrontEndValueCache[{{
Charting`ScaledTicks[{Log, Exp}], 
Charting`ScaledFrameTicks[{Log, Exp}]}, {
      Automatic, Automatic}}, {{{{2.302585092994046, 
FormBox["10", TraditionalForm], {0.01, 0.}, {
AbsoluteThickness[0.1]}}, {2.995732273553991, 
FormBox["20", TraditionalForm], {0.01, 0.}, {
AbsoluteThickness[0.1]}}, {3.912023005428146, 
FormBox["50", TraditionalForm], {0.01, 0.}, {
AbsoluteThickness[0.1]}}, {4.605170185988092, 
FormBox["100", TraditionalForm], {0.01, 0.}, {
AbsoluteThickness[0.1]}}, {1.6094379124341003`, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {1.791759469228055, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {1.9459101490553132`, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {2.0794415416798357`, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {2.1972245773362196`, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {2.70805020110221, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {3.4011973816621555`, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {3.6888794541139363`, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {4.0943445622221, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {4.248495242049359, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {4.382026634673881, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {4.499809670330265, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {5.0106352940962555`, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {5.298317366548036, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {5.703782474656201, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {5.991464547107982, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {6.214608098422191, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}}, {{2.302585092994046, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.01, 0.}, {
AbsoluteThickness[0.1]}}, {2.995732273553991, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.01, 0.}, {
AbsoluteThickness[0.1]}}, {3.912023005428146, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.01, 0.}, {
AbsoluteThickness[0.1]}}, {4.605170185988092, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.01, 0.}, {
AbsoluteThickness[0.1]}}, {1.6094379124341003`, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {1.791759469228055, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {1.9459101490553132`, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {2.0794415416798357`, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {2.1972245773362196`, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {2.70805020110221, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {3.4011973816621555`, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {3.6888794541139363`, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {4.0943445622221, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {4.248495242049359, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {4.382026634673881, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {4.499809670330265, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {5.0106352940962555`, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {5.298317366548036, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {5.703782474656201, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {5.991464547107982, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}, {6.214608098422191, 
FormBox[
TemplateBox[{0., 0.}, "Spacer2"], TraditionalForm], {0.005, 0.}, {
AbsoluteThickness[0.1]}}}}, {Automatic, Automatic}}],
GridLines->{None, None},
GridLinesStyle->Directive[
GrayLevel[0.5, 0.4]],
Method->{"OptimizePlotMarkers" -> True, 
     "CoordinatesToolOptions" -> {"DisplayFunction" -> ({
(Identity[#]& )[
Part[#, 1]], 
(Exp[#]& )[
Part[#, 2]]}& ), "CopiedValueFunction" -> ({
(Identity[#]& )[
Part[#, 1]], 
(Exp[#]& )[
Part[#, 2]]}& )}},
PlotRange->{{0.9375000000000003, 4.}, {1.8423502929319653`, 
    4.6895665325705655`}},
PlotRangeClipping->True,
PlotRangePadding->{{
Scaled[0.02], 
Scaled[0.02]}, {
Scaled[0.02], 
Scaled[0.05]}},
Ticks->{Automatic, 
Charting`ScaledTicks[{Log, Exp}]}]\)

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
{RGBColor[0.368417, 0.506779, 0.709798], PointSize[0.009166666666666668], 
       AbsoluteThickness[1.6], LineBox[CompressedData["
1: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
edzG30/EqoGDp1o+8PeTsEmkN7RbTwP/BWgM2Pg=
"]]}}, 
{RGBColor[0.368417, 0.506779, 0.709798], PointSize[0.009166666666666668], 
      AbsoluteThickness[1.6]}, {
{RGBColor[0.368417, 0.506779, 0.709798], PointSize[0.009166666666666668], 
       AbsoluteThickness[1.6]}, {}}, {
{RGBColor[0.368417, 0.506779, 0.709798], PointSize[0.009166666666666668], 
       AbsoluteThickness[1.6]}, {}}}, {{}, {}}},
AspectRatio->0.6180339887498948,
Axes->{True, True},
AxesLabel->{None, None},
AxesOrigin->{0, 0},
DisplayFunction->Identity,
Frame->{{False, False}, {False, False}},
FrameLabel->{{None, None}, {None, None}},
FrameTicks->{{Automatic, Automatic}, {Automatic, Automatic}},
GridLines->{None, None},
GridLinesStyle->Directive[
GrayLevel[0.5, 0.4]],
Method->{"OptimizePlotMarkers" -> True, 
     "CoordinatesToolOptions" -> {"DisplayFunction" -> ({
(Identity[#]& )[
Part[#, 1]], 
(Identity[#]& )[
Part[#, 2]]}& ), "CopiedValueFunction" -> ({
(Identity[#]& )[
Part[#, 1]], 
(Identity[#]& )[
Part[#, 2]]}& )}},
PlotRange->{{0, 200.}, {0, 2.1340713059251457`}},
PlotRangeClipping->True,
PlotRangePadding->{{
Scaled[0.02], 
Scaled[0.02]}, {
Scaled[0.02], 
Scaled[0.05]}},
Ticks->{Automatic, Automatic}]\)

In[121]:= xx = Sum[w[[i, i]] Outer[Times, Transpose[u][[i]], Transpose[v][[i]]], {i, 
    3}];

In[122]:= y1 = sn[xx];

In[123]:= ListPlot[y1, Joined -> True]

Out[123]= \!\(\*
GraphicsBox[{{}, {{{}, {}, 
{RGBColor[0.368417, 0.506779, 0.709798], PointSize[0.009166666666666668], 
       AbsoluteThickness[1.6], LineBox[CompressedData["
1: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
oSl3lke/I5v/ZHwsGHo8bK6BvwCC6tKs
"]]}}, 
{RGBColor[0.368417, 0.506779, 0.709798], PointSize[0.009166666666666668], 
      AbsoluteThickness[1.6]}, {
{RGBColor[0.368417, 0.506779, 0.709798], PointSize[0.009166666666666668], 
       AbsoluteThickness[1.6]}, {}}, {
{RGBColor[0.368417, 0.506779, 0.709798], PointSize[0.009166666666666668], 
       AbsoluteThickness[1.6]}, {}}}, {{}, {}}},
AspectRatio->0.6180339887498948,
Axes->{True, True},
AxesLabel->{None, None},
AxesOrigin->{0., 0},
DisplayFunction->Identity,
Frame->{{False, False}, {False, False}},
FrameLabel->{{None, None}, {None, None}},
FrameTicks->{{Automatic, Automatic}, {Automatic, Automatic}},
GridLines->{None, None},
GridLinesStyle->Directive[
GrayLevel[0.5, 0.4]],
Method->{"OptimizePlotMarkers" -> True, 
     "CoordinatesToolOptions" -> {"DisplayFunction" -> ({
(Identity[#]& )[
Part[#, 1]], 
(Identity[#]& )[
Part[#, 2]]}& ), "CopiedValueFunction" -> ({
(Identity[#]& )[
Part[#, 1]], 
(Identity[#]& )[
Part[#, 2]]}& )}},
PlotRange->{{0., 200.}, {-0.16395220841736205`, 2.528923518493486}},
PlotRangeClipping->True,
PlotRangePadding->{{
Scaled[0.02], 
Scaled[0.02]}, {
Scaled[0.05], 
Scaled[0.05]}},
Ticks->{Automatic, Automatic}]\)

In[124]:= xx = Sum[w[[i, i]] Outer[Times, Transpose[u][[i]], Transpose[v][[i]]], {i, 2, 
    40}];

In[125]:= y1 = sn[xx];

In[126]:= ListPlot[y1, Joined -> True]

Out[126]= \!\(\*
GraphicsBox[{{}, {{{}, {}, 
{RGBColor[0.368417, 0.506779, 0.709798], PointSize[0.009166666666666668], 
       AbsoluteThickness[1.6], LineBox[CompressedData["
1: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
/wNjrBEP
"]]}}, 
{RGBColor[0.368417, 0.506779, 0.709798], PointSize[0.009166666666666668], 
      AbsoluteThickness[1.6]}, {
{RGBColor[0.368417, 0.506779, 0.709798], PointSize[0.009166666666666668], 
       AbsoluteThickness[1.6]}, {}}, {
{RGBColor[0.368417, 0.506779, 0.709798], PointSize[0.009166666666666668], 
       AbsoluteThickness[1.6]}, {}}}, {{}, {}}},
AspectRatio->0.6180339887498948,
Axes->{True, True},
AxesLabel->{None, None},
AxesOrigin->{0., 0},
DisplayFunction->Identity,
Frame->{{False, False}, {False, False}},
FrameLabel->{{None, None}, {None, None}},
FrameTicks->{{Automatic, Automatic}, {Automatic, Automatic}},
GridLines->{None, None},
GridLinesStyle->Directive[
GrayLevel[0.5, 0.4]],
Method->{"OptimizePlotMarkers" -> True, 
     "CoordinatesToolOptions" -> {"DisplayFunction" -> ({
(Identity[#]& )[
Part[#, 1]], 
(Identity[#]& )[
Part[#, 2]]}& ), "CopiedValueFunction" -> ({
(Identity[#]& )[
Part[#, 1]], 
(Identity[#]& )[
Part[#, 2]]}& )}},
PlotRange->{{0., 200.}, {-0.7196831508520415, 0.5613284788306379}},
PlotRangeClipping->True,
PlotRangePadding->{{
Scaled[0.02], 
Scaled[0.02]}, {
Scaled[0.05], 
Scaled[0.05]}},
Ticks->{Automatic, Automatic}]\)

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
