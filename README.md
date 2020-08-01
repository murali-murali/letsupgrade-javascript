# letsupgrade-javascript
Project 
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
