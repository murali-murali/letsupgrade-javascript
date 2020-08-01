# letsupgrade-javascript
Project 1
<!doctype html>
 <html lang="en">
                      
  <head>                
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

 <title> project 1</title>
    <style>
   
      
      body {
    font-family: 'Poppins', sans-serif;
    
     
}



h1{
    color: rgb(49, 49, 49);
    margin-top: 40px;
    text-align: center;
    font-size: 32px;
}

.input-group{
    
    margin: 50px 0px;
}

.input-group input{
    height: 45px;
    
}

.btn-add{

    background-color: blue;
    color: white;
    padding: 0px 63px;
}

.btn-remove{

    background-color: red;
    color: white;
    padding: 0px 50px;
}

ul{
    display: flex;
    -ms-flex-direction: column;
    flex-direction: column;
    padding-left: 0;
    margin-bottom: 0;

    
}
li{
    position: relative;
    display: block;
    padding: 10px 20px;
    margin-bottom: 10px;
    background-color:
    #fff;
    border: 1px solid
    rgba(0,0,0,.125);
    border-top-left-radius: .25rem;
    border-top-right-radius: .25rem;
    border-bottom-left-radius: .25rem;
    border-bottom-right-radius: .25rem;
    
}



      
    </style>
      </head>
                      
      <body>              
     <div class="container">
      <div class="row">
         <h1> Add & Remove Items From List Using JavaScript</h1>
    <hr>                   
     <div class="input-group">
     <input type="text" class="form-control" id="candidate" required>
      <button onclick="addItem()" class="btn btn-add" type="button">Add Item</button>
    <button onclick="removeItem()" class="btn btn-remove" type="button">Remove Item</button>
        </div>
       <ul id="dynamic-list">
       </ul>
                      
  </div>
   </div>
   </div>
     <script>
                      
      function addItem() {
      var ul = document.getElementById("dynamic-list");
      var candidate = document.getElementById("candidate");
      var li = document.createElement("li");
      li.setAttribute('id', candidate.value);
      li.appendChild(document.createTextNode(candidate.value));
      ul.appendChild(li);
  }
  
  
  function removeItem() {
      var ul = document.getElementById("dynamic-list");
      var candidate = document.getElementById("candidate");
      var item = document.getElementById(candidate.value);
      ul.removeChild(item);
  }


              </script>        
                      </body>

                      </html>
               
                    
           Project 2
           
      <!DOCTYPE html>

<html>
    <head>
    <style>
        #outputBox {
    width : 150px;
    height : 25px;
 background-color:  DarkGoldenRod;
   border: 1px solid ;

 text-align:center;
}

body { 
font-family: 'Poppins', sans-serif; 
background: rgb(107,186,222); 
background: -moz-linear-gradient(90deg, rgba(107,186,222,1) 0%, rgba(232,156,205,1) 100%); 
background: -webkit-linear-gradient(90deg, rgba(107,186,222,1) 0%, rgba(232,156,205,1) 100%); 
background: linear-gradient(90deg, rgba(107,186,222,1) 0%, rgba(232,156,205,1) 100%); 
filter: progid:DXImageTransform.Microsoft.gradient(startColorstr="#6bbade",endColorstr="#e89ccd",GradientType=1); 
} 


#startpause{
    background-color: Grey;
    width : 50px;
    height : 25px;
    border : 1px solid #999;

}
#reset{
background-color: Grey;
    width : 50px;
    height : 25px;
    border : 1px solid #999;

}

        
</style>
        <meta http-equiv="CONTENT-TYPE" content="text/html; charset=UTF-8">
        <title> STOP WATCH PROJECT 2 </title>
    </head>

    <body bgcolor="AntiqueWhite" >
        <h1>STOP WATCH </h1>
     
    <p id="outputBox"</p>
   <div class="container">  
    <button id="startpause" onclick="startpause()" > Start </button>
    <button id="reset" onclick="reset()">Reset</button> 
    </div>
     
     <script> 
         
    var  time=0;
    var running=0;
    
    function startpause(){
     if(running==0) {
       running=1;
       increment();
      document.getElementById("startpause").innerHTML= "pause";
       }
       else 
       {
       running=0;
        document.getElementById("startpause").innerHTML= "resume";
      }
       }

    function reset() {
       running=0;
       time=0;
      document.getElementById("startpause").innerHTML= "start";
      document.getElementById("outputBox").innerHTML= "00:00:00";
       }

    function increment(){
       if(running ==1) {
     setTimeout(function(){
       time++;
       var mins =Math.floor(time/10/60);
       var secs =Math.floor(time/10);
       var tenths= time % 10;
      if(mins<10) {
 mins= "0"+mins;

}
if(secs<10){

secs = "0" + secs;

}


       Car("outputBox").innerHTML=mins+":"+secs+":"+tenths;
       increment();
       },100)
       }
       }
    </script>
    </body>
</html>
 
 
 
 
 
 Project 3
 
 <!DOCTYPE html>

<html>
    <head> 
      <meta http-equiv="CONTENT-TYPE" content="text/html; charset=UTF-8">
        <title> project 3</title>
     <style>
         
h1 {
   text-align :center;
}
      
#btn{

  background-color: Cyan;
  height : 100px;
   width : 250px;
   font-size : 15px;
   margin : 0 auto;

}
#container{
     background-color: blue;
    
     height :100px;
     width: 250px;
    margin:0 auto;
   text-align: center;


}
#output{

   background-color: Cyan;
   height : 100px;
   width : 250px;
   margin : 0 auto;

}     

     </style>
    </head>
    
    <body bgcolor="Beige">
        <h1>Quotus</h1>
   <div id="container">
     
     <div id="output">  welcome To My Quatos</div>
       <button id="btn">press the next Quotus </button>
   </div>
       
        
   <script>
   
    let btn = document.getElementById("btn");
    let output = document.getElementById("output");
    let quotes= [
       
       '“The purpose of our lives is to be happy.” — Dalai Lama',

'“Life is what happens when you’re busy making other plans.” — John Lennon',

'“Get busy living or get busy dying.” — Stephen King',

 '“You only live once, but if you do it right, once is enough.” — Mae West',

'“Many of life’s failures are people who did not realize how close they were to success when they gave up.”– Thomas A. Edison',

'If you want to live a happy life, tie it to a goal, not to people or things.”– Albert Einstein',

' “Never let the fear of striking out keep you from playing the game.”– Babe Ruth',
       
'“Money and success don’t change people; they merely amplify what is already there.” — Will Smith',

'“Your time is limited, so don’t waste it living someone else’s life. Don’t be trapped by dogma – which is living with the results of other people’s thinking.” – Steve Jobs',

'“The purpose of our lives is to be happy.” — Dalai Lama',

' “Life is what happens when you’re busy making other plans.” — John Lennon',
       
 '“Get busy living or get busy dying.” — Stephen King',

' “You only live once, but if you do it right, once is enough.” — Mae West',

'“Many of life’s failures are people who did not realize how close they were to success when they gave up.”– Thomas A. Edison',


'“If you want to live a happy life, tie it to a goal, not to people or things.”– Albert Einstein',
       
'“Never let the fear of striking out keep you from playing the game.”– Babe Ruth',

'“Money and success don’t change people; they merely amplify what is already there.” — Will Smith',

' “Your time is limited, so don’t waste it living someone else’s life. Don’t be trapped by dogma – which is living with the results of other people’s thinking.” – Steve Jobs',

'“Not how long, but how well you have lived is the main thing.” — Seneca',

' “If life were predictable it would cease to be life, and be without flavor.” – Eleanor Roosevelt',

'“The whole secret of a successful life is to find out what is one’s destiny to do, and then do it.”– Henry Ford',

'“In order to write about life first you must live it.”– Ernest Hemingway',

'“The big lesson in life, baby, is never be scared of anyone or anything.”– Frank Sinatra'
  ];
   btn.addEventListener('click',function() {
 var randomQuote= quotes[Math.floor(Math.random() * quotes.length)]

output.innerHTML=randomQuote;

})     
   </script>
    </body>
</html>

 
 
 
