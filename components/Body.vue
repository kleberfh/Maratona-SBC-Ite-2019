<template>
    <div class="div-mother">
        <div class="div-father">
            <section id="sobre" class="section-div" style="background-image: url('imgs/maratona2018-1.jpeg');">
                <div class="section-container">
                    <div class="section-card">
                        <div class="section-content" id="main-card">
                            <p class="section1-title section1-text">
                                Maratona SBC de Programação 2019
                            </p>
                            <p class="section1-text section1-text-content">
                                A Maratona de Programação é um evento da Sociedade Brasileira de Computação que existe desde o ano de 1996.
                                A Maratona nasceu das competições regionais classificatórias para as finais mundiais do concurso de programação, o International Collegiate Programming Contest, e é parte da regional sulamericana do concurso. Neste ano ocorre a 24a. edição da Maratona.
                                Ela se destina a alunos e alunas de cursos de graduação e início de pós-graduação na área de Computação e afins (Ciência da Computação, Engenharia de Computação, Sistemas de Informação, Matemática, etc).
                                A competição promove nos estudantes a criatividade, a capacidade de trabalho em equipe, a busca de novas soluções de software e a habilidade de resolver problemas sob pressão.
                                De ano para ano temos observado que as instituições e principalmente as grandes empresas da área têm valorizado os alunos que participam da Maratona.
                            </p>
<!--                            <p class="section1-complement" style="font-size: 2vh"> Conheça mais sobre a Maratona SBC de Programação no site oficial: </p> <a class="section1-link" style="color: #2C9473" href="http://maratona.ime.usp.br/sobre19.html" target="_blank">http://maratona.ime.usp.br</a>-->
                        </div>
                    </div>
                </div>
            </section>
            <section id="2019" class="w-full h-screen" style="background-color: #2C9473">
                <div class="section-container">
                    <div class="section-card" style="padding: 0 !important;">
                        <div class="section-content" style="height: 80vh; width: 92vw">
                            <p class="section4-title section4-text-content">
                                Edição de 2019
                            </p>
                            <vue-easy-lightbox
                                :visible="visible_event"
                                :imgs="event_photos"
                                :index="event_index"
                                @hide="handleHide(true)"
                            ></vue-easy-lightbox>
                            <div class="carousel-div-section-pc">
                                <Carousel class="carousel-section"
                                          :autoplay="true"
                                          :autoplayHoverPause="true"
                                          :perPage="1"
                                          :navigationEnabled="true"
                                          :paginationActiveColor="'#00E099'"
                                          :paginationColor="'#b3b3b3'"
                                          :navigationClickTargetSize="20"
                                >
                                    <Slide class="slide" v-for="(photos, index) in event_photos" :key="photos">
                                        <div @click="() => {showImg(index, true)}">
                                            <img class="carousel-img" :src="photos"/>
                                        </div>
                                    </Slide>
                                </Carousel>
                            </div>
                            <div class="carousel-div-section-mobile">
                                <Carousel class="carousel-section"
                                          :autoplay="true"
                                          :perPage="1"
                                          :paginationActiveColor="'#00E099'"
                                          :paginationColor="'#b3b3b3'"
                                >
                                    <Slide class="slide" v-for="(photos, index) in event_photos" :key="photos">
                                        <div @click="() => {showImg(index, true)}">
                                            <img class="carousel-img" :src="photos"/>
                                        </div>
                                    </Slide>
                                </Carousel>
                            </div>
                        </div>
                    </div>
                </div>
            </section>
            <section id="programacao" class="section-div" style="background-color: #00E099">
                <div class="section-container">
                    <div class="section2-card">
                        <div class="section2-title section2-text">
                            <p>Veja a programação do dia:</p>
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
            <section id="instituicao" class="section-div" style="background-image: url('imgs/ite.jpeg'); min-width: 100vw">
                <div class="section-container">
                    <div class="section-div">
                        <div class="section3-main-card">
                            <p class="section2-text section3-title">Conheça a ITE - Instituição Toledo de Ensino</p>
                            <p class="section1-text" style="font-size: 1.4rem;">Sede oficial da SBC em Bauru
                            </p>
                            <div class="section3-cards">
                                <iframe class="section3-map-card" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3690.769254107142!2d-49.0966401854633!3d-22.32456482296583!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x94bf6645d046a863%3A0x32474a28d7b8b120!2sFaculdade+de+Direito+de+Bauru+-+ITE!5e0!3m2!1spt-BR!2sbr!4v1508958104539" width="100%" height="490" frameborder="0" allowfullscreen=""></iframe>
                                <div class="section3-card" style="background-color: #055E5B;">
                                    <div>
                                        <div class="w-full mb-4">
                                            Conheça nossas redes sociais:
                                        </div>
                                        <div class="section3-social-resp">
                                            <div class="section3-social-item">
                                                <a class="section3-social-link" href="https://www.facebook.com/iteoficial/" target="_blank">
                                                    <font-awesome-icon :icon="['fab', 'facebook-square']"></font-awesome-icon>
                                                    FACEBOOK
                                                </a>
                                            </div>
                                            <div class="section3-social-item">
                                                <a class="section3-social-link"  href="https://www.instagram.com/iteoficial/" target="_blank">
                                                    <font-awesome-icon :icon="['fab', 'instagram']"></font-awesome-icon>
                                                    INSTAGRAM
                                                </a>
                                            </div>
                                            <div class="section3-social-item">
                                                <a class="section3-social-link" href="https://www.ite.edu.br/" target="_blank">
                                                    <font-awesome-icon :icon="['fab', 'chrome']"></font-awesome-icon>
                                                    SITE
                                                </a>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </section>
            <section id="laboratorio" class="w-full h-screen" style="background-color: #2C9473">
                <div class="section-container">
                    <div class="section-card" style="padding: 0 !important;">
                        <div class="section-content" style="height: 80vh; width: 92vw">
                            <p class="section4-title section4-text-content">
                                Nossos Laboratórios
                            </p>
                            <vue-easy-lightbox
                                    :visible="visible_lab"
                                    :imgs="labs"
                                    :index="lab_index"
                                    @hide="handleHide(false)"
                            ></vue-easy-lightbox>
                            <div class="carousel-div-section-pc">
                                <Carousel class="carousel-section"
                                          :autoplay="true"
                                          :autoplayHoverPause="true"
                                          :perPage="1"
                                          :navigationEnabled="true"
                                          :paginationActiveColor="'#00E099'"
                                          :paginationColor="'#b3b3b3'"
                                          :navigationClickTargetSize="20"
                                >
                                    <Slide class="slide" v-for="(lab, index) in labs" :key="lab">
                                        <div @click="() => {showImg(index, false)}">
                                            <img class="carousel-img" :src="lab"/>
                                        </div>
                                    </Slide>
                                </Carousel>
                            </div>
                            <div class="carousel-div-section-mobile">
                                <Carousel class="carousel-section"
                                          :autoplay="true"
                                          :perPage="1"
                                          :paginationActiveColor="'#00E099'"
                                          :paginationColor="'#b3b3b3'"
                                >
                                    <Slide class="slide" v-for="(lab, index) in labs" :key="lab">
                                        <div @click="() => {showImg(index, false)}">
                                            <img class="carousel-img" :src="lab"/>
                                        </div>
                                    </Slide>
                                </Carousel>
                            </div>
                        </div>
                    </div>
                </div>
            </section>
        </div>
        <div>
            <div class="contato-card" id="contato">
                <img class="contato-img" src="imgs/contato/coordenador.jpeg" />
                <div class="contato-text">
                    <p class="contato-title"> Professor e Coordenador Anderson Talon</p>
                    <p class="contato-desc"> Coordenador dos cursos 'Sistema de Informação' e 'Análise e Desenvolvimento de Sistemas' além de ser o organizador responsável pela maratona em Bauru e na ITE </p>
                    <div class="contato-links">
                        <div class="contato-link">
                        <a class="contato-email" href="mailto:anderson.talon@ite.edu.br">Email: anderson.talon@ite.edu.br </a>
                        </div>
                        <div class="contato-link">
                        <a class="contato-tel" href="tel:1421075000">Telefone: (14) 2107-5000 </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="patrocinadores">
            <div class="">
                <p class="patr-title">Nossos patrocinadores:</p>
            </div>
            <div class="patr-imgs">
                <img class="img-patrocinador" v-for="patr in patrs" :src="patr"/>
            </div>
        </div>
    </div>
</template>

<script>
    import VueEasyLightbox from 'vue-easy-lightbox'
    import VueCal from 'vue-cal'
    import 'vue-cal/dist/vuecal.css'
    import { Carousel, Slide } from 'vue-carousel';

    export default {
        name: "Body",
        components: {
            VueEasyLightbox,
            VueCal,
            Carousel,
            Slide

        },
        data() {
            return {
                event_photos: [
                    'imgs/2019/1.jpeg',
                    'imgs/2019/2.jpeg',
                    'imgs/2019/3.jpeg',
                    'imgs/2019/4.jpeg',
                    'imgs/2019/5.jpeg',
                    'imgs/2019/6.jpeg',
                    'imgs/2019/7.jpeg',
                    'imgs/2019/8.jpeg',
                    'imgs/2019/9.jpeg',
                    'imgs/2019/10.jpeg',
                    'imgs/2019/11.jpeg',
                    'imgs/2019/12.jpeg',
                    'imgs/2019/13.jpeg',
                    'imgs/2019/14.jpeg',
                    'imgs/2019/15.jpeg',
                    'imgs/2019/16.jpeg',
                    'imgs/2019/17.jpeg',
                    'imgs/2019/18.jpeg',
                ],
                labs: [
                  'imgs/laboratorios/Laboratorio 3.jpeg',
                  'imgs/laboratorios/Laboratorio 4.jpeg',
                  'imgs/laboratorios/Laboratorio 6.jpeg',
                ],
                patrs: [
                'imgs/patrocinadores/ite.png',
                'imgs/patrocinadores/arcasolutions.png',
                'imgs/patrocinadores/firework.png',
                'imgs/patrocinadores/harpo.png',
                'imgs/patrocinadores/ictus.png',
                'imgs/patrocinadores/sinconecta.png',
                ],
                visible_event: false,
                visible_lab: false,
                event_index: 0,   // default
                lab_index: 0,   // default
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
                scrollPosition: null,
                slide: 0,
                sliding: null,
            }
        },
        methods: {
            showImg (index, target = false) {
                if (target) {
                    console.log(index);
                    this.event_index = index;
                    this.visible_event = true
                } else {
                    this.lab_index = index;
                    this.visible_lab = true
                }
            },
            handleHide (target = false) {
                if (target) this.visible_event = false;
                if (!target) this.visible_lab = false
            }
        },
        mounted() {
            var controller = new this.$scrollmagic.Controller({
                globalSceneOptions: {duration: "100%"}
            });

            var scene1 = new this.$scrollmagic.Scene({triggerElement: "#sobre"})
                .setClassToggle("#menu-sobre", "menu-item-active")
                .addTo(controller);
            var scene2 = new this.$scrollmagic.Scene({triggerElement: "#laboratorio"})
                .setClassToggle("#menu-laboratorio", "menu-item-active")
                .addTo(controller);
            var scene3 = new this.$scrollmagic.Scene({triggerElement: "#programacao"})
                .setClassToggle("#menu-programacao", "menu-item-active")
                .addTo(controller);
            var scene4 = new this.$scrollmagic.Scene({triggerElement: "#instituicao"})
                .setClassToggle("#menu-instituicao", "menu-item-active")
                .addTo(controller);
            var scene5 = new this.$scrollmagic.Scene({triggerElement: "#contato"})
                .setClassToggle("#menu-contato", "menu-item-active")
                .addTo(controller);
        },
    }

</script>

<style scoped>

    .div-mother {
        min-width: 100vw;
    }

    .div-father {
        display: flex;
        flex-wrap: wrap;
        flex-direction: row;
    }

    .section-div {
        min-width: 100vw;
        height: 100vh;
        width: 100%;
        -webkit-background-size: 100%;
        -moz-background-size: 100%;
        -o-background-size: 100%;
        background-size: 100%;
        -webkit-background-size: cover;
        -moz-background-size: cover;
        -o-background-size: cover;
        background-size: cover;
    }

    .section-container {
        margin: 0 auto;
        min-height: 100vh;
        min-width: 100vw;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
    }

    .section-card {
        display: block;
        margin-top: auto;
        margin-bottom: auto;
    }

    .section-content {
        border-radius: 14px;
        width: 80vw;
        background-color: white;
        box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2), 0 6px 20px 0 rgba(0,0,0,0.19);
    }

    /*SECTION 1*/
    .section1-text {
        font-family: 'Roboto Mono', monospace;
    }
    .section1-title {
        font-size: 2rem;
        margin-top: 1rem;
        font-weight: 700;
    }
    .section1-text-content {
        margin: 1rem;
        font-size: 1rem;
    }

    /*SECTION 2*/
    .section2-card {
        display: block;
        /*margin: 2rem;*/
    }
    .section2-text {
        font-family: 'Roboto Mono', monospace;
    }
    .section2-title {
        font-size: 2rem;
        margin-bottom: 1rem;
        font-weight: 700;
    }

    /*SECTION 3*/
    .section3-title {
        font-size: 2rem;
        margin: 2rem;
        font-weight: 700;
    }
    .section3-main-card {
        display: block;
        margin-top: auto;
        margin-bottom: auto;
        height: 40rem;
    }
    .section3-cards {
        display: inline-flex;
    }
    .section3-map-card {
        height: -webkit-fill-available;
        width: 42rem;
        margin: 1rem;
        border-radius: 30px;
        border: 2px solid #004731;
    }
    .section3-card {
        height: -webkit-fill-available;
        width: 42rem;
        margin: 1rem;
        border-radius: 30px;
        border: 2px solid #004731;
    }
    .section3-map-card:hover {
        border: 2px solid #00E099;
    }
    .section3-card:hover {
        border: 2px solid #00E099;
    }
    .section3-social {
        display:grid;
        margin: inherit;
        font-size: 1.5em;
    }
    .section3-social-link:hover {
        color: #00E099;
    }

    /*SECTION 4*/
    .section4-title {
        font-size: 2rem;
        font-weight: 700;
    }
    .section4-text-content {
        font-family: 'Roboto Mono', monospace;
        padding: 1rem 1rem 0rem 1rem;
    }
    .carousel-div-section-pc {
        padding-left: 5.5rem;
        padding-top: 1rem;
    }
    .carousel-div-section-mobile {
        display: none;
        padding-left: 4rem;
        padding-top: 1rem;
    }
    .carousel-section {
        height: 70vh;
        width: 80vw;
    }

    .carousel-img {
        object-fit: scale-down !important;
        max-width: 85vh !important;
        margin: auto !important;
    }

    #map {
        height: 400px;  /* The height is 400 pixels */
        width: 100%;  /* The width is the width of the web page */
    }

    /*Contato*/

    .contato-card {
        margin: 2rem;
        height: 20rem;
        background-color: #055E5B;
        box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2), 0 6px 20px 0 rgba(0,0,0,0.19);
        display: flex;
    }

    .contato-img {
        max-height: 20rem;
        width: auto;
        height: auto;
    }

    .contato-text {
        padding: 1rem;
    }

    .contato-title {
        font-size: 2rem;
        font-weight: bold;
        margin: 0.5rem;
    }

    .contato-desc {
        color: rgb(246, 252, 255);
        font-size: 1.2rem;
        margin: 0.5rem;
        padding-top: 1rem;
    }

    .contato-links {
        display: grid;
    }

    .contato-link {
        padding: 0.5rem;
    }

    .contato-email {
        font-size: 1.6rem;
        margin: 0.5rem;
    }

    .contato-email:hover {
        color: #00E099;
    }

    .contato-tel {
        font-size: 1.6rem;
        margin: 0.5rem;
    }

    .contato-tel:hover {
        color: #00E099;
    }

    /*Patrocinadores*/

    .patrocinadores {
        margin-top: 1rem;
        display: grid;
        background-color: #2C9473;
    }

    .patr-title {
        text-align: center;
        font-size: 2rem;
    }

    .patr-imgs {
        display: flex;
        flex-wrap: wrap;
    }

    .img-patrocinador {
        max-width: 20rem;
        max-height: 5rem;
        width: auto;
        height: auto;
        margin: 0.5rem;
    }

    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    @media only screen and (min-width: 961px) {
        #main-card {
            padding: 2rem
        }
        .section-card {
            padding-top: 12rem;
        }
        .section1-text-content {
            white-space: pre-line;
            font-size: 1rem;
            margin: 0.4rem;
        }

        .section3-map-card {
            height: 76vh !important;
        }

        .section3-card {
            height: 76vh !important;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
            font-size: 2rem;
        }
        .contato-desc {
            padding-bottom: 1rem;
        }
    }

    @media only screen and (min-width: 961px) and (max-width: 1400px) {
        .section3-cards {
            margin-left: 1rem;
            margin-right: 1rem;
            display: flex;
        }
        .section3-map-card {
            height: 76vh !important;
            margin: 1rem auto;
        }
        .section3-card {
            height: 76vh;
        }
        .contato-text {
            padding: 0.5rem;
        }

        .contato-title {
            font-size: 2rem;
            font-weight: bold;
            margin: 0.5rem;
        }

        .contato-desc {
            color: rgb(246, 252, 255);
            font-size: 1rem;
            margin: 0.5rem;
            padding-top: 0.5rem;
        }

        .contato-links {
            display: grid;
        }

        .contato-link {
            padding: 0.2rem;
        }

        .contato-email {
            font-size: 1.6rem;
            margin: 0.5rem;
        }

        .contato-tel {
            font-size: 1.6rem;
            margin: 0.5rem;
        }
    }

    @media only screen and (max-width: 960px) {
        #main-card {
            padding: 0.5rem
        }
        .section1-title {
            font-size: 1.4rem;
        }
        .section-card {
            padding-top: 7rem;
        }
        .section1-text-content {
            white-space: pre-line;
            font-size: 0.6rem;
            margin: 0.4rem;
        }
        .section2-card {
            margin-top: 0.1rem;
        }
        .section3-cards {
            display: grid;
            height: 70%;
        }
        .section3-title {
            font-size: 1.4rem;
        }
        .section3-map-card {
            border-radius: 30px;
            width: -webkit-fill-available;
            margin: .2rem auto;
        }
        .section3-card {
            width: -webkit-fill-available;
            margin: .4rem;
            height: 100%;
        }
        .section3-social-resp {
            display: inline-flex;
            margin-top: 1rem;
        }
        .section3-social-item {
            margin-right: 0.5rem;
        }
        .patr-title {
            margin: auto;
        }
        .patr-imgs {
            display: grid;
        }

        .contato-card {
            border-radius: 10px;
            margin: 1rem;
            height: 30%;
            background-color: #055E5B;
            box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2), 0 6px 20px 0 rgba(0,0,0,0.19);
            display: grid;
        }

        .contato-img {
            padding-top: 0.5rem;
            max-height: 10rem;
            border-radius: 50%;
            width: auto;
            height: auto;
            margin: auto;
        }

        .contato-text {
            padding: 0.2rem;
        }

        .contato-title {
            font-size: 1.6rem;
            font-weight: bold;
            margin: auto;
            text-align: center;
        }

        .contato-desc {
            color: rgb(246, 252, 255);
            font-size: 1rem;
            margin: 0.5rem;
            padding-top: 0.5rem;
            text-align: center;
        }

        .contato-links {
            display: grid;
        }

        .contato-link {
            padding: 0.1rem;
            text-align: center;
        }

        .contato-email {
            font-size: 1.6rem;
            margin: 0.2rem;
        }

        .contato-tel {
            font-size: 1.6rem;
            margin: 0.2rem;
        }

        .carousel-div-section-pc {
            display: none;
            padding-left: 4rem;
            padding-top: 1rem;
        }

        .carousel-div-section-mobile {
            display: block;
            padding-left: 3.5rem;
            padding-top: 1rem;
        }


        .img-patrocinador {
            max-width: 20rem;
            max-height: 5rem;
            width: auto;
            height: auto;
            margin: 0.5rem auto;
        }
    }

    @media only screen and (max-width: 400px) {
        .carousel-img {
            max-width: 100% !important;
        }

        .carousel-div-section-mobile {
            padding-left: 1.5rem;
            padding-top: 6rem;
        }
    }

</style>
