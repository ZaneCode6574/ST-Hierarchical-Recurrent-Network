# Introduction
The primary goal of articulated object motion prediction is to generate future motion by observing sequence of 3D skeletons. Currently, people focus on creatures such as human and animals motion prediction. As we scrutinized current methods, we found that previous workings always focused on the temporal angle, which ignores the fine-grained spatial aspect and the inner relationship of one pose. Meanwhile, state-of-art models only obtained well results on simple activities for long-term prediction. To dig out the reasons behind this and address these problems, we proposed a novel spatio-temporal hierarchical recurrent network, which can simultaneously model local and global sptio-temporal context. Furthermore, a structured stack LSTM decoder is used to obtain spine, arm, and leg respectively. In the end, a novel loss function is introduced to compute a quantized weight for each bone of one pose. Extensive experiments demonstrated the superiority of our model on both short-term and long-term motion prediction over state-of-art models.

# Visualization of long-term prediction

&nbsp;&nbsp;

## Walking


<center><iframe width="560" height="315" src="https://www.youtube.com/embed/4Z1IWTl-_7w" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>

&nbsp;

## Posing


<center><iframe width="560" height="315" src="https://www.youtube.com/embed/UptXczFf6Ro" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>

&nbsp;

## Eating


<center><iframe width="560" height="315" src="https://www.youtube.com/embed/Scur-WShQ5Y" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>

&nbsp;

# Results on short-term prediction

<html xmlns:o="urn:schemas-microsoft-com:office:office"
xmlns:x="urn:schemas-microsoft-com:office:excel"
xmlns="http://www.w3.org/TR/REC-html40">

<head>
<meta http-equiv=Content-Type content="text/html; charset=utf-8">
<meta name=ProgId content=Excel.Sheet>
<meta name=Generator content="Microsoft Excel 15">
<link rel=File-List href="工作簿1.fld/filelist.xml">
<style id="工作簿1_6812_Styles">
<!--table
	{mso-displayed-decimal-separator:"\.";
	mso-displayed-thousand-separator:"\,";}
@page
	{margin:.75in .7in .75in .7in;
	mso-header-margin:.3in;
	mso-footer-margin:.3in;}
.font5
	{color:windowtext;
	font-size:9.0pt;
	font-weight:400;
	font-style:normal;
	text-decoration:none;
	font-family:等线;
	mso-generic-font-family:auto;
	mso-font-charset:134;}
tr
	{mso-height-source:auto;
	mso-ruby-visibility:none;}
col
	{mso-width-source:auto;
	mso-ruby-visibility:none;}
br
	{mso-data-placement:same-cell;}
.style0
	{mso-number-format:General;
	text-align:general;
	vertical-align:middle;
	white-space:nowrap;
	mso-rotate:0;
	mso-background-source:auto;
	mso-pattern:auto;
	color:black;
	font-size:12.0pt;
	font-weight:400;
	font-style:normal;
	text-decoration:none;
	font-family:等线;
	mso-generic-font-family:auto;
	mso-font-charset:134;
	border:none;
	mso-protection:locked visible;
	mso-style-name:常规;
	mso-style-id:0;}
.style26
	{background:#C6EFCE;
	mso-pattern:black none;
	color:#006100;
	font-size:12.0pt;
	font-weight:400;
	font-style:normal;
	text-decoration:none;
	font-family:等线;
	mso-generic-font-family:auto;
	mso-font-charset:134;
	mso-style-name:好;
	mso-style-id:26;}
.style35
	{background:#FFFFCC;
	mso-pattern:black none;
	border:.5pt solid #B2B2B2;
	mso-style-name:注释;
	mso-style-id:10;}
td
	{mso-style-parent:style0;
	padding-top:1px;
	padding-right:1px;
	padding-left:1px;
	mso-ignore:padding;
	color:black;
	font-size:12.0pt;
	font-weight:400;
	font-style:normal;
	text-decoration:none;
	font-family:等线;
	mso-generic-font-family:auto;
	mso-font-charset:134;
	mso-number-format:General;
	text-align:general;
	vertical-align:middle;
	border:none;
	mso-background-source:auto;
	mso-pattern:auto;
	mso-protection:locked visible;
	white-space:nowrap;
	mso-rotate:0;}
.xl63
	{mso-style-parent:style0;
	text-align:center;}
.xl64
	{mso-style-parent:style35;
	font-size:11.0pt;
	font-weight:700;
	text-align:center;
	border-top:.5pt solid windowtext;
	border-right:.5pt solid windowtext;
	border-bottom:.5pt solid windowtext;
	border-left:.5pt solid #B2B2B2;}
.xl65
	{mso-style-parent:style0;
	font-size:11.0pt;
	text-align:center;
	border-top:none;
	border-right:.5pt solid windowtext;
	border-bottom:.5pt solid windowtext;
	border-left:none;}
.xl66
	{mso-style-parent:style0;
	font-size:11.0pt;
	text-align:center;
	border-top:none;
	border-right:.5pt solid windowtext;
	border-bottom:.5pt solid windowtext;
	border-left:.5pt solid windowtext;}
.xl67
	{mso-style-parent:style0;
	font-size:11.0pt;
	text-align:center;
	border-top:none;
	border-right:none;
	border-bottom:.5pt solid windowtext;
	border-left:.5pt solid windowtext;}
.xl68
	{mso-style-parent:style0;
	font-size:11.0pt;
	text-align:center;}
.xl69
	{mso-style-parent:style26;
	font-size:11.0pt;
	font-weight:700;
	text-align:center;
	border:.5pt solid windowtext;}
.xl70
	{mso-style-parent:style26;
	font-size:11.0pt;
	font-weight:700;
	text-align:center;
	border-top:.5pt solid windowtext;
	border-right:none;
	border-bottom:.5pt solid windowtext;
	border-left:.5pt solid windowtext;}
.xl71
	{mso-style-parent:style26;
	font-size:11.0pt;
	font-weight:700;
	text-align:center;
	border-top:.5pt solid windowtext;
	border-right:.5pt solid windowtext;
	border-bottom:.5pt solid windowtext;
	border-left:none;}
.xl72
	{mso-style-parent:style35;
	font-size:11.0pt;
	text-align:center;
	border:.5pt solid windowtext;}
.xl73
	{mso-style-parent:style35;
	font-size:11.0pt;
	text-align:center;
	border-top:.5pt solid windowtext;
	border-right:.5pt solid #B2B2B2;
	border-bottom:.5pt solid windowtext;
	border-left:.5pt solid windowtext;}
.xl74
	{mso-style-parent:style0;
	font-size:11.0pt;
	text-align:center;
	border-top:.5pt solid windowtext;
	border-right:.5pt solid windowtext;
	border-bottom:.5pt solid windowtext;
	border-left:none;}
.xl75
	{mso-style-parent:style0;
	font-size:11.0pt;
	text-align:center;
	border:.5pt solid windowtext;}
.xl76
	{mso-style-parent:style0;
	font-size:11.0pt;
	text-align:center;
	border-top:.5pt solid windowtext;
	border-right:none;
	border-bottom:.5pt solid windowtext;
	border-left:.5pt solid windowtext;}
ruby
	{ruby-align:left;}
rt
	{color:windowtext;
	font-size:9.0pt;
	font-weight:400;
	font-style:normal;
	text-decoration:none;
	font-family:等线;
	mso-generic-font-family:auto;
	mso-font-charset:134;
	mso-char-type:none;
	display:none;}
-->
</style>
</head>

<body link="#0563C1" vlink="#954F72">
<!--[if !excel]>　　<![endif]-->
<!--下列信息由 Microsoft Excel 的发布为网页向导生成。-->
<!--如果同一条目从 Excel 中重新发布，则所有位于 DIV 标记之间的信息均将被替换。-->
<!----------------------------->
<!--“从 EXCEL 发布网页”向导开始-->
<!----------------------------->

<div id="工作簿1_6812" align=center x:publishsource="Excel">

<table border=0 cellpadding=0 cellspacing=0 width=783 style='border-collapse:
 collapse;table-layout:fixed;width:585pt'>
 <col width=87 span=9 style='width:65pt'>
 <tr height=21 style='height:16.0pt'>
  <td rowspan=2 height=42 class=xl63 width=87 style='height:32.0pt;width:65pt'>Methods</td>
  <td colspan=8 class=xl68 width=696 style='width:520pt'>Directions</td>
 </tr>
 <tr height=21 style='height:16.0pt'>
  <td height=21 class=xl65 style='height:16.0pt'>80ms</td>
  <td class=xl66 style='border-left:none'>160ms</td>
  <td class=xl66 style='border-left:none'>320ms</td>
  <td class=xl66 style='border-left:none'>400ms</td>
  <td class=xl66 style='border-left:none'>560ms</td>
  <td class=xl66 style='border-left:none'>640ms</td>
  <td class=xl66 style='border-left:none'>720ms</td>
  <td class=xl67 style='border-left:none'>1000ms</td>
 </tr>
 <tr height=21 style='height:16.0pt'>
  <td height=21 style='height:16.0pt'>ST_HMR</td>
  <td class=xl71 style='border-top:none'>0.41</td>
  <td class=xl69 style='border-top:none;border-left:none'>0.58</td>
  <td class=xl69 style='border-top:none;border-left:none'>0.78</td>
  <td class=xl69 style='border-top:none;border-left:none'>0.86</td>
  <td class=xl69 style='border-top:none;border-left:none'>0.98</td>
  <td class=xl69 style='border-top:none;border-left:none'>1.04</td>
  <td class=xl69 style='border-top:none;border-left:none'>1.19</td>
  <td class=xl70 style='border-top:none;border-left:none'>1.48</td>
 </tr>
 <tr height=21 style='height:16.0pt'>
  <td height=21 style='height:16.0pt'>ERD</td>
  <td class=xl74 style='border-top:none'>1.06</td>
  <td class=xl75 style='border-top:none;border-left:none'>1.17</td>
  <td class=xl75 style='border-top:none;border-left:none'>1.19</td>
  <td class=xl75 style='border-top:none;border-left:none'>1.24</td>
  <td class=xl75 style='border-top:none;border-left:none'>1.33</td>
  <td class=xl75 style='border-top:none;border-left:none'>1.41</td>
  <td class=xl75 style='border-top:none;border-left:none'>1.51</td>
  <td class=xl76 style='border-top:none;border-left:none'>1.79</td>
 </tr>
 <tr height=21 style='height:16.0pt'>
  <td height=21 style='height:16.0pt'>LSTM-3LR</td>
  <td class=xl74 style='border-top:none'>0.97</td>
  <td class=xl75 style='border-top:none;border-left:none'>1.07</td>
  <td class=xl75 style='border-top:none;border-left:none'>1.18</td>
  <td class=xl75 style='border-top:none;border-left:none'>1.25</td>
  <td class=xl75 style='border-top:none;border-left:none'>1.37</td>
  <td class=xl75 style='border-top:none;border-left:none'>1.45</td>
  <td class=xl75 style='border-top:none;border-left:none'>1.55</td>
  <td class=xl76 style='border-top:none;border-left:none'>1.79</td>
 </tr>
 <tr height=21 style='height:16.0pt'>
  <td height=21 style='height:16.0pt'>SRNN</td>
  <td class=xl74 style='border-top:none'>0.673</td>
  <td class=xl75 style='border-top:none;border-left:none'>0.93</td>
  <td class=xl75 style='border-top:none;border-left:none'>1.02</td>
  <td class=xl75 style='border-top:none;border-left:none'>1.16</td>
  <td class=xl75 style='border-top:none;border-left:none'>1.36</td>
  <td class=xl75 style='border-top:none;border-left:none'>1.44</td>
  <td class=xl75 style='border-top:none;border-left:none'>1.57</td>
  <td class=xl76 style='border-top:none;border-left:none'>1.9</td>
 </tr>
 <tr height=21 style='height:16.0pt'>
  <td height=21 style='height:16.0pt'>Res-GRU</td>
  <td class=xl74 style='border-top:none'>0.48</td>
  <td class=xl75 style='border-top:none;border-left:none'>0.69</td>
  <td class=xl75 style='border-top:none;border-left:none'>0.9</td>
  <td class=xl75 style='border-top:none;border-left:none'>1.03</td>
  <td class=xl75 style='border-top:none;border-left:none'>1.15</td>
  <td class=xl75 style='border-top:none;border-left:none'>1.23</td>
  <td class=xl75 style='border-top:none;border-left:none'>1.37</td>
  <td class=xl76 style='border-top:none;border-left:none'>1.7</td>
 </tr>
 <tr height=21 style='height:16.0pt'>
  <td height=21 style='height:16.0pt'>Zero-velocit<span style='display:none'>y</span></td>
  <td class=xl74 style='border-top:none'>0.39</td>
  <td class=xl75 style='border-top:none;border-left:none'>0.59</td>
  <td class=xl75 style='border-top:none;border-left:none'>0.79</td>
  <td class=xl75 style='border-top:none;border-left:none'>0.89</td>
  <td class=xl75 style='border-top:none;border-left:none'>1.02</td>
  <td class=xl75 style='border-top:none;border-left:none'>1.08</td>
  <td class=xl75 style='border-top:none;border-left:none'>1.22</td>
  <td class=xl76 style='border-top:none;border-left:none'>1.5</td>
 </tr>
 <tr height=21 style='height:16.0pt'>
  <td height=21 style='height:16.0pt'>MHU</td>
  <td class=xl74 style='border-top:none'>-</td>
  <td class=xl74 style='border-top:none'>-</td>
  <td class=xl74 style='border-top:none'>-</td>
  <td class=xl74 style='border-top:none'>-</td>
  <td class=xl74 style='border-top:none'>-</td>
  <td class=xl74 style='border-top:none'>-</td>
  <td class=xl74 style='border-top:none'>-</td>
  <td class=xl74 style='border-top:none'>-</td>
 </tr>
 <tr height=21 style='height:16.0pt'>
  <td height=21 style='height:16.0pt'>HMR</td>
  <td class=xl64 style='border-top:none'>0.41</td>
  <td class=xl72 style='border-top:none;border-left:none'>0.6</td>
  <td class=xl72 style='border-top:none;border-left:none'>0.82</td>
  <td class=xl72 style='border-top:none;border-left:none'>0.91</td>
  <td class=xl72 style='border-top:none;border-left:none'>1.04</td>
  <td class=xl72 style='border-top:none;border-left:none'>1.1</td>
  <td class=xl72 style='border-top:none;border-left:none'>1.26</td>
  <td class=xl73 style='border-top:none;border-left:none'>1.57</td>
 </tr>
 <![if supportMisalignedColumns]>
 <tr height=0 style='display:none'>
  <td width=87 style='width:65pt'></td>
  <td width=87 style='width:65pt'></td>
  <td width=87 style='width:65pt'></td>
  <td width=87 style='width:65pt'></td>
  <td width=87 style='width:65pt'></td>
  <td width=87 style='width:65pt'></td>
  <td width=87 style='width:65pt'></td>
  <td width=87 style='width:65pt'></td>
  <td width=87 style='width:65pt'></td>
 </tr>
 <![endif]>
</table>

</div>


<!----------------------------->
<!--“从 EXCEL 发布网页”向导结束-->
<!----------------------------->
</body>

</html>
