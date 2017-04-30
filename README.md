#html file
<!Doctype html>
<html>
<head>
<title>BMI calculator
</title>
<link rel="stylesheet" href="bmi style.css">

</head>
<body>
<div id ="wrap">
<div id="headerout">

<div id="header">
<div id="logo">
<a href="#" >
<img src="" width="265" height="29"</a>
</div>
</div>


</div>


</div>
<div id="clear"></div>
<div id="main">
<div id="content">
<H1>BMI CALCULATOR</H1>
<p><img src="images/bar.png"></p>
<div id="leftinput">
<div id="topmenu" class="topmenucenter">
<ul>
<li id="menuon">
<a href="#" onclick="popmenu('standard',1);return false;">us units</a></li>
<li>
<a href="#" onclick="popmenu('metric',1);return false;">Metric units</a></li>
<li>
<a href="#" onclick="popmenu('other',0);return false;">other units</a>
</li>
</ul>
<div class="panel2">
<table id="calinputtable" width="263">
<form name="calform"></form>
<input type="hidden" name="ctype" id="ctype" value="standard">
<tbody>
<tr>
<td width="50">Age</td>
<td align="right" width="140"><input type="text" name="cage" value="25" class="innormal"> </td>
<td width="73">&nbsp </td>
</tr>
<tr>
<td>Gender</td>
<td align="right" >
<label for="csex1">
<input type="radio" name="csex" id="csex1" value="m" checked>
Male
</label>
&nbsp;
<label for="csex2"> 
<input type="radio" name="csex" id="csex2" value="f" >
FeMale</label>
</td>
<td >&nbsp </td>

</tr>
</tbody>
</table>
<table width="263" id="standardheightweight" bgcolor="#eeeeee" style="display:none;">
<tbody>
<tr>
<td width="50">Height</td>
<td align="right" width="140">
<input type="text" name="cheightfeet" id="cheightfeet" value="5" class="in2char">
"Feet"
<input type="text" name="cheightinch" id="cheightinch" value="10" class="in2char">
</td>
<td width="73">inches</td>
</tr>
<tr id="metricweight">
<td>Weight</td>
<td align="right">
<input type="text" name="cpound" id="cpound" value="160" class="innormal"></td>
<td>pounds</td>
</tr>

</tbody></table>
<table width="263" bgcolor="#eeeeee" >
<tbody>
<tr>
<td colspan="2" align="right" width="190"><input name="printit" value="0" type="hidden" >
<input type="images"  src="images/calculate.png" value="calculate" alt="calculate">
</td>
<td width="73">&nbsp;</td>
</tr>
</tbody>
</table>
</div>

</div>
</div>
<div id="rightoutput"></div>

<script></script>
<br>
<p>The Body Mass Index (BMI) Calculator can be used to calculate your BMI value and weight status while taking your age into consideration. Use the "metric units" tab if you are more comfortable with the international standard metric units. The referenced weight range and calculation formula is listed below.</p>
<h2>Reference</h2>
<p>Your BMI is a measurement of your body weight based on your height and weight. Although your BMI does not actually "measure" your percentage of body fat, it is a useful tool to estimate a healthy body weight based on your height. Due to its ease of measurement and calculation, it is the most widely used diagnostic indicator to identify a person's optimal weight depending on his height. Your BMI "number" will inform you if you are underweight, of normal weight, overweight, or obese. However, due to the wide variety of body types, the distribution of muscle and bone mass, etc., it is not appropriate to use this as the only or final indication for diagnosis.
</p>
</div>
<div id="right"></div>
</div>
<script>

function popMenu(inval, insubmit){
	htmlVal = "";
	if (inval == "metric"){
		htmlVal = htmlVal + "<li><a href=\"#\" onclick=\"popMenu('standard',1);return false;\">US Units</a></li> <li id='menuon'><a href=\"#\" onclick=\"popMenu('metric',1);return false;\">Metric Units</a></li> <li><a href=\"#\" onclick=\"popMenu('other',0);return false;\">Other Units</a></li>";
		gObj("ctype").value="metric";
		gObj("standardheightweight").style.display = 'none';
		gObj("metricheightweight").style.display = 'block';
		htmlVal = "<ul>" + htmlVal + "</ul>";
		gObj("ucframe").innerHTML ="";
		if (insubmit==1) document.calform.submit();
	}else if (inval == "standard"){
		htmlVal = htmlVal + "<li id='menuon'><a href=\"#\" onclick=\"popMenu('standard',1);return false;\">US Units</a></li> <li><a href=\"#\" onclick=\"popMenu('metric',1);return false;\">Metric Units</a></li> <li><a href=\"#\" onclick=\"popMenu('other',0);return false;\">Other Units</a></li>";
		gObj("ctype").value="standard";
		gObj("standardheightweight").style.display = 'block';
		gObj("metricheightweight").style.display = 'none';
		htmlVal = "<ul>" + htmlVal + "</ul>";
		gObj("ucframe").innerHTML ="";
		if (insubmit==1) document.calform.submit();
	}else{
		htmlVal = gObj("topmenu").innerHTML ;
		gObj("ucframe").innerHTML = "<iframe src=\"/converter/converter.php?type=\" style=\"overflow:hidden;width:100%\" width=\"100%\" height=\"238\" frameborder=\"NO\" scrolling=\"NO\" allowTransparency=\"true\" ></IFRAME>";
	}
	gObj("topmenu").innerHTML = htmlVal;
}
popMenu("standard",0);
</script>
<div id="clear"></div>
<div id="footer">

<a href="#">ABOUT US</a>
|
©Adeel hassan 
</div>
</div>
</body>
</html>
