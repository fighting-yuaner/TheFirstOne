# TheFirstOne
#I have no idea

<!DOCTYPE html>
<html>
<head>
<script>
var c=0;
var t;
var timer_is_on=0;

function timedCount()
{
document.getElementById('txt').value=c;
c=c+1;
t=setTimeout(function(){timedCount()},1000);
}

function doTimer()
{
if (!timer_is_on)
  {
  timer_is_on=1;
  timedCount();
  }
}

function stopCount()
{
clearTimeout(t);
timer_is_on=0;
}
</script>
</head>

<body>
<form>
<input type="button" value="Start count!" onclick="doTimer()" />
<input type="text" id="txt" />
<input type="button" value="Stop count!" onclick="stopCount()" />
</form>
<p>
Click on the "Start count!" button above to start the timer. The input field will count forever, starting at 0. Click on the "Stop count!" button to stop the counting. Click on the "Start count!" button to start the timer again.
</p>
</body>
</html>
