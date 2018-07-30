# VideoDemo
A demo only for authorized users (A kiosk mode)
<script src="http://apps.bdimg.com/libs/jquery/2.1.1/jquery.min.js"></script>

<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.5.0/css/font-awesome.min.css" integrity="sha384-XdYbMnZ/QjLh6iI4ogqCTaIjrFk87ip+ekIjefZch0Y+PvJ8CDYtEs1ipDmPorQ+" crossorigin="anonymous"

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Test</title>
    <link rel="stylesheet" href="style.css">
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta charset="UTF-8">
    <title>VideoDemo</title>
    <link rel="stylesheet" href="https://cdn.bootcss.com/bootstrap/3.3.7/css/bootstrap.min.css" integrity="sha384-BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u" crossorigin="anonymous">
</head>
</head>

<style type="text/css">
::-webkit-media-controls{
    display:none !important;
}

#demo-bar-badge {
    display: inline-block;
    width: 302px;
    padding: 0 !important;
    margin: 0 !important;
    background-color: transparent !important;
    color: #FFFFFF;
    font-size: 50px;
    font-family: Gulim;
  }


#video{
    width: 740px;
    height:680px;
    margin-top: -100;
}

body{
 background: url(http://www.designbolts.com/wp-content/uploads/2014/03/Blue-Blur-Background1.jpg) no-repeat center;
overflow-x: hidden;
}

#demo-top-bar {
    text-align: left;
    background: #222;
    position: relative;
    zoom: 1;
    width: 104%;
    z-index: 6000;
    padding: 15px 150PX 15px;
    margin-left:-20px;


  }

#all{
    margin:0 auto;
    width: 740px;
    height:680px;
    position: relative;
}

.butDemo{
     position: absolute;

  background:#454545;
  bottom: 180px;
   width: 740;
   margin-left: -370px;

}

#paragraph{

font-family: Arail black;
font-size: 28px;
color:#FFF;
font-weight: bold;

}

#paragraph2{

font-family: Arail black;
font-size: 18px;
color:#FFF;

}


</style>




<body align="center" class="container-fluid">
    
<div id="demo-top-bar">
  <h1 id="demo-bar-badge" ><b>Video Demo</b></h1>
</div>
<br>
<br>
<br>
<br>

<p id="paragraph">This page is currently only supported by Google chrome </p>
<p id="paragraph2"> and make sure you have the updated version of the browser</p>       

<div id="all">
     <video  loop  id="video" >
        <source src="mov_bbb.mp4" type="video/mp4">
    </video>
<button onclick="goFullscreen('video'); return false" class="btn btn-info butDemo" > <i class="fa fa-send-o"></i>  Start the demo</button>
</div>




<script>
     var password = "123456789";
function goFullscreen(id) {
    
    var inputPassword;
    var password = "123456789";

    inputPassword=prompt("Enter password to start the demo");
    if(inputPassword==password){
    var element = document.getElementById(id);

    if (element.mozRequestFullScreen) {
      element.mozRequestFullScreen();
    } else if (element.webkitRequestFullScreen) {
      element.webkitRequestFullScreen();
   }  else if (element.msRequestFullScreen) {
      element.msRequestFullScreen();
   }

element.play();




}

else{
    alert("Only authorized operation is allowed")
  }




}























</script>
</body>
</html>
