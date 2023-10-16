# Lab4Web

## WEB LAYOUT

- Web layout merupakan kerangka yang mengatur penempatan tata letak sebuah elemen pada halaman web. Tata letak element seperti navigasi, header, tombol CTA (Call to Action), dan elemen lainnya pada halaman web, sehingga tampilan web dapat disesuaikan dengan desain yang ada. Dengan layout website yang tepat, informasi akan tampil dengan lebih menawan dan fungsional Halaman web sering kali dibagi menjadi header, menu, konten, dan footer: Ada banyak sekali desain tata letak yang dapat dipilih.<br>

## BOX ELEMENT

- Element HTML dapat dianggap sebagai sebuah Box atau kotak. Box tersebut digunakan untuk membuat layout web. Pada dasarnya semua element HTML adalah box dengan beberapa perbedaan. Ada yang floating ada juga yang tanpa floating. Tag yang biasanya digunakan dalam merancang layout web adalah tag div dengan konsep box element. Konsep box element terdiri dari Margin, Border, Padding, dan Content. <br>

## CSS FLOAT PROPERTY

- CSS Float Property memungkinkan elemen HTML dibuat seolah-olah mengambang diantara
elemen yang lainnya. Dengan konsep tersebut dapat dengan mudah menentukan posisi atau letak sebuah elemen HTML. Sehingga dalam membuat layout web dapat dengan mudah dilakukan. Property yang digunakan untuk mendefinisikan adalah float dan clear.<br>

## LANGKAH-LANGKAH PRAKTIKUM

### BOX
1. Membuat dokumen HTML dan tambahkan kode untuk membuat box element. Setelah itu tambahkan deklarasi CSS pada **HEAD** untuk membuat float element.

    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Box Element</title>
        <style>
            div {
                float:left;
                padding: 10px;  
            }
            .div1 {
                background: red;
            }
            .div2 {
                background: yellow;
            }
            .div3 {
                background: green;
            }
        </style>
    </head>
    <body>
    <header>
        <h1>Box Element</h1>
        <section>
            <div class="div1">Div 1</div>
            <div class="div2">Div 2</div>
            <div class="div3">Div 3</div>
        </section>
    </header>
    </body>
    </html>
    ```

    ![img](gambar/1.png)<br>

2. Mengatur Clearfix Element untuk mengatur element setelah float element. Lalu tambahkan element lainnya seperti div3 kemudian atur property clear pada CSS.

    ```html
    <section>
        <div class="div1">Div 1</div>
        <div class="div2">Div 2</div>
        <div class="div3">Div 3</div>
        <div class="div4">Div 4</div>
    </section>
    ```
    <br>

    ```css
    .div4 {
        background-color: blue;
        clear: left;
        float: none;
    }
    ```

    ![img](gambar/2.png)<br>

### MEMBUAT LAYOUT SEDERHANA
1. Buat file baru dengan file css kemudian buat kerangka layout dengan semantics element.

    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Layout Sederhana</title>
        <link rel="stylesheet" href="css/style.css">
    </head>
    <body>
        <div id="container">
            <header>
                <h1>Layout Sederhana</h1>
            </header>
            <nav>
                <a href="home.html" class="active">Home</a>
                <a href="artikel.html">Artikel</a>
                <a href="about.html">About</a>
                <a href="kontak.html">Kontak</a>
            </nav>
            <section id="hero"></section>
            <section id="wrapper">
                <section id="main"></section>
                <aside id="sidebar"></aside>
            </section>
            <footer>
                <p>&copy; 2021 - Universitas Pelita Bangsa</p>
            </footer>
        </div>
    </body>
    </html>
    ```

    ![img](gambar/3.png)<br>

2. Kemudian tambahkan kode CSS untuk membuat layoutnya.

    ```css
    /* import google font */
    @import
    url('https://fonts.googleapis.com/css2family=Open+Sans:ital,wght@0,300;0,400;0,600;0,700;0,800;1,300;1,400;1,600;1,700;1,800&display=swap');
    @import
    url('https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:ital,wght@0,300;0,700;1,300&display=swap');
    /* Reset CSS */
    * {
    margin: 0;
    padding: 0;
    }
    body {
    line-height:1;
    font-size:100%;
    font-family:'Open Sans', sans-serif;
    color:#5a5a5a;
    }
    #container {
    width: 980px;
    margin: 0 auto;
    box-shadow: 0 0 1em #cccccc;
    }
    /* header */
    header {
    padding: 20px;
    }
    header h1 {
    margin: 20px 10px;
    color: #b5b5b5;
    }
    ```

    ![img](gambar/4.png)<br>

3. Kemudian selanjutnya mengatur Navigasi

    ```css
    /* navigasi */
    nav {
    display: block;
    background-color: #1f5faa;
    }
    nav a {
    padding: 15px 30px;
    display: inline-block;
    color: #ffffff;
    font-size: 14px;
    text-decoration: none;
    font-weight: bold;
    }
    nav a.active,
    nav a:hover {
    background-color: #2b83ea;
    }
    ```

    ![img](gambar/5.png)<br>

4. Selanjutnya membuat hero panel. Tambahkan di HTML dan CSS

    ```html
    <section id="hero">
    <h1>Hello World!</h1>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
    elit, iaculis innisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
    vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
    pretium ac.</p>
    <a href="home.html" class="btn btn-large">Learn more &raquo;</a>
    </section>
    ```
    <br>

    ```css
    /* Hero Panel */
    #hero {
    background-color: #e4e4e5;
    padding: 50px 20px;
    margin-bottom: 20px;
    }
    #hero h1 {
    margin-bottom: 20px;
    font-size: 35px;
    }
    #hero p {
    margin-bottom: 20px;
    font-size: 18px;
    line-height: 25px;
    }
    ```

    ![img](gambar/6.png)<br>

5. Selanjutnya mengatur main content dan sidebar, lalu tambahkan CSS float dan element lain dalam sidebar

    ```css
    /* main content */
    #wrapper {
    margin: 0;
    }
    #main {
    float: left;
    width: 640px;
    padding: 20px;
    }
    /* sidebar area */
    #sidebar {
    float: left;
    width: 260px;
    padding: 20px;
    }
    /* widget */
    .widget-box {
    border:1px solid #eee;
    margin-bottom:20px;
    }
    .widget-box .title {
    padding:10px 16px;
    background-color:#428bca;
    color:#fff;
    }
    .widget-box ul {
    list-style-type:none;
    }
    .widget-box li {
    border-bottom:1px solid #eee;
    }
    .widget-box li a {
    padding:10px 16px;
    color:#333;
    display:block;
    text-decoration:none;
    }
    .widget-box li:hover a {
    background-color:#eee;
    }
    .widget-box p {
    padding:15px;
    line-height:25px;
    }
    ```

    <br>

    ```html
    <aside id="sidebar">
        <div class="widget-box">
            <h3 class="title">Widget Header</h3>
            <ul>
                <li><a href="#">Widget Link</a></li>
                <li><a href="#">Widget Link</a></li>
                <li><a href="#">Widget Link</a></li>
                <li><a href="#">Widget Link</a></li>
                <li><a href="#">Widget Link</a></li>
            </ul>
        </div>
        <div class="widget-box">
            <h3 class="title">Widget Text</h3>
            <p>Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt
            arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer
            pharetra est nunc, nec pretium nunc pretium ac.</p>
        </div>
    </aside>
    ```

    ![img](gambar/7.png)<br>

6. Selanjutnya mengatur Footer. Tambahkan di CSS untuk Footer

    ```css
    /* footer */
    footer {
    clear:both;
    background-color:#1d1d1d;
    padding:20px;
    color:#eee;
    }
    ```

    ![img](gambar/8.png)<br>

7. Setelah itu tambahkan Element lainnya pada Main Content

    ```html
    <section id="main">
        <div class="row">
            <div class="box">
                <img src="https://dummyimage.com/120/db7d25/fff.png" alt="" class="image-circle">
                <h3>Heading</h3>
                <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
                <a href="#" class="btn btn-default">View detail</a>
            </div>
            <div class="box">
                <img src="https://dummyimage.com/120/3e73e6/fff.png" alt=""
                class="image-circle">
                <h3>Heading</h3>
                <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis
                euismod.</p>
                <a href="#" class="btn btn-default">View detail</a>
            </div>
            <div class="box">
                <img src="https://dummyimage.com/120/71e6d4/fff.png" alt=""
                class="image-circle">
                <h3>Heading</h3>
                <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis
                euismod.</p>
                <a href="#" class="btn btn-default">View detail</a>
            </div>
        </div>
    </section>
    ```
    <br>

    ```css
    /* box */
    .box {
    display:block;
    float:left;
    width:33.333333%;
    box-sizing:border-box;
    -moz-box-sizing:border-box;
    -webkit-box-sizing:border-box;
    padding:0 10px;
    text-align:center;
    }
    .box h3 {
    margin: 15px 0;
    }
    .box p {
    line-height: 20px;
    font-size: 14px;
    margin-bottom: 15px;
    }
    box img {
    border: 0;
    vertical-align: middle;
    }
    .image-circle {
    border-radius: 50%;
    }
    .row {
    margin: 0 -10px;
    box-sizing: border-box;
    -moz-box-sizing: border-box;
    -webkit-box-sizing: border-box;
    }
    .row:after, .row:before,
    .entry:after, .entry:before {
    content:'';
    display:table;
    }
    .row:after,
    .entry:after {
    clear:both;
    }
    ```

    ![img](gambar/9.png)<br>

8. Terakhir membuat Content Artikel. Tambahkan di HTML dan CSS

    ```html
    <hr class="divider" />
    <article class="entry">
        <h2>First featurette heading.</h2>
        <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc pretium ac.</p>
    </article>
        <hr class="divider" />
        <article class="entry">
        <h2>First featurette heading.</h2>
        <img src="https://dummyimage.com/150/7b8a70/fff.png" alt=""
        class="right-img">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
        elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
        vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
        pretium ac.</p>
    </article>
    ```

    <br>

    ```css
    .divider {
    border:0;
    border-top:1px solid #eeeeee;
    margin:40px 0;
    }
    /* entry */
    .entry {
    margin: 15px 0;
    }
    .entry h2 {
    margin-bottom: 20px;
    }
    .entry p {
    line-height: 25px;
    }
    .entry img {
    float: left;
    border-radius: 5px;
    margin-right: 15px;
    }
    .entry .right-img {
    float: right;
    }
    ```

    ![img](gambar/10.png)<br>

### PERTANYAAN & TUGAS

1. Tambahkan Layout untuk menu About
=> buat single layout yang berisi deskripsi, portfolio, dll<br>
 - **HASIL**
    ![img](gambar/11.png)
    <br>
    <br>
2. Tambahkan layout untuk menu Contact
=> yang berisi form isian: nama, email, message, dll<br>
- **HASIL**
    ![img](gambar/12.png)
    <br>
    <br>