<html>
   <head>
     <script>

var tBase = new Array();
tBase[0] = new Array('url_duzego_obrazka1.jpg','url_malego_obrazka1.jpg');
tBase[1] = new Array('url_duzego_obrazka2.jpg','url_malego_obrazka1.jpg');
tBase[2] = new Array('url_duzego_obrazka3.jpg','url_malego_obrazka1.jpg');
tBase[3] = new Array('url_duzego_obrazka4.jpg','url_malego_obrazka1.jpg');
tBase[4] = new Array('url_duzego_obrazka5.jpg','url_malego_obrazka1.jpg');

function fPrev(x){
   vCurrentImg = x;
   document.getElementById('iImgPrev').src = tBase[x][0];
}
window.onload = function(){
   var a = '<img id="iImgPrev" src="'+tBase[0][0]+'"><br>';
   for (i=0; i<tBase.length; i++) a += '<a href="javascript:fPrev('+i+')"><img class="thumb" src="'+tBase[i][1]+'" /></a>';
   document.getElementById('browser').innerHTML = a;
}
     </script>
   </head>
   <body>
     <div id="browser"></div>
   </body>
