<html>
<body>
<title>Display Webcam Stream</title>
<style>
#container {
margin: 0px auto;
 width: 100%;
height: auto;
border: 0px #333 solid;
}
#a {
width: 100%;
height: auto;
align: center;
}
</style>
<body>
<div id="container">
<center>
<video autoplay controlls id="a"style="border:5px ridge aqua;border-radius:8px;video-align: center;"></video>
</center>
<script>
 var video = document.querySelector("#a");
if (navigator.getUserMedia) {       
    navigator.getUserMedia({video: true}, handleVideo, videoError);
}
function handleVideo(stream) {
    video.src = window.URL.createObjectURL(stream);
}
function videoError(e) {}
</script>
</body>
</html>
