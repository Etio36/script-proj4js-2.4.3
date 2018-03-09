# script-proj4js-2.4.3
script to convert coordinates etrs89 to wgs84 


hi, i am using proj4js 2.4.3 and programming a schttps://github.com/Etio36/script-proj4js-2.4.3ript to convert coordinates etrs89 to wgs84 can someone give me an opinion on whether it is correct? do not know if i am using proj4js well? I have imported the files proj4.js and proj4-src.js and estouy using it in visual studio. my script is:
<script src="~/Scripts/proj4-src.js"></script>

     <script src="~/Scripts/proj4.js"></script>

     <script type="text/javascript">
         alert("ok!");
         convertir('723544', '4347185', '0')

         
         function convertir (x, y, z){
             var head1 = document.getElementsByTagName("head")[0];
             var s = document.createElement('script');
             s.type = '/text/javascript';
             s.src = '~/Scripts/proj4.js';
             head1.appendChild(s);
            

             Systeme1 = new proj4.Proj("EPSG:25830");      
             Systeme2 = new proj4.Proj("EPSG:4326");   Coordenadas Geográficas WGS84"
             alert("ok!");
             var Point = new proj4.toPoint('723544', '4347185', '0');
             Point =  proj4(Systeme1, Systeme2 ).forward(Point);
             alert("punto= " & Point);
             return Point;

            
         }
     </script>
