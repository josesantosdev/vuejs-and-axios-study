<template>
    <header>
        <nav class="container">
            <a href="/"><img src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/wdev.svg
" alt="DEV" id='logo'></a>

            <img src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/menu.svg
" alt="Abrir menu" id="menu-button" v-on:click="openMenu">


<div id="menu-overlay" v-if="menuActive" v-on:click="closeMenu" >

</div>

<div id="menu-itens" :class="{active:menuActive}">
    <a href="/"><img src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/wdev.svg
" alt="DEV" id='menu-logo'></a>
    <ul>
        <li><a href="/">Home</a></li>
        <li><a href="/videos">Vídeos</a></li>
        <li><a href="/sobre">Sobre</a></li>
        <li><a href="/contato">Contato</a></li>
    </ul>
</div>
        </nav>
    </header>
</template>

<script>
export default{
    name: 'Header',
    data(){
        return{
            menuActive: false
        }
    },
    methods:{
        openMenu: function(){
            this.menuActive = true
        },
        closeMenu: function(){
            this.menuActive = false
        }
    }
}
</script>

<style scoped>
   nav{
       display: flex;
       justify-content: space-between;
       height: 60px;
       align-items: center;
   }
   header{
        background-color: var(--color-background-nav);
        height: 60px;
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    #logo{
        width: 130px;
    }

    #menu-button{
        width: 30px;
    }

    #menu-overlay{
        position: fixed;
        top: 0;
        left: 0;
        width: 40%;
        height: 100vh;
        background-color: black;
        opacity: 0.8;
    }

    #menu-logo{
        width: 110px;
        margin-top: 30px;
        margin-bottom: 10px;
    }

    #menu-itens{
        position: fixed;
        top:0;
        right:0;
        background-color: var(--color-background-nav);
        width: 60%;
        height: 100vh;
        display:none;
        flex-direction: column;
        justify-content: flex-start;
        align-items: center;

    }
    #menu-itens.active{
        display: flex;
    }

    ul{
        list-style: none;
        text-align: center;
        height: 60px;
        align-items: center;
    }

    ul li a{
        color:var(--color-text-light);
    }

    ul li{
        margin: 20px 0px;
    }

    @media (min-width: 700px){
        #menu-button,
        #menu-logo,
        #menu-overlay{
            display: none;
        }

        #menu-itens{
            display:flex;
            position: static;
            height: 60px;
            width: auto;
        
        }

        ul{
            display: flex;
        }

        ul li{
            margin: 0;
            margin-left: 20px;
        }

    }
</style>
