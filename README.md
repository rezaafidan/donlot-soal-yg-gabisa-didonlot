
# **hack-brainacademy**
___
**donlot soal yg gabisa di donlot**

![logo](https://github.com/user-attachments/assets/dd00349c-6c1c-46ba-bd1d-173316c2c2c3)

---

### **Table of Contents**

- [HackScript](#HackScript)
- [Requirement](#Requirement)
- [Instruction](#Instruction)
- [Liscense](#Liscense)

 
### **HackScript**

Script download soal :

`firefox-console-script`

```
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
```

### **Requirement**

Required Tools :

1. mozila firefox is required (another browser are not supported)

### **Instruction**

Instruction using this script :

1. Retrieve **Brain Academy soal** via the Mozilla Firefox web browser
2. copy the hack script
3. open **Developer Tools** by pressing "**Ctrl+Shift+C**" on Windows
   or "**Cmd+Opt+I**" on Mac OS
5. open **console** tabs on developer tools
6. type "**allow pasting**"
7. paste the hack script
8. press **Enter**
9. the file will be downloaded
![Screenshot 2024-10-01 212452](https://github.com/user-attachments/assets/e436d267-5a68-47e1-abb5-2cb0cb2ac5a6)
![Screenshot 2024-10-01 212552](https://github.com/user-attachments/assets/09f7f5d3-eacf-44aa-a3f0-4d7d331edfa4)

### Licsense

support author :

- Neo Adiyatma instagram.com/nyotodd
- Reza Afidan linki.ee/rezaafidan
