<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chào mừng các bạn</title>
    <style>
        #NoiDung {
            border-style: double; 
            border-width: 3px; 
            padding: 4px 4px 1px 4px;
        }
        .TieuDe {
            font-size: 30pt;
            font-weight: bold;
        }
        .NoiDung {
            font-size: 15pt;
            font-weight: italic;
        }
    </style>
</head>
<body>

<p>JAVASCRIPT và CSS</p>
<p>
    <input type="button" value="Xanh" name="B3" onclick="MauXanh()">
    <input type="button" value="  Đỏ  " name="B4" onclick="MauDo()">
    <input type="button" value="Vàng" name="B5" onclick="MauVang()">
    <input type="button" value="Không màu" name="B6" onclick="KhongMau()">
</p>

<p>
    <select id="fontSize" size="1">
        <option value="20px">20px</option>
        <option value="40px">40px</option>
        <option value="90px">90px</option>
    </select>
    <input type="button" value="Đặt cỡ chữ" onclick="DatCoChu()">
</p>

<p>
    <select id="heightSize" size="1">
        <option value="100px">100px</option>
        <option value="200px">200px</option>
        <option value="400px">400px</option>
    </select>
    <input type="button" value="Đặt chiều cao" onclick="DatChieuCao()">
    <input type="button" value="Tăng chiều cao" onclick="TangChieuCao()">
</p>

<input type="button" value="Nạp css tiêu đề" onclick="NapCssTieuDe()">
<input type="button" value="Nạp css nội dung" onclick="NapCssNoiDung()">

<div id="NoiDung">
    #NoiDung: Xin chào các bạn!
</div>

<script>
    function MauXanh() {
        document.getElementById("NoiDung").style.backgroundColor = "Green";
    }

    function MauDo() {
        document.getElementById("NoiDung").style.backgroundColor = "Red";
    }

    function MauVang() {
        document.getElementById("NoiDung").style.backgroundColor = "Yellow";
    }

    function KhongMau() {
        document.getElementById("NoiDung").style.backgroundColor = "";
    }

    function DatCoChu() {
        var select = document.getElementById("fontSize");
        var size = select.options[select.selectedIndex].value;
        document.getElementById("NoiDung").style.fontSize = size;
    }

    function DatChieuCao() {
        var select = document.getElementById("heightSize");
        var height = select.options[select.selectedIndex].value;
        document.getElementById("NoiDung").style.height = height;
    }

    function TangChieuCao() {
        var content = document.getElementById("NoiDung");
        var currentHeight = content.offsetHeight;
        content.style.height = (currentHeight + 50) + "px"; 
    }


    function NapCssTieuDe() {
        var tieuDe = document.getElementById("NoiDung");
        tieuDe.style.fontSize = "40px"; 
        tieuDe.style.fontWeight = "bold"; 
        tieuDe.style.color = "blue"; 
    }


    function NapCssNoiDung() {
        var noiDung = document.getElementById("NoiDung");
        noiDung.style.fontSize = "20px"; 
        noiDung.style.fontStyle = "italic"; 
        noiDung.style.color = "green"; 
    }
</script>

</body>
</html>
