<template>
    <nav id="header" class="menu-header">
        <div class="menu-content">
            <div class="menu-logo">
                <a class="menu-text"  href="https://www.ite.edu.br/" target="_blank">
                    <img class="menu-img" src="imgs/logo-ite.png" /> ITE - Maratona SBC 2019
                </a>
            </div>

            <div class="menu-items" id="nav-content">
                <ul class="menu-sub-items">
                    <li class="menu-item">
                        <a id="menu-sobre" class="menu-item-link" v-scroll-to="'#sobre'" href="#">Sobre</a>
                    </li>
                    <li class="menu-item">
                        <a id="menu-programacao" class="menu-item-link" v-scroll-to="{el: '#programacao', offset: -20}" href="#">Programação</a>
                    </li>
                    <li class="menu-item">
                        <a id="menu-instituicao" class="menu-item-link" v-scroll-to="{el: '#instituicao', offset: -40}" href="#">Instituição</a>
                    </li>
                    <li class="menu-item">
                        <a id="menu-laboratorio" class="menu-item-link" v-scroll-to="{el: '#laboratorio', offset: -30}" href="#">Laboratório</a>
                    </li>
                    <li class="menu-item">
                        <a id="menu-contato" class="menu-item-link" v-scroll-to="'#contato'" href="#">Contato e Patrocinadores</a>
                    </li>
                    <li class="menu-item menu-item-active">
                        <a id="others_years" class="menu-item-link" href="#">2019</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</template>

<script>
    import VueScrollTo from 'vue-scrollto';

    export default {
        name: "Header",
        components: {
            VueScrollTo
        },
    }
</script>

<style>

    /* - MENU STYLE - */
    .menu-header {
        font-family: Quicksand, sans-serif;
        background-color: #2C9473;
        border-color: #00E099;
        width: 100%;
        color: white;
        border-bottom-width: 2px;
        position: fixed;
        z-index: 50;
    }

    .menu-content {
        padding-top: 0.5rem;
        padding-bottom: 0.5rem;
    }

    .menu-logo {
        padding-left: 1rem;
        align-items: center;
    }

    .menu-text {
        text-decoration: none;
        color: white;
        font-weight: 500;
    }

    .menu-img {
        width: 2.5rem;
        display: inline;
    }

    .menu-items {
        display: flex;
        flex-grow: 1;
        width: auto;
        padding: 0;
        margin-top: 0;
        background-color: transparent;
        color: black;
    }

    .menu-sub-items {
        display: flex;
        flex: 1 1 0%;
        justify-content: flex-end;
        align-items: center;
        list-style: none;
    }

    .menu-item {
        margin-right: 0.75rem;
        border-radius: 999px;
    }

    .menu-item:hover {
        background-color: #68d391;
        color: white !important;
        text-decoration: none !important;
    }

    .menu-item-link {
        padding: 0.5rem 1rem;
        font-weight: 200;
        display: inline-block;
        text-decoration: inherit;
    }

    .menu-item-active {
        border-radius: 999px;
        background-color: #68d391;
        color: white;
    }


    /*DESKTOP*/
    @media only screen and (min-width: 961px) {
        .menu-content {
            display: flex;
        }
        .menu-text {
            font-size: 2.25rem;
        }
    }

    /*MOBILE*/
    @media only screen and (max-width: 960px) {
        .menu-content {
            display: grid;
        }
        .menu-logo {
            padding-top: 0.5rem;
        }
        .menu-text {
            font-size: 1.6rem;
        }
        .menu-img {
            width: 2rem;
        }
        .menu-items {
            overflow-x: auto;
        }
        .menu-sub-items {
            margin-left: 1rem;
            margin-right: 1rem;
        }
        .menu-item {
            text-align: center;
        }
    }
</style>
