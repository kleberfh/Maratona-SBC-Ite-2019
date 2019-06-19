<template>
    <div style="min-width: 100vw;">
        <div class="mx-auto flex flex-wrap flex-col md:flex-row">
            <section id="sobre" class="w-full h-screen bg-fixed bg-center bg-cover overflow-auto" style="background-image: url('imgs/maratona2018-1.jpeg'); min-width: 100vw">
                <div class="container">
                    <div class="flex mb-4">
                        <div class="bg-white" style="border-radius: 14px; height: 60vh; width: 80vw; box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2), 0 6px 20px 0 rgba(0,0,0,0.19);height:100%">
                            <p class="font-bold section1-text section1-title mt-2" style="font-size: 4vh; margin-top: 4vh">Maratona SBC de Programação 2019</p>
                            <p class="section1-text section1-text-content text-base" style="font-size: 2.2vh; margin-top: 4vh">
                                A Maratona de Programação é um evento da Sociedade Brasileira de Computação que existe desde o ano de 1996.
                                A Maratona nasceu das competições regionais classificatórias para as finais mundiais do concurso de programação, o International Collegiate Programming Contest, e é parte da regional sulamericana do concurso. Neste ano ocorre a 24a. edição da Maratona.
                                Ela se destina a alunos e alunas de cursos de graduação e início de pós-graduação na área de Computação e afins (Ciência da Computação, Engenharia de Computação, Sistemas de Informação, Matemática, etc).
                                A competição promove nos estudantes a criatividade, a capacidade de trabalho em equipe, a busca de novas soluções de software e a habilidade de resolver problemas sob pressão.
                                De ano para ano temos observado que as instituições e principalmente as grandes empresas da área têm valorizado os alunos que participam da Maratona.
                            </p>
                            <p class="section1-complement" style="font-size: 2vh"> Conheça mais sobre a Maratona SBC de Programação no site oficial: </p> <a class="section1-link" style="color: #2C9473" href="http://maratona.ime.usp.br/sobre19.html" target="_blank">http://maratona.ime.usp.br</a>
                        </div>
                    </div>
                </div>
            </section>
            <section id="programacao" class="w-full h-screen" style="background-color: #00E099">
                <div class="container">
                    <div class="flex flex-col">
                        <div class="w-full mb-10">
                            <p class="text-4xl font-bold section1-text section1-title">Veja a programação do dia:</p>
                        </div>
                        <div class="w-full" >
                            <VueCal class="bg-gray-100 border-solid border-2" style="height: 80vh; width: 90vw; border-radius: 8px; margin-left: auto; margin-right: auto; box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2), 0 6px 20px 0 rgba(0,0,0,0.19);"
                                    locale="pt-br"
                                    selectedDate="2019-06-14"
                                    time
                                    :timeFrom="9 * 60"
                                    :timeTo="20.5 * 60"
                                    :timeStep="30"
                                    default-view="day"
                                    :disableViews="['years', 'year', 'month', 'week']"
                                    :events="events"
                                    hide-view-selector
                                    hideTitleBar
                            ></VueCal>
                        </div>
                    </div>
                </div>
            </section>
            <section id="instituicao" class="w-full h-screen bg-fixed bg-center bg-cover overflow-auto" style="background-image: url('imgs/ite.jpeg'); min-width: 100vw">
                <div class="container">
                    <div class="flex mb-4">
                        <div class="bg-white" style="border-radius: 14px; height: 80vh; width: 90vw; box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2), 0 6px 20px 0 rgba(0,0,0,0.19);height:100%;">
                            <p class="font-bold section1-text section1-title mt-2" style="font-size: 4vh; margin-top: 4vh">Conheça a ITE - Instituição Toledo de Ensino</p>
                            <p class="section1-text" style="font-size: 2.2vh;">Sede oficial da SBC em Bauru
                            </p>
                            <div class="flex flex-row">
                                <div class="w-full sm:w-1/2 md:w-2/3 lg:w-2/3 xl:w-2/3 m-4 border-solid border-2 border-gray-500 card-inst center-content" style="background-color: #004731;">
                                    <div class="flex flex-wrap">
                                        <iframe class="" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3690.769254107142!2d-49.0966401854633!3d-22.32456482296583!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x94bf6645d046a863%3A0x32474a28d7b8b120!2sFaculdade+de+Direito+de+Bauru+-+ITE!5e0!3m2!1spt-BR!2sbr!4v1508958104539" width="100%" height="490" frameborder="0" style="height: -webkit-fill-available; margin: auto; border-radius: 30px" allowfullscreen=""></iframe>
                                    </div>
                                </div>
                                <div class="center-content w-full sm:w-1/2 md:w-1/3 lg:w-1/3 xl:w-1/3 m-4 border-solid border-2 border-gray-500 card-inst" style="background-color: #055E5B;">

                                    <div class="flex flex-wrap">
                                        <div class="w-full mb-4 bg-gray-500" style="margin-top:18%">
                                            FACEBOOK
                                        </div>
                                        <div class="w-full mb-4 bg-gray-400" style="margin-top:15%">
                                            INSTAGRAM
                                        </div>
                                        <div class="w-full mb-4 bg-gray-500" style="margin-top:15%">
                                            SITE
                                        </div>
                                        <div class="w-full mb-4 bg-gray-400" style="margin-top:15%">
                                            360
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </section>
            <section id="laboratorio" class="w-full h-screen" style="background-color: #2C9473">
                <div class="container-uncenter">
                    <div class="flex flex-col">
                        <div>
                            <p class="text-4xl font-bold section2-title">Conheça nosso laboratório</p>
                        </div>
                        <div>
                            <div class="flex flex-row ml-6 mr-6">
                                <div class="w-1/3 h-12 mr-6 cursor-pointer img-aligning-sides">
                                    <img class="img-card border-solid border-4 hover:border-gray-200 border-gray-900" src="imgs/lab1.jpeg" @click="index = 0; showMultiple()" />
                                </div>
                                <div class="w-1/3 h-12 mr-6 cursor-pointer img-aligning-middle">
                                    <img class="img-card border-solid border-4 hover:border-gray-200 border-gray-800" src="imgs/lab2.jpeg" @click="index = 1; showMultiple()" />
                                </div>
                                <div class="w-1/3 h-12 cursor-pointer img-aligning-sides">
                                    <img class="img-card border-solid border-4 hover:border-gray-200 border-gray-900" src="imgs/lab3.jpeg" @click="index = 2; showMultiple()" />
                                </div>
                            </div>
                        </div>
                    </div>
                    <VueEasyLightbox
                        :visible="visible"
                        :imgs="imgs"
                        :index="index"
                        @hide="handleHide"
                    ></VueEasyLightbox>
                </div>
            </section>
<!--            <section class="w-full h-screen" style="background-color: #009465"></section>-->
        </div>
        <div>
            <div id="contato" class="flex mt-4 mb-4">
                <div class="w-2/4" style="margin-right: auto; margin-left: auto;">
                    <section class="bg-green-600" style="height: 60vh; box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2), 0 6px 20px 0 rgba(0,0,0,0.19); border-radius: 8px"></section>
                </div>
            </div>
        </div>
        <div class="flex flex-wrap h-24 center-content">
            <div class="w-full w-1/1 mt-2">
                <p class="text-xl font-bold ml-3">Nossos patrocinadores:</p>
            </div>
            <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4 xl:w-1/6 mt-12 mx-6 cursor-pointer">
                <img class="img-patrocinio" src="http://maratona.ite.edu.br/images/arcasolutions.png" />
            </div>
            <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4 xl:w-1/6 mt-12 mx-6 cursor-pointer">
                <img class="img-patrocinio" src="http://maratona.ite.edu.br/images/partnerfusion.png" />
            </div>
            <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4 xl:w-1/6 mt-12 mx-6 cursor-pointer">
                <img class="img-patrocinio" src="http://maratona.ite.edu.br/images/ictus.png" />
            </div>
            <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4 xl:w-1/6 mt-12 mx-6 cursor-pointer">
                <img class="img-patrocinio" src="http://maratona.ite.edu.br/images/harpo.png" />
            </div>
            <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4 xl:w-1/6 mt-12 mx-6 cursor-pointer">
                <img class="img-patrocinio" src="http://maratona.ite.edu.br/images/neoassist.gif" />
            </div>
        </div>
    </div>
</template>

<script>
    import VueEasyLightbox from 'vue-easy-lightbox'
    import VueCal from 'vue-cal'
    import 'vue-cal/dist/vuecal.css'

    export default {
        name: "Body",
        components: {
            VueEasyLightbox,
            VueCal,

        },
        data() {
            return {
                imgs: '',  // Img Url , string or Array
                visible: false,
                index: 0,   // default
                events: [
                    {
                        start: '2019-06-14 9:00',
                        end: '2019-06-14 10:00',
                        title: 'Chegada dos times e entrega do material',
                        class: 'calendar-event-start',
                    },
                    {
                        start: '2019-06-14 10:00',
                        end: '2019-06-14 11:00',
                        title: 'Sessão de Aquecimento',
                        class: 'calendar-event-training',
                    },
                    {
                        start: '2019-06-14 12:00',
                        end: '2019-06-14 14:00',
                        title: 'Almoço',
                        class: 'calendar-event-launch',
                    },
                    {
                        start: '2019-06-14 14:00',
                        end: '2019-06-14 19:00',
                        title: 'Competição',
                        class: 'calendar-event-competition',
                    },
                    {
                        start: '2019-06-14 19:00',
                        end: '2019-06-14 20:30',
                        title: 'Encerramento, divulgação dos resultados e premiações',
                        class: 'calendar-event-results',
                    }
                ],
                scrollPosition: null
            }
        },
        methods: {
            showMultiple() {
                this.imgs = ['imgs/lab1.jpeg', 'imgs/lab2.jpeg', 'imgs/lab3.jpeg']
                this.show()
            },
            show() {
                this.visible = true
            },
            handleHide() {
                this.visible = false
            },
            updateScroll() {
                this.scrollPosition = window.scrollY
            }
        },
        created() {
        },
        mounted() {

            var controller = new this.$scrollmagic.Controller({
                globalSceneOptions: {duration: "100%"}
            });

            var scene1 = new this.$scrollmagic.Scene({triggerElement: "#sobre"})
                .setClassToggle("#menu-sobre", "active")
                .addTo(controller);
            var scene2 = new this.$scrollmagic.Scene({triggerElement: "#laboratorio"})
                .setClassToggle("#menu-laboratorio", "active")
                .addTo(controller);
            var scene3 = new this.$scrollmagic.Scene({triggerElement: "#programacao"})
                .setClassToggle("#menu-programacao", "active")
                .addTo(controller);
            var scene4 = new this.$scrollmagic.Scene({triggerElement: "#instituicao"})
                .setClassToggle("#menu-instituicao", "active")
                .addTo(controller);
            var scene5 = new this.$scrollmagic.Scene({triggerElement: "#contato"})
                .setClassToggle("#menu-contato", "active")
                .addTo(controller);
        },
        destroy() {
        }
    }

</script>

<style scoped>
    .center-content {
        justify-content: center;
        align-items: center;
    }

    .container {
        margin: 0 auto;
        min-height: 100vh;
        min-width: 100vw;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
    }
    .container-uncenter {
        margin: 0 auto;
        min-height: 100vh;
        display: flex;
        justify-content: center;
        text-align: center;
    }

    /*SECTION 1*/
    .section1-text {
        font-family: 'Roboto Mono', monospace;
    }
    .section1-title {
        margin-top: 2vh;
    }
    .section1-text-content {
        margin-top: 2vh;
        margin-left: 4vw;
        margin-right: 4vw;
    }
    .section1-complement {
        font-family: 'Quicksand', sans-serif;
        margin-top: 4vh;
    }
    .section1-link {
        font-family: 'Quicksand', sans-serif;
    }

    /*SECTION 2*/
    .section2-title {
        font-family: 'Roboto Mono', monospace;
        margin-top: 8vh;
    }
    .img-card {
        border-radius: 8px;
        box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2), 0 6px 20px 0 rgba(0,0,0,0.19);
        height:
    }
    .img-aligning-middle {
        margin-top: 30vh;
    }
    .img-aligning-sides {
        margin-top: 15vh;
    }

    .card-inst {
        height: 60vh;
        border-radius: 32px
    }

    .card-inst:hover {
        border-color: #00E099;
    }

    #map {
        height: 400px;  /* The height is 400 pixels */
        width: 100%;  /* The width is the width of the web page */
    }

    /*FOOTER*/
    .img-patrocinio {
        max-width:200px;
        max-height:100px;
        width: auto;
        height: auto;
    }

</style>
