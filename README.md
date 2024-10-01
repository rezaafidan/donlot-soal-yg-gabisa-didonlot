# hack-brainacademy
menghapuskan kesenjangan reguler

![logo](https://github.com/user-attachments/assets/dd00349c-6c1c-46ba-bd1d-173316c2c2c3)

script hack download soal :

let jspdf = document.createElement( "script" );
jspdf.onload = function () {
let pdf = new jsPDF();
let elements = document.getElementsByTagName( "img" );
for ( let i in elements) {
let img = elements[i];
if (!/^blob:/.test(img.src)) {
continue ;
}
let canvasElement = document.createElement( 'canvas' );
let con = canvasElement.getContext( "2d" );
canvasElement.width = img.width;
canvasElement.height = img.height;
con.drawImage(img, 0, 0,img.width, img.height);
let imgData = canvasElement.toDataURL( "image/jpeg" , 1.0);
pdf.addImage(imgData, 'JPEG' , 0, 0);
pdf.addPage();
}
pdf.save( "download.pdf" );
};
jspdf.src = 'https://cdnjs.cloudflare.com/ajax/libs/jspdf/1.3.2/jspdf.min.js' ;
document.body.appendChild(jspdf);
.
note :
1. mozila firefox is required (another browser are not supported)
2. allow cookies
3. allow javascript
4. enable developer mode

instruction :
1. Retrieve **Brain Academy soal** via the Mozilla Firefox web browser-
2. copy the hack script..
3. open **inspect element**
4. open **console** tabs on inspect element
5. type "**allow pasting**"
6. paste the hack script
7. press **Enter**
8. the file will be downloaded
![Screenshot 2024-10-01 212452](https://github.com/user-attachments/assets/e436d267-5a68-47e1-abb5-2cb0cb2ac5a6)
![Screenshot 2024-10-01 212552](https://github.com/user-attachments/assets/09f7f5d3-eacf-44aa-a3f0-4d7d331edfa4)

support author :
linkti.ee/rezaafidan
