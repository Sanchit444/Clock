Skip to content
Search or jump to…
Pull requests
Issues
Marketplace
Explore
 
@Sanchit444 
Sanchit444
/
Clock
Public
1
00
Code
Issues
Pull requests
Actions
Projects
Wiki
Security
Insights
Settings
Add files via upload
 main
@Sanchit444
Sanchit444 committed 9 minutes ago 
1 parent 7196f6b commit 665a171fa436290973a47d3c41977036d0779a28
Showing  with 93 additions and 0 deletions.
 59  clock.css 
@@ -0,0 +1,59 @@
#clockcontainer{
    position: relative;
    margin: auto;
   /* border: 2px solid red; */
    height: 450px;
    width: 450px;
    background: url(clock3.jpg) no-repeat;
    background-size: 100%; 
    /* background-size: cover; */

}
#hours, #minute, #second{
    position: absolute;
    background: white;
    border-radius: 10px;
    transform-origin: bottom;
}
#hours{
    width: .5%;
    height: 10%;
    top: 24%;
    /* left: 49%; */
     left: 51%; 
    opacity: 0.8;
    /* display: none;
    /* display: none; */
}
#minute{
    width: .34%;
    height: 13%;
    top: 21%;
     left: 51%; 
    /* left: 54%; */
    opacity: 0.8;
     /* display: none; */
}
#second{
    width: .15%;
    height: 15%;
    top: 19%;
    /* left: 47%; */
    left: 51%;
    opacity: 0.8;
    /* display: none; */
    /* transform-origin: 67% 76.3%; */


}

.dot {
    position: absolute;
    height: 13px;
    width: 14px;
    background-color: white;
    border-radius: 50%;
    display: inline-block;
    top: 32%;
    left: 50%;
} 
 21  clock.html 
@@ -0,0 +1,21 @@
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Clock</title>
    <link rel="stylesheet" href="clock.css">
    <script src="clock.js"></script>
  </head>
  <body>
    <div id="clockcontainer">
      <div id="hours"></div>
      <div id="minute"></div>
      <div id="second"></div>
      <!-- <div id="hours"></div> -->
      <div class="container">
      <div class="dot"></div>
    </div></div> 
  </body>
</html>
 13  clock.js 
@@ -0,0 +1,13 @@
setInterval(() => {
    // console.log("")
    d = new Date();
    ht= d.getHours();
    mt = d.getMinutes();
    st = d.getSeconds();
    hr = 30*ht+mt/2;
    mr = 6*mt;
    sr = 6*st;
      hours.style.transform = `rotate(${hr}deg)`;
      minute.style.transform = `rotate(${mr}deg)`;
      second.style.transform = `rotate(${sr}deg)`;
}, 1000); 
 BIN +26.9 KB clock3.jpg 
Binary file not shown.
0 comments on commit 665a171
@Sanchit444
 
 
Leave a comment
No file chosen
Attach files by dragging & dropping, selecting or pasting them.
 You’re receiving notifications because you’re watching this repository.
© 2021 GitHub, Inc.
Terms
Privacy
Security
Status
Docs
Contact GitHub
Pricing
API
Training
Blog
About
Loading complete
