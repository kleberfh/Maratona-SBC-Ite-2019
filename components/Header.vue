<template>
    <nav id="header" class="fixed w-full z-30 top-0 text-white border-solid border-b-2" style="background-color: #2C9473; border-color: #00E099">
        <div class="w-full mx-auto flex flex-wrap items-center justify-between mt-0 py-2">
            <div class="pl-4 flex items-center" style="font-family: 'Quicksand', sans-serif;">
                <a class="toggleColour text-white no-underline hover:no-underline font-medium text-2xl lg:text-4xl"  href="https://www.ite.edu.br/" target="_blank">
                    <img class="w-10 fill-current inline" src="imgs/logo-ite.png" /> ITE - Maratona SBC 2019
                </a>
            </div>

            <div class="block lg:hidden pr-4">
                <button id="nav-toggle" class="flex items-center px-3 py-2 border rounded text-gray-500 border-gray-600 hover:text-gray-800 hover:border-teal-500 appearance-none focus:outline-none;" >
                    <svg class="fill-current h-3 w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><title>Menu</title><path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z"/></svg>
                </button>
            </div>

            <div class="w-full flex-grow lg:flex lg:items-center lg:w-auto hidden lg:block mt-2 lg:mt-0 bg-white lg:bg-transparent text-black p-4 lg:p-0 z-20" id="nav-content"
            style="font-family: 'Quicksand', sans-serif;">
                <ul class="list-reset lg:flex justify-end flex-1 items-center">
                    <li class="mr-3 rounded-full hover:bg-green-400 hover:opacity-25">
                        <a id="menu-sobre" class="inline-block text-black font-thin no-underline hover:text-white hover:text-underline py-2 px-4" v-scroll-to="'#sobre'" href="#">Sobre</a>
                    </li>
                    <li class="mr-3 rounded-full hover:bg-green-400 hover:opacity-25">
                        <a id="menu-programacao" class="inline-block text-black font-thin no-underline hover:text-white hover:text-underline py-2 px-4" v-scroll-to="{el: '#programacao', offset: -20}" href="#">Programação</a>
                    </li>
                    <li class="mr-3 rounded-full hover:bg-green-400 hover:opacity-25">
                        <a id="menu-instituicao" class="inline-block text-black font-thin no-underline hover:text-white hover:text-underline py-2 px-4" v-scroll-to="{el: '#instituicao', offset: -40}" href="#">Instituição</a>
                    </li>
                    <li class="mr-3 rounded-full hover:bg-green-400 hover:opacity-25">
                        <a id="menu-laboratorio" class="inline-block text-black font-thin no-underline hover:text-white hover:text-underline py-2 px-4" v-scroll-to="{el: '#laboratorio', offset: -30}" href="#">Laboratório</a>
                    </li>
                    <li class="mr-3 rounded-full hover:bg-green-400 hover:opacity-25">
                        <a id="menu-contato" class="inline-block text-black font-thin no-underline hover:text-white hover:text-underline py-2 px-4" v-scroll-to="'#contato'" href="#">Contato e Patrocinadores</a>
                    </li>
                </ul>
                <button id="navAction" class="mx-auto lg:mx-0 bg-white text-gray-800 font-medium rounded-full mt-4 lg:mt-0 py-4 px-8 shadow opacity-75 focus:border-0"
                style="font-family: 'Nunito', sans-serif">2019</button>
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
    .active {
        border-radius: 9999px;
        background-color: #68d391;
        color: #fff;
    }
</style>
