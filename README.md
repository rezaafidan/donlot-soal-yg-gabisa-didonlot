
download undownloadable
 
### **Script**

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

### **Instruction**

Instruction using this script :

1. Retrieve **pdf** via web browser
2. copy the script
3. open **Developer Tools** by pressing :
- "**Ctrl+Shift+C**" on Windows or
- "**Cmd+Opt+I**" on Mac OS
4. open **console** tabs on developer tools
5. type "**allow pasting**" and enter
6. paste the script and enter
