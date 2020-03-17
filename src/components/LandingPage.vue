<template>
    <div class="landing-page">
        <div class="welcome-board">
            <div class="brand">Retro-kolekcja</div>
            <div class="go">
                <button class="btn" @click="scrollTo('about')">
                    <img src="../../public/arrow.svg" alt="GO">
                </button>
            </div>
        </div>
        <div class="about" id="about">
            <div class="header">Czym jest Retro-kolekcja?</div>
            <p>Retro-kolekcja jest narzędziem pozwalającym na łatwe zarządzanie Twoją kolekcją sprzętu komputerowego. Możesz składać zestawy i tworzyć galerię prezentującą Twoje zbiory<span class="blink">_</span></p>

            <div class="go">
                <button class="btn" @click="scrollTo('join')">
                    <img src="../../public/arrow.svg" alt="GO">
                </button>
            </div>
        </div>
        <div class="join" id="join">
            <div class="Dołącz">Zostań retro-kolekcjonerem razem z nami!</div>
            <div class="form-wrapper">
                <label class="form-label" for="username">Nazwa użytkownika</label>
                <input type="text" name="username" id="username" class="form">

                <label class="form-label" for="email">Adres email</label>
                <input type="email" name="email" id="email" class="form">

                <label class="form-label" for="password">Hasło</label>
                <input type="password" name="password" id="password" class="form">

                <label class="form-label" for="password2">Powtórz hasło</label>
                <input type="password2" name="password2" id="password2" class="form">

                <button class="form-btn">Dołącz</button>
            </div>
        </div>
        <div class="footer">

        </div>
    </div>
</template>

<script>
    export default {
        name: "LandingPage",
        methods:{
            scrollTo: (elementID)=>{
                document.getElementById(elementID).scrollIntoView({ block: 'end',  behavior: 'smooth' })
            }
        }
    }
</script>

<style scoped>
    html{
        scroll-behavior: smooth;
    }
    .welcome-board{
        width: 100%;
        min-height: 100vh;
        background-color: #000;
        background-image: url('../../public/alex-motoc-wvOhowrohUI-unsplash.jpg');
        background-position: center;
        display: flex;
        justify-content: center;
        align-items: center;
        background-size: cover;
    }
    .about{
        min-height: calc(100vh - 10rem);
        background-color: #eee;
        padding: 5rem;
        background-image: url("../../public/about1.png");
        background-repeat: no-repeat;
        background-position: bottom right;
    }
    .join{
        min-height: 100vh;
        background-color: #000;
        background-image: url("../../public/noise.gif");
    }
    .footer {
        min-height: 30vh;
        background-color: #2c3e50;
    }
    .brand{
        color: #222;
        font-size: 3em;
        position: absolute;
        top: 20%;
        left: 50%;
        transform: translate(-50%, -50%);
        background-color: #D4D3C9;
        border-top: 2px solid #F9FBEB;
        border-left: 2px solid #F9FBEB;
        border-bottom: 2px solid #868872;
        border-right: 2px solid #868872;
        font-family: W95f;
        padding: .5rem 2rem;
    }
    .go img{
        width: 3rem;
    }
    .go{
        text-align: center;
        position: relative;
        bottom: 0px;
        display: block;
    }
    .header{
        font-size: 2em;
    }
    .about p{
        margin-top:10rem;
        width: 60vw;
    }
    .blink{
        animation: blinker 1s linear infinite;
    }
    .form{
        background-color: #000;
        border: 2px solid #fff;
        padding: .5rem;
        color: #fff;
        font-family: 'W95f';
        caret-color: transparent;
        width: 30rem;
        margin-bottom: 1rem;
        display: block;
    }
    .form-btn{
        background-color: #000;
        border: 2px solid #fff;
        padding: .5rem;
        color: #fff;
        font-family: 'W95f';
        caret-color: transparent;
        width: 31.2rem;
        margin-top: 2rem;
        display: block;
    }
    .form-label{
        display: block;
        color: #eee;
    }
    .form-label::after{
        content: ':';
    }

    @keyframes blinker {
        50% {
            opacity: 0;
        }
    }

</style>