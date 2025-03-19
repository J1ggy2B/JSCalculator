//-------Calculator--------------------------------------------------------------------
function clearScrn(val)
{
document.getElementById("ip").value = val;
}

function append(val)
{
document.getElementById("ip").value += val;
}

function evaluateScrn() 
{ 
try 
{ 
  clearScrn(eval(document.getElementById("ip").value)) 
} 
catch(e) 
{
document.getElementById("disp").value = "Err!"
} 
} 
//------------Calculator----Memory Functions------------------------------------

function addToMem()
{

var val = document.getElementById("ip").value;
if( (val ==="") || (val === null) )
		{
		document.getElementById("ip").value = "Mem Null Err";
		}	
	else{
		localStorage.setItem("memVal", val);
		document.getElementById("ip").value = "";
		}	
}

function recallMem()
{
		if( (localStorage.getItem("memVal") ==="") || (localStorage.getItem("memVal")=== null) )
		{
		document.getElementById("ip").value = "Null";
		}	
	else{
		document.getElementById("ip").value += localStorage.getItem("memVal");
		}	
}
function clearMem()
{
		if( (localStorage.getItem("memVal") ==="") || (localStorage.getItem("memVal")=== null) )
		{
		document.getElementById("ip").value = "Mem Empty";
		}	
	else{
		localStorage.removeItem("memVal");
		document.getElementById("ip").value = "";
		}	
}

