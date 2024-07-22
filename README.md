# Project-1 - ProGamers

Font Awasome 
===
    <!-- Font Awasome -->
    <script src="https://kit.fontawesome.com/1d23864fb5.js" crossorigin="anonymous"></script>

Google Fonts 
===
   <!-- Google - Font -->
    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link href="https://fonts.googleapis.com/css2?family=Montserrat&display=swap" rel="stylesheet">
===
Slicky
+		https://kenwheeler.github.io/slick/
CSS ⬆️ 
+		<link rel="stylesheet" type="text/css" href="//cdn.jsdelivr.net/npm/slick-carousel@1.8.1/slick/slick.css"/>
Bootstap (v5.3)
⬆️
+   <!--Bootstrap CSS  --> 
 		   <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet"
                    integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
⬇️
+       <!-- Bootstrap JS --> 
 		   <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"
                   integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz"
                   crossorigin="anonymous"></script> 
---
jQuery ⬇️⬇️ nad JS
+		<script type="text/javascript" src="//code.jquery.com/jquery-1.11.0.min.js"></script>
+		<script type="text/javascript" src="//code.jquery.com/jquery-migrate-1.2.1.min.js"></script>
JS ⬇️ 
+		<script type="text/javascript" src="//cdn.jsdelivr.net/npm/slick-carousel@1.8.1/slick/slick.min.js"></script>

---
Navbar
+  https://getbootstrap.com/docs/5.3/components/navbar/
+     position-sticky top-0
+     navbar-nav ms-auto
-     fluid
-     bg-body-tertiary
-                    <li class="nav-item">
                        <a class="nav-link disabled" aria-disabled="true">Disabled</a>
                    </li>
---
Captions
+ https://getbootstrap.com/docs/5.3/components/carousel/#captions/
---
Card groups
+ https://getbootstrap.com/docs/5.3/components/card/
---
Scrollspy
+ https://getbootstrap.com/docs/5.3/components/scrollspy/

⚠️ w Bootstrapie każdy paragraf ma ustawiony automatycznie margines od dołu i trzeba go ręcznie zmieniać ⚠️  🔷 mb-1 🔷
---
Animista
+ 	https://animista.net/
+ 	https://animista.net/play/attention/bounce
---

AOS - Animate on scroll library
+ 		https://michalsnik.github.io/aos/
+ ❗❗❗❗ .aboutus-hover {transition: color 0.3s;} blokuje animację w AOS i trzeba go usunąć albo zakomentować❗❗❗❗
+ ✅✅✅✅ rozwiązanie problemu ✅✅✅✅
+ 		<div data-aos="zoom-in" data-aos-delay="100"> nadany na rodzica +
CSS ⬆️
+ 		<link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
JS ⬇️
+		<script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
HTML 🔶
+		    <script>
		        AOS.init({
		        startEvent: 'DOMContentLoaded',
		        offset:200,
		        once: true,
		    });
		    </script>
===
HTML (index.html)
---
https://fontawesome.com/icons/bars?f=classic&s=solid
-     <span class="navbar-toggler-icon"></span>
+     <i class="fa-solid fa-bars"></i>
+     <i class="fa-solid fa-headset"></i>
-     Navbar - zaminana nazwy na ikonę i dodaję nazwę PROGAMERS

+  dodanie dodatkowych nav-link (o nas; portfolio; cena; zespół; osiągnięcia; kontakt)

---

===
CSS(Scss) (main.scss)(_colors.scss)
---
+                     nav {
                            text-transform : uppercase;
                       .nav-link, .navbar-nav .nav-link.active, .navbar-nav .show>.nav-link, .navbar-brand, .fa-bars {
                            color: #fff;
                    
+                        .nav-link:focus, .nav-link:hover, .navbar-nav .nav-link.active, .navbar-nav .show>.nav-link {
                         color: #039dff;
                         z-index:5;       #Zapobiega przykrywaniu nawigacji
                        }
                    }
_colors.scss
+         $main-color: #039dff;
          $white-color: #fff;
          $light-grey;

main.scss
---
+      @use './colors' as *;
         color: $white-color;
          color: $main-color;
---
HEADER
---
+    header.hero-img {
+       position:relative;
        height:100vh;
        backgroung-image: url("../img/hero-small.jpeg");
        background-size: cover;
         background-position: center;

 ❗❗ Problemy ze wsparciem np: Safarii ❗❗
+        background-attachment: fixed;
  
+         color: $white;
        z-index: 0;    #CIEŃ(1)
         h1 {
             text-transform: uppercase;
         }
      }

+    .hero-shadow {
+       position: absolute;
       top: 0;
       left: 0;
       width: 100%;
       height: 100%;
        background-color: rgb(0,0,0,.8);
        z-index: -5;   #CIEŃ(1)
        }
WYŚRODKOWANIE TEKSTU NA STRONIE (domyślnie jest flex-direction row ⚠️)
+    .hero-text {
+       display: flex;
        justyfy-content: center;
        align-items: center;
        flex-direction: column    #Trzeba dodać by wyśrodkować tekst
         height: 100%;
       }
ZAMIANA KOLORU GAMERS
+        .blue-text {
        color: $main.color;
       }

===
JS (script.js)
---
+     dodaje do index.html 🔶 <script src="./js/script.js"></script> 🔶
+     Zamiast 'click' daję DOMContentLoader'    🔶 document.addEventListener('DOMContentLoaded', function () {🔶
+    	  trzyma moją nawigację        🔶    const nav = document.querySelector('.navbar') 🔶
scss
+     dodaję .shadow-bg {
    	background-color: rgba(0,0,0,.9);
        }
===
MOBILE - CORECT 📱 = iPhone 5/SE ✅ Samsung Galaxy S8+✅ iPadPro✅ Samsung Galaxy S20 Ultra✅
===
HTML
....
+      dodaję text-center    <div class="hero-text text-center">  🔶 Lub w SCSS dodaje text-align: center   wyjdzie na to samo 🔶 
+     dodaję padding 2 kategorii  🔶  <div class="hero-text text-center p-2">
SCSS
....
+     @media (min-width: 768px) {
	    .hero-text {
		    h1 {
			    font-size: 42px;
		    }
		
		p{
			font-size: 20px;
		}
MAIN index.html
....
+     id = lepiej jest używać w JS lub do kotwiczenia elementów na stronie niż stylowaniu CSS 🔴 id zjada pamięć 🔴

+     Dodajemy class i podpinamy z id na 🔶  <section id="aboutus" class="aboutus bg-light py-5 ">
+     pozycjonowanie kontenera na stronie   🔶   <div class="container">
+      <h2 class="section-title">o nas</h2>
+      <div class="underline"></div>
+         🔵 <div class="row"> 🔵
+            🔵 <div class="col-sm-6 col-md-4 text-center"> 🔵
  ⚪ ikony z Font Awesome ⚪
+        <p><i class="fa-solid fa-mobile-screen"></i></p>
+        <p><i class="fas fa-desktop"></i></p>
+        <p><i class="fas fa-file-code"></i></p>
+        <p><i class="fas fa-paw"></i></p>
+         <p><i class="fas fa-hamburger"></i></p>
+          <p><i class="fas fa-glass-cheers"></i></p>
+         <i class="fa-solid fa-bars"></i>
+          <i class="fa-solid fa-headset"></i>
+ 		<i class="fa-brands fa-steam"></i>
+  		<i class="fa-brands fa-playstation"></i>
+  		<i class="fa-brands fa-xbox"></i>
+  		<i class="fas fa-mobile-alt"></i>
+  		<i class="fas fa-desktop"></i>
+	      <i class="fas fa-gamepad"></i>
+	  <i class="fab fa-facebook-f"></i>
+	  <i class="fab fa-twitter"></i>
+	  <i class="fab fa-linkedin-in">
+	   <i class="fas fa-thumbs-up"></i>
+	    <i class="fas fa-trophy"></i>
+		<i class="fas fa-user-friends"></i>
+		<i class="far fa-building"></i>
+		<i class="fas fa-dice"></i>
+		<i class="fas fa-share-alt"></i>
Scss
+    POWIĘKSZENIE TEKSTU I WYŚRODKOWANIE
+        .section-title {
	    text-align: center;
    	text-transform: uppercase;
        }
+    KRESKA POD NAPISEM
+        .underline {
+     	W elemencie blokowym  🔶 margin: 0 auto 40px;🔶
	    width: 60px;
	    height: 4px;
	    background-color: $main-color;
        }
+		.aboutus {
		i {
		margin-top: 20px;
		font-size: 30px;
		}

+		.aboutus-card-title {
			font-size: 18px;
			text-transform: uppercase;
		}

+		.aboutus-card-text {
			font-size: 14px;
		}
		}
ABOUT - PODŚWIETLENIE IKON NA BŁĘKITNY 🔵 :hover 🔵
+		 <div class="col-sm-6 col-md-4 text-center 🔹 aboutus-hover🔹">
		 
+		.aboutus-hover{
			transition: color .3s;
			}
+		 .aboutus-hover:hover {
		color: $main-color;
		
			}
PRZYDATNA WŁĄŚCIWOŚĆ DO SCROLOWANIA NA TELEFONY ✳️

+ SCSS
+	dodajemy
+		html {
		scroll-padding-top: 74px ;
		}
⚠️ F12 - po najechaniu na pasek nawigacji widzę jakie parametry i jaki styl ma pasek w tym wypadku 74px ⚠️

PRZYDATNA WŁĄŚCIWOŚĆ DO SCROLOWANIA NA PC ✳️
+		 @media (min-width: 992px){
			html {
			scroll-padding-top: 72px ;
			}
		}
ZAMYKANIE NAWIGACJI PO NACIŚNIĘCIU WYBORU LUB INNEGO MIEJSCA NA TELEGONIE ✴️ JS ✴️
AUTOMATYCZNE ZAMYKANIE...
+ Badam nawigację w F12
+ 		dodaję do js. wszystkie linki ✴️	const allNavItems = document.querySelectorAll('.nav-link')
+ 		trzeba dodać by show się aktywowało ✴️ const navList = document.querySelector('.navbar-collapsa')
+ 		dodaję nasłuchiwanie na clicka w pętli na wszystkie linki ✴️
+ 		allNavItems.forEach(item => item.addEventListener('click', () => {navList.classList.remove('show')	
		}))
❇️ SEKCJA - TWORZYMY GRY NA PLATFORMY ❇️ HTML
+ 		 <section class="aboutus-hero py-5">
         	   <div class="aboutus-shadow"></div>

          	  <div class="cointener"></div>
          	      <h2  class="section-title">tworzymy gry na platformy</h2>
	                <div class="underline"></div>
     		   </section>
❇️ SEKCJA - TWORZYMY GRY NA PLATFORMY ❇️ SCSS 
+		.aboutus-hero {
		position: relative;
		background-image: url(../img/pc-small.jpg);
		background-size: cover;
		background-position: center;
		color: $light-grey;
		z-index: 0;
+		.aboutus-shadow {
  		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background-color: rgba(0, 0, 0, 0.7);
		z-index: -5;
		}
             }
ZMIANA POZYCJONOWANIA FLEX NA ❇️ SEKCJI - TWORZYMY GRY NA PLATFORMY ❇️
+		col-sm-6 col-md-4
  ZAMIENIAM NA
+		col-lg-4
+	  <div class="col-lg-4 text-center aboutus-hero-item">
+	  <p class="aboutus-hero-title mb-1">
SCSS
+ 		.aboutus-hero-item {
			margin: 10px 0;

+		i{
+		
			font-size: 36px;
		}
+		.aboutus-hero-title {
			font-size: -24px;
			}
		}

+ 		.aboutus-hero {
		background-image: url('../img/pc-big.jpg');
	}
⬜ PORTFOLIO ⬜
+ 		.portfolio {
			.carousel-item {
				height: 600px;
			}
+		.carousel-indicators {
			padding-bottom: 20px;
			}
 💲 CENA  💲
+		 <section id="prices" class="prices py-5 bg-light">
          		  <h2 class="section-title">ceny</h2>
          		  <div class="underline"></div>

 +           <div class="container">
                <div class="price-wrap row text-center justify-content-center">
                    <div class="col-md-4 col-xl-4">
                        <div class="price-box">

scss - PRICE BOX 💟💟💟
+ 		.prices {
			.price-box {
				margin: 20px;
  				padding: 30px;
				background-color:$white;
				box-shadow: 5px 5px 5px rgb(0, 0, 0, 0.4);
  				transition: scale .3s;
				span {
				font-weight: bold;
					}
			}
+			i {
			padding: 0 5px;
			font-size: 24px;
			}
+			button {
				padding: 10px 20px;
				text-transform: uppercase;
			}
+		.price-box:hover {
		transform scale();    ⚠️ lub nowszy zapis ⚠️ scale: 1.5;
		}

+			.price-title {
				color: $main-color;
				text-transform: uppercase;
				font-weight: bold;
				font-size: 20px;
+		.price-tag {
			font-weight: bold;
			font-size: 30px;
		}
+		.price-info {
		margin-top: 30px;

		a{
			text-decoration: none;
		}
			}
Sekcja Zespół
Card groups (niższy) ⚠️ 
+		https://getbootstrap.com/docs/5.3/components/card/
+    	<div class="card-footer d-flex justify-content-around">

+ 		.team-shadow {
			position: absolute;
			top: 0;
			left: 0;
			width: 100%;
			height: 100%;
			background-color: rgba(0, 0, 0, 0.7);
			z-index: -5;
			}

+		.card {
			transition: scale 0.3s;
			img {
				height: 300px;
				object-fit: cover;
			}

			i {
				padding: 10px;
			}

+			.card-body {
				height: 160px;
			}
		}

+		.card:hover {
			scale: 0.96;
		}


+		.card-title {
			margin-bottom: 20px;
			text-align: center;
			text-transform: uppercase;
		}

Sticky index.html ✴️
+ <!-- team -->
            <div class="container">
                <div class="card-group team-carousel">
Sticky scss ✴️
+		 .card-body {
		height: 160px;
		}
Slick.js ✴️
+		$('.team-carousel').slick({
+			arrows: false,
+			autoplay: true,
			mobileFirst: true,
 			slidesToShow: 1,
  			slidesToScroll: 1,
 			responsive: [

				{
 			breakpoint: 768,
 			settingd: {slideToShow: 2,}
 			 },
		        {
		            breakpoint: 992,
		            settings: {slidesToShow: 3,}
		        }
		
 		    ] 			
  		})  ;
 🗽 OSIĄGNIĘCIA 🗽 
 HTML dodaję
 +         <section class="achievements py-5" id="achievements">
            <h2 class="section-title">osiągnięcia</h2>
            <div class="underline"></div>

            <div class="container">
+                <div class="row text-center achievements-list">
                    <div class="col-md-6 col-lg-4 col-xl-2">
                        <i class="fas fa-thumbs-up"></i>
                        <p class="achievement-number">100%</p>
                        <p class="achievement-text">XYZ/p>
SCSS
+		.achievements-list {
			padding: 20px 0;
		}
+		.achievements-list i {
			padding: 10px;
			font-size: 48px;
			color: #fff;
			text-shadow: 0 0 5px rgb(0, 0, 0, 0.8);
		}
+		.achievements-list .achievement-number {
			font-size: 22px;
		}
+		.achievements-list .achievement-text {
			font-size: 13px;
			text-transform: uppercase;
		}
👬👬 KONTAKT 👬👬
html🔆
+     <section id="contact" class="contact py-5">

            <h2 class="section-title">kontakt</h2>
            <div class="underline"></div>

            <div class="container">

                <div class="row text-center contact-us">
+                    <div class="col-sm-6 col-lg-4 contact-item order-1">
css🔆
+		 .contact {
			position: relative;
			background-image: url('../img/contact-bg.jpeg');
			background-position: bottom;
			background-attachment: fixed;
			background-size: cover;
			z-index: 0;

+		.section-title {
			color: $light-gray;
		}

+		.underline {
		background-color: $light-gray;
		}

+		.contact-shadow {
			position: absolute;
			top: 0;
			left: 0;
			width: 100%;
			height: 100%;
			background-color: rgb(0, 9, 27, 0.85);
			z-index: -5;
		}

+		.contact-us {
			display: flex;
			align-items: center;
			color: $white;
		
+		.contact-item {
			margin: 30px 0;		
			
			h3 {
				margin-bottom: 15px;
				text-transform: uppercase;
				letter-spacing: 2px;
			}
		}

+		.social-media {
			font-size: 26px;

			a {
				padding: 10px;
				color: $white;
				transition: color .3s;
			}

			a:hover{
				color: $main-color;
			}
FOOTER 🔲 ©️ ®️ ™️ 
+     <footer class="bg-dark text-light py-4 text-center">
        <p class="mb-0">&copy;2024 | ProGamers</p>
        <div class="container"></div>
      </footer>
🎠🎠🎠 ANIMATIONS 🎠🎠🎠

_animations.scss
+		.bounce-top {
		    display:block;
			animation: bounce-top 2s infinite both;
		}
		
		@keyframes bounce-top {
		    0% {
		      transform: translate(-50%,-45px);
		      animation-timing-function: ease-in;
		      opacity: 1;
		    }
		    24% {
		        opacity: 1;
		    }
		    40% {
		        transform: translate(-50%,-24px);
		      animation-timing-function: ease-in;
		    }
		    65% {
		      transform: translate(-50%,-12px);
		      animation-timing-function: ease-in;
		    }
		    25%,
		    55%,
		    75%,
		    87% {
		      transform: translate(-50%,0px);
		      animation-timing-function: ease-out;
		    }
		    100% {
		      transform: translate(-50%,0px);
		      animation-timing-function: ease-out;
		      opacity: 1;
		    }
		  }
AOS

+            <h1 data-aos="fade-up "data-aos-delay="200">witajcie w pro<span class="blue-text">gamers</span></h1>
+            <p data-aos="fade-up  "data-aos-delay="400"></p>>W miejscu, gdzie gry tworzymy z pasją</p>
+            <a data-aos="fade-up  "data-aos-delay="600"></a>href="#aboutus" class="btn btn-outline-light mt-2 text-uppercase">poznaj nas</a>
Bootstrap - Scrollspy
HTML
+ 		<body data-bs-spy="scroll" data-bs-target="#navId">
   		 <nav class="navbar navbar-expand-lg position-fixed top-0 w-100 py-3" id="navId">
