# Yen hoc web frontend 
*Mục lục*

1. [Tạo hai khối](#bai1)
2. [Gắn link vào hình và chỉnh hover](#bai2)
3. [Tạo nhiều tin nhỏ ngang](#bai3)
4. [Gắn/ nhúng video](#bai4)
5. [Gắn icon](#bai5)
6. [Hiệu ứng đổi màu và nhích lên + chữ giữa đường kẻ](bai6)
7. [chồng khối](bai7)



## 1.TẠO HAI KHỐI <a name="bai1"></a>
```html
<div class="khoi-tong">
    <div class="noidung">
        <h2>khối 1</h2>
        <img class="img-noidung" src="../assets/images/team-1.jpg">
        <p class="doan">Lorem Ipsum has been the industry's standard dummy text ever since the</p>
    </div>
    <div class="noidung">
        <h2>khối 2</h2>
        <img class="img-noidung" src="../assets/images/team-1.jpg">
        <p class="doan">Lorem Ipsum has been the industry's standard dummy textr<p>              
    </div>         
</div>
```
```css
/*chỉnh 2 khối*/
.noidung{
    background-color: white;
    width: 960px;
    height: 400px;
    margin-bottom: 10px;
    padding-top : 20px;
    padding-bottom: 0px;
    border-bottom: 1px solid/*đường thẳng*/ red; /* đường kẻ giữa 2 khối */
    padding-left: 10px;
}
.doan{
    /*font-style: 20px;*/
    /*font-weight: bold; (in đậm)*/
    font-family: Arial;
    line-height: 30px; /*(giãn dòng)*/ 
}
.img-noidung{
    width: 150px;
    float: left; /*hình bên trái chữ*/
    margin-right: 20px; /* chữ nằm ngay khung */
}
.khoi-tong{
    width: 1000px;
    border: 2px solid blueviolet; /*viền tím*/
}
```
## 2. Gắn link vào hình và chỉnh hover <a name="bai2"></a>
```html
 <div class="gan-link-hinh-hover">
    <a href="https://www.facebook.com/"><img class="hinh-hover" src="../assets/images/work-1.jpg"></a>
    <h3>tạp chí</h3>
    <a class="link-chu" href="https://www.facebook.com/">hình mèo con</a>
</div>
```
```css
/*gan link và chỉnh hover*/
.gan-link-hinh-hover{
    width: 860px;
    background-color: yellow;
}
.hinh-hover{
   width: 100%;
}
.link-chu{
    text-decoration: none;
    color: black;
    font-weight: bold;
    font-size: 20px;
    font-family: arial;
    display: block;
    margin-bottom: 10px;  
}
a.link-chu:hover{
    text-decoration: none;
    color: orangered;
    text-decoration: none;
}
```
## 3. TẠO NHIỀU TIN NHỎ NGANG <a name="bai3"></a>
```html
<article class="tin-phu">
    <div class="nhieu-tin-nho-ngang">
        <a  href="https://www.facebook.com/"><img class="hinh-nho" src="../assets/images/team-1.jpg"></a>
        <a class="link-chu" href="https://www.facebook.com/">tên bài gì đó dài thật dài luôn á ngen</a>
        <p>1 giờ trước</p>
    </div>

    <div class="nhieu-tin-nho-ngang">
        <a  href="https://www.facebook.com/"><img class="hinh-nho" src="../assets/images/team-1.jpg"></a>
        <a class="link-chu" href="https://www.facebook.com/">tên bài gì đó dài thật dài luôn á ngen</a>
        <p>1 giờ trước</p>
    </div>
</article>
```
```css
/*nhiều khối ngang*/
article.tin-phu{
    padding: 10px;
    background-color: green;
    width: 860px;
    display: block;
    margin-bottom: 10px;
    overflow: hidden; /*không nhảy lum la*/
}
div.nhieu-tin-nho-ngang{
    width: 230px;
    float: left;
    margin-right: 10px;/*cách khung phải*/
    margin-left: 40px;/*cách khung trái*/
    padding-right:30px; /*chữ ngay hình*/
    padding-top: 20px;
}
.hinh-nho{
    width: 200px;
    height: 160px;
    padding-top:10px;
}
```
## 4. NHÚNG VIDEO <a name="bai4"></a>
> chọn chia sẻ video chọn nhúng và sao chép rồi dán vào
```html
<div class="nhung-video">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/BV2FdDmGiW0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
```
```css
/*nhúng video*/
.nhung-video{
    width: 100%;
    margin-top: 10px;
    /*text-align: center; giữa trang*/
}
```
## 5. GẮN ICON <a name="bai5"></a>
```html
<head>
    <!-- javascript -->
    <script src="https://kit.fontawesome.com/89b1e83cc8.js" crossorigin="anonymous"></script>
</head>

cách 1
<span style="font-size: 3em; color: Tomato;">
    <i class="fab fa-facebook-square"></i>
</span>
cách 2: chỉnh trong css
<div class="icon"> 
    <i class="fab fa-facebook-square"></i>
</div>
```
```css
/* gắn icon*/
.icon{
    color: blue;
    font-style: 60px;
}
```
## 6. HIỆU ỨNG ĐỔI MÀU VÀ NHẢY LÊN + chữ giữa đường kẻ <a name="bai6"></a>
```HTML
<div class="main-container">
    <div class="follow-title">
        <h3>follow us</h3>
    </div>
    <div class="follow-icon">
        <div class="icon">
            <i class="fab fa-facebook-square">
                <p class="chu-duoi-icon">fans</p>
            </i> 
        </div>
        <div class="icon tw">
            <i class="fab fa-facebook-square">
                <p class="chu-duoi-icon">followers</p>
            </i>
        </div>
        <div class="icon gg">
            <i class="fab fa-facebook-square">
                <p class="chu-duoi-icon">yen</p>
            </i>
        </div>
    </div>
</div>
```
```css
*{
    margin: 0;
    padding:0;
    border: none;
    background-color: grey;
}
.main-container{
    width: 450px;
    height: 260px;
    margin: 20px;
    padding: 20px;
    background-color: brown;
}
.follow-title{
    font-family: 'Times New Roman', Times, serif;
    background-color: brown;
    border-bottom: 2px solid black;
    padding-top: 5px;
    padding-bottom: 5px;
}
.follow-title h3{
    background-color: brown;
    display: inline;
    color: white;
    padding: 5px 10px;
    position: relative;/*chỉnh chữ giữa đường kẻ*/
    top: 20px;/*chỉnh chữ giữa đường kẻ*/
    left: 50px;/*chỉnh chữ giữa đường kẻ*/
}
.follow-icon{
    font-family: 'Times New Roman', Times, serif;
    background-color: brown;
    padding-bottom: 5px;
    overflow: hidden;
}
.icon{
    width: 120px;
    height: 120px;
    background-color: blueviolet;
    float: left;
    margin-right: 10px;
    text-align: center;
    margin-top: 20px;
    transition: 0.3s;
}
.icon i{
    font-size: 50px;
    color: white;
    background-color: transparent;
    display: block;
    margin-top:10px ;    
}
.chu-duoi-icon{
    background-color: transparent;
    margin-top: 10px ;
   font-size: 20px;
    color: white; 
}
.follow-icon :hover{
    background-color: black;
    margin-top: 10px;
    transition: 0.3s;
}
```
## 7. CHỒNG KHỐI <a name="bai7"></a>
```html
 <div class="khoi-tong">
    <div class="noi-dung">
        <img src="../assets/images/team-1.jpg">
        <a href="https://www.facebook.com/">Facebook</a>
    </div>
</div>
```
```css
.khoi-tong{
    width: 275px;
    height: 250px;
    padding-right: 15px;
}
.noi-dung{
    width: 260px;
    height: 195px;
    position: relative;/*làm mốc*/
}
.noi-dung img{
    width: 260px;
    height: 195px;
}
.noi-dung a{
    width: 260px;
    font-size: 20px;
    padding-left: 30px;
    display: block;
    color: white;
    text-align: center;
    background-color: #0000005e;
    text-transform: uppercase;/* viết hoa*/
    /* định vị trí theo hình*/
    position: absolute;
    bottom: 0px;
    left: 0px;
}
```