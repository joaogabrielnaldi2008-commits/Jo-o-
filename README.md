```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Empresa TechVision</title>

<!-- Ícones -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">

<style>

body{
    margin:0;
    font-family:Arial, Helvetica, sans-serif;
    background-color:#f4f4f4;
}

/* SIDEBAR */
.sidebar{
    height:100%;
    width:220px;
    position:fixed;
    background-color:#222;
    padding-top:20px;
}

.sidebar a{
    padding:15px;
    text-decoration:none;
    font-size:18px;
    color:white;
    display:block;
}

.sidebar a:hover{
    background-color:#575757;
}

/* CONTEÚDO */
.main{
    margin-left:230px;
    padding:20px;
}

/* CABEÇALHO */
header{
    background-color:#0d6efd;
    color:white;
    padding:20px;
    text-align:center;
    border-radius:10px;
}

header img{
    width:100px;
}

/* SLIDESHOW */
.slideshow-container{
    max-width:800px;
    position:relative;
    margin:auto;
    margin-top:30px;
}

.mySlides{
    display:none;
}

.mySlides img{
    width:100%;
    height:400px;
    border-radius:10px;
}

.text{
    color:white;
    font-size:20px;
    padding:10px;
    position:absolute;
    bottom:8px;
    width:100%;
    text-align:center;
    background:rgba(0,0,0,0.5);
    border-radius:0 0 10px 10px;
}

/* BOTÕES */
.prev, .next{
    cursor:pointer;
    position:absolute;
    top:50%;
    width:auto;
    padding:16px;
    margin-top:-22px;
    color:white;
    font-weight:bold;
    font-size:20px;
    transition:0.3s;
    border-radius:0 3px 3px 0;
    user-select:none;
    background-color:rgba(0,0,0,0.5);
}

.next{
    right:0;
    border-radius:3px 0 0 3px;
}

.prev:hover, .next:hover{
    background-color:black;
}

/* RODAPÉ */
footer{
    margin-top:40px;
    background-color:#222;
    color:white;
    text-align:center;
    padding:20px;
    border-radius:10px;
}

footer a{
    color:white;
    margin:10px;
    font-size:25px;
}

</style>
</head>

<body>

<!-- SIDEBAR -->
<div class="sidebar">
    <a href="#"><i class="fa fa-home"></i> Home</a>
    <a href="#"><i class="fa fa-user"></i> Sobre</a>
    <a href="#"><i class="fa fa-briefcase"></i> Serviços / Produtos</a>
    <a href="#"><i class="fa fa-envelope"></i> Contato</a>
</div>

<!-- CONTEÚDO PRINCIPAL -->
<div class="main">

    <!-- CABEÇALHO -->
    <header>
        <img src="https://cdn-icons-png.flaticon.com/512/5968/5968705.png" alt="Logo">
        <h1>TechVision</h1>
        <p>Inovação e tecnologia para o seu futuro</p>
    </header>

    <!-- SERVIÇOS / PRODUTOS -->
    <section>
        <h2 style="text-align:center; margin-top:30px;">
            Serviços e Produtos
        </h2>

        <!-- SLIDESHOW -->
        <div class="slideshow-container">

            <div class="mySlides fade">
                <img src="https://images.unsplash.com/photo-1518770660439-4636190af475" alt="Desenvolvimento Web">
                <div class="text">
                    Desenvolvimento de Sites Modernos
                </div>
            </div>

            <div class="mySlides fade">
                <img src="https://images.unsplash.com/photo-1526374965328-7f61d4dc18c5" alt="Sistemas">
                <div class="text">
                    Sistemas Empresariais Inteligentes
                </div>
            </div>

            <div class="mySlides fade">
                <img src="https://images.unsplash.com/photo-1498050108023-c5249f4df085" alt="Suporte Técnico">
                <div class="text">
                    Suporte Técnico e Consultoria
                </div>
            </div>

            <!-- BOTÕES -->
            <a class="prev" onclick="plusSlides(-1)">❮</a>
            <a class="next" onclick="plusSlides(1)">❯</a>

        </div>
    </section>

    <!-- RODAPÉ -->
    <footer>
        <p>Email: contato@techvision.com</p>
        <p>Telefone: (12) 99999-9999</p>

        <a href="https://www.facebook.com" target="_blank">
            <i class="fab fa-facebook"></i>
        </a>

        <a href="https://www.instagram.com" target="_blank">
            <i class="fab fa-instagram"></i>
        </a>

        <a href="https://www.linkedin.com" target="_blank">
            <i class="fab fa-linkedin"></i>
        </a>
    </footer>

</div>

<!-- JAVASCRIPT -->
<script>

let slideIndex = 1;
showSlides(slideIndex);

function plusSlides(n){
    showSlides(slideIndex += n);
}

function showSlides(n){
    let i;
    let slides = document.getElementsByClassName("mySlides");

    if(n > slides.length){
        slideIndex = 1;
    }

    if(n < 1){
        slideIndex = slides.length;
    }

    for(i = 0; i < slides.length; i++){
        slides[i].style.display = "none";
    }

    slides[slideIndex-1].style.display = "block";
}

/* SLIDESHOW AUTOMÁTICO */
setInterval(function(){
    plusSlides(1);
}, 3000);

</script>

</body>
</html>
```

