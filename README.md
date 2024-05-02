# repositorioweb
Ejercicios web
comeplat js
const images = document.querySelectorAll('.image');
const modal = document.getElementById('modal');
const modalDescription = document.getElementById('modal-description');

images.forEach(image => {
    image.addEventListener('click', () => {
        modalDescription.textContemt = image.CDATA_SECTION_NODE.description;
        modal.style.display = 'block';
    });

});

document.querySelector('.close').addEventListener('click', () => {
    modal.style.display = 'none';

});


---------------------------

.image-container {
    display: flex;
    justify-content: space-around;
    margin-top: 20px;
}
 .image {
     width: 300px;
     height: 200px;
     object-fit: cover;
     cursor: pointer;
     transition: transform 0.3s ease_in_out;
 }

 .image:horver {
     transform: scale(1,1);
 }
 /* para al ventan modal
 */
 .modal {
     display: none;
     position: fixed;
     z-index: 1;
     left: 0;
     top: 0;
     width: 100%;
     height: 100%;
     background-color: rgba(0,0,0,0.5);
 }

 .modal-content {
     background-color: #fefefe;
     margin: 15% auto;
     padding: 20px;
     border: 1px solid #888;
     width: 50%;
     max-width: 300px;
     border-radius:10px;
     box-shadow: 0 5px 10px rgba(0,0,0, 0.3);
 }

 .close{
     color: #aaa;
     float: right;
     font-size: 28px;
     font-weight: bold;
 }
 .close:hover,
 .close:focus {
     color: black;
     text-decoration: none;
     cursor: pointer;
 }
 ----------------------------------------
 <!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Hello, world!</title>
    <link rel="stylesheet" type="text/css" href="completa.css">
  </head>
  <body>
    <h1>Mostrador de Productos</h1>
    <div class="image-container">
        <img src="D:\Disco extraíble - copia\imagens por usar/casa-de-la-moneda-1.jpg" alt="Image 1" class="image" data-
description="Cepillo Precio:25 Bs.-">
<img src="D:\Disco extraíble - copia\imagens por usar/6142bdb4caef990adb477f93.jpeg" alt="Image 2" class="image" data-
description="Detergente 5 Kgs Precio:95Bs.-">
<img src="D:\Disco extraíble - copia\imagens por usar/arani iglesia.jpg" alt="Image 3" class="image" data-
description="Javoncillo 25 Grs Precio:30 Bs.-">
    <div id="modal" class="modal">
        <div class="modal-content">
            <span class="close">&times;</span>
            <p id="modal-description"></p>
        </div>
    </div>
    </div>
    <script src="completa.js"></script>
  </body>
</html>
