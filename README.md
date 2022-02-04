<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        body{
            background-color: rgb(46, 46, 46);
            display: flex;
            justify-content: center;
            align-items: center;
        }
        #container{
            color: rgb(228, 213, 213);
            font-size: 100px;
            text-align: center;
            height: 350px;
            font-family:Arial, Helvetica, sans-serif;
            border: 5px solid white;
            border-left: 5px solid  crimson;
            border-right: 5px solid cyan;
            border-top: 5px solid greenyellow;
            /* border: ; */
            padding: 50px 50px;
            border-radius:0px ;
            box-shadow: rgba(75, 145, 236, 0.2) 0px 2px 65px;

         
            
            /* cursor: pointer; */
            
            

        }
        #hr{
            color: rgb(21, 191, 197);
        }
        #sec{
            color: crimson;
        }
       
        p{
            font-size: 50px;
            margin: 0px 0 30px 0;
            font-family:'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
        }
        #samay{
            font-size: 20px;
            font-family:monospace;
        }
        
    </style>

</head>
<body>
    <div id="container">
        <p id = "text">CLOCK</p>
        <span class="clock" id = "hr">00</span>
        <span class = "figure">:</span>
        <span class="clock" id = "min">00</span>
        <span class = "figure">:</span>
        <span class="clock" id = "sec">00</span>
        <span class="clock" id = "samay">AM</span>

        <!-- <div id="btn">
            <button id = "btn-container" onclick="Start()">Start</button>
        </div> -->
    </div>
    <script>
         var randomColor = Math.floor(Math.random()*16777215).toString(16);
         console.log(randomColor);

      
            let para = document.getElementById("text");
            para.style.color = "#" + randomColor;

      
       
        // setTimeout(function(){
           
        //     para.style.color = "#" + randomColor;
        // }, 1000);


   function newDate(){
    var time = new Date();
    var hrs = time.getHours();
    var Mins = time.getMinutes();
    var secs = time.getSeconds();
    if(hrs < 10){
        hrs = "0"+ hrs;
      
    }
    if(Mins < 10){
        Mins = "0"+ Mins;


    }
    if(secs < 10){
        secs = "0"+ secs;

    }
    if(hrs > 12 ){
        document.getElementById("samay").innerHTML = "PM";
    }else{
        document.getElementById("samay").innerHTML = "AM";
    }

    document.getElementById("hr").innerHTML = hrs;
    document.getElementById("min").innerHTML = Mins;
    document.getElementById("sec").innerHTML = secs;

  }
  setInterval(newDate);



   </script>  


</body>
</html>
