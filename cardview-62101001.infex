<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Weather</title>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.0-beta1/dist/js/bootstrap.bundle.min.js" integrity="sha384-ygbV9kiqUc6oa4msXn9868pTtWMgiQaeYH7/t7LECLbyPA2x65Kgf80OJFdroafW" crossorigin="anonymous"></script>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.0-beta1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-giJF6kkoqNQ00vy+HMDP7azOuL0xtbfIcaT9wjKHr8RbDVddVHyTfAAsrekwKmP1" crossorigin="anonymous">
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
</head>

<style>
    .card {
      background-color : #89d0f3;
      width: 45%;
      margin: auto;
      margin-top: 20px;
      margin-bottom: 20px;
      padding-top: 30px;
      padding-bottom: 30px;
      border: 3px dashed black; width: 500px;

    }
    .card:hover {
      box-shadow: 0 8px 16px 0 #064463;
    }
    .container {
      padding: 2px 16px;
    }
    .weather{
      padding-left: 23px;
      padding-bottom: 5px;
    }
    .search_weather{
      padding-left: 23px;
      
    }
   h3{
      padding-top: 15px;
   }
   body{
        background-color:rgb(208, 239, 253);
    }
    </style>

<body>
   
  <div class="container">  
         <div class="card">
         <u> <h2><b><center> Check the climate view card</center></b></h2></u>
         <center><img src="https://www.gelschool.com/geleducation/images/map6.png" alt="map" style="width:50%"></center> 
          <div class="row">
           <center> <input type="text" id="la" placeholder="Latitude" class="form-control" style="width: 40%; margin-left: 25px; margin-top: 20px; text-align: center;" >
            <input type="text" id="long" placeholder="Longitude" class="form-control" style="width: 40%;margin-left: 20px;  margin-top: 20px; text-align: center">
            <a>
            <button id="load" class="btn btn-primary btn-sm" style=" width: 100px; margin-top: 10px; margin-right: -20px; "><b>Load</b></button>
            </a></center>
        </div>
         
            <div class="weather">      
          <center> <h3><span id="name"> At &#127780;&#127758;</span><br> </h3></center> <p></p>
              <h5>  <span id="coun_try">Country: </span><br>
                <span id="main_temp">Temp: </span> Celsius<br>
                <span id="main_tempmax">Temp max: </span> Celsius<br>
                <span id="main_tempmin">Temp min: </span> Celsius<br>
                <span id="humi_dity">Humidity: </span> %<br>
                <span id="sunrise">Sunrise: </span> unix<br>
                <span id="sunset">Sunset: </span> unix<br>
                <span id="winddeg">Wind deg: </span> degree<br>
                <span id="windspeed">Wind speed: </span> m/s<br>
                <span id="clouds">Cloud: </span> %<br></h5>
            </div>
            <div class="search_weather">
            <center><h3> At &#127780;&#127758; <span id="name1"> </span><br> </h3></center>  <p></p>
            <h5>  Country: <span id="coun_try1"> </span><br>
              Temp: <span id="main_temp1"> </span> Celsius<br>
              Temp max: <span id="main_temp_max1"> </span> Celsius<br>
              Temp min: <span id="main_temp_min1"> </span> Celsius<br>
              Humidity: <span id="humi_dity1"> </span> %<br>
              Sunrise: <span id="sunrise1"> </span> unix<br>
              Sunset: <span id="sunset1"> </span> unix<br>
              Wind deg: <span id="winddeg1"></span> degree<br>
              Wind speed: <span id="windspeed1"> </span> m/s<br>
              Cloud: <span id="clouds1"> </span> %<br></h5>
            </div>
          </div>
         </div>
    </div>  
          
 <script> 
   function weather_loading(){ 
     $(".search_weather").hide();
     var url ="https://api.openweathermap.org/data/2.5/weather?lat=8.795540&lon=99.843698&appid=e8916dd91122d70a0b9527ebfefc1ccc&units=metric";
     
           $.get(url)
            .done((data)=>{
              console.log(data)
                $("#name").append(data.name);
                $("#main_temp").append(data.main.temp);
                $("#main_tempmax").append(data.main.temp_max);
                $("#main_tempmin").append(data.main.temp_min);
                $("#humi_dity").append(data.main.humidity);
                $("#coun_try").append(data.sys.country);
                $("#sunrise").append(data.sys.sunrise);
                $("#sunset").append(data.sys.sunset);
                $("#winddeg").append(data.wind.deg);
                $("#windspeed").append(data.wind.speed);
                $("#clouds").append(data.clouds.all);
                      })         
           .fail((xhr, status, err)=>{
                    console.log("error")
                });   
          }
   function weather_searching(){ 
           $(".weather").hide();
           $(".search_weather").show();
           var url ="https://api.openweathermap.org";
           var a = $("#la").val();
           var b = $("#long").val();

           url = url + "/data/2.5/weather?lat=" + a + "&lon=" + b +"&appid=e8916dd91122d70a0b9527ebfefc1ccc&units=metric"; 
           
            $.getJSON(url)
            .done((data)=>{
              console.log(data)
              $("#name1").append(data.name);
              $("#main_temp1").append(data.main.temp);
              $("#main_tempmax1").append(data.main.temp_max);
              $("#main_tempmin1").append(data.main.temp_min);
              $("#humi_dity1").append(data.main.humidity);
              $("#coun_try1").append(data.sys.country);
              $("#sunrise1").append(data.sys.sunrise);
              $("#sunset1").append(data.sys.sunset);
              $("#winddeg1").append(data.wind.deg);
              $("#windspeed1").append(data.wind.speed);
              $("#clouds1").append(data.clouds.all);
                      })         
           .fail((xhr, status, err)=>{
                    console.log("error")
                });
          }     
    function remove(){
         $("#name1").empty();
         $("#main_temp1").empty();
         $("#main_tempmax1").empty();
         $("#main_tempmin1").empty();
         $("#humi_dity1").empty();
         $("#coun_try1").empty();
         $("#sunrise1").empty();
         $("#sunset1").empty();
         $("#winddeg1").empty();
         $("#windspeed1").empty();
         $("#clouds1").empty();
    }
    $(()=>{ 
      weather_loading();
            $("#load").click(()=>{ 
              weather_searching();
            });
            $("#load").click(()=>{
                remove();
            });   
     });
   </script>        
  </body>
</html>