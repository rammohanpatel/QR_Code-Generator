# QR_Code-Generator


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="qrcode.css">
    <title>QR-Code Generator</title>
</head>
<body>
    <div class="container">
        <p>Enter your text or URL</p>
        <input type="text" placeholder="Text or URL" id="qrtext">
        <div id="Imgbox">
        <img src="" id="qrImage">
        </div>
        <button onclick="generateQR()">Generate QR-Code</button>

    </div>
    
    <script>
        let imgbox=document.getElementById("Imgbox")
        let qrImage=document.getElementById("qrImage")
        let qrtext=document.getElementById("qrtext")

        function generateQR(){
            if(qrtext.value.length > 0){
               qrImage.src=" https://api.qrserver.com/v1/create-qr-code/?size=150x150&data="+qrtext.value;
               Imgbox.classlist.add("show-img");
            }
        }
    </script>
</body>
</html>


//css

*{
    margin: 0;
    padding: 0;
    font-family: sans-serif,'Poppins';
}

body{
    background:#080808 ;
}

.container{
    background: #fff;
    border-radius:  10px;
    width: 400px;
    padding: 25px 35px;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
.container p{
    font-weight: 1000;
    font-size: 30px;
    margin-bottom: 8px;
    text-align: center;
}
.container input{
    width: 100%;
    height: 25px;
    border: 1px solid #494eea;
    outline: 0;
    padding: 10px;
    padding: 10px;
    margin: 10px 0 20px;
    border-radius: 5px;
}
.container button{
    width:100%;
    height: 50px;
    background: #494eea;
    color: #fff;
    border:0;
    outline: 0;
    border-radius: 5px;
    box-shadow:0 10px 10px rgba(0,0,0,0.1);
    cursor: pointer;
    margin: 20px 0;
    font-weight: 500;
}
#Imgbox{
    width: 200px;
    border-radius:5px;
    max-height: 300px;
    margin: 10px auto;
    /*border: 1px solid #d1d1d1;
    /*overflow: hidden;
    transition: max-height 1s;*/
}

#Imgbox img{
    width:100%;
    padding: 10px;
    margin: 10px auto;
}
/*
#Imgbox.show-img{
    max-height:300px;
    margin: 10px auto;
    border: 1px solid #d1d1d1;
}

 
