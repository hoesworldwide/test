<!doctype html>
<html>
  <head>
    <title>Demo Seite</title>
    <link rel="stylesheet" type="text/css" href="css/demo-site.css" />
    <script>
        function error() {
            alert("Die Positionsbestimmung ist Fehlgeschlagen!")
        }   
         
        function success(pos){
            alert("Längengrad: " + pos.coords.longitude + " und Breitengrad: " + pos.coords.latitude);
        }       
         
        if (navigator.geolocation){
            navigator.geolocation.getCurrentPosition(success, error);
        }else{
            alert("Geoortung wird nicht unterstützt!");
        }
    </script>
  </head>
  <body>
    <h1><a href="http://www.webentwickler-oase.de">Webentwickler-Oase (zur&uuml;ck zum Blog)</a></h1>    
    <p class="center">Deine Koordinaten werden in einem Popup ausgegeben. Füge diese einfach in das Google Maps Suchfenster ein, um deine Position auf einer Karte anzuzeigen.</p>
  </body>
</html>
