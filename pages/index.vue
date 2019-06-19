<template>
    <body class="overflow-x overflow-y-hidden">
        <Header />
        <Body />
    </body>
</template>

<script>
import Header from '~/components/Header.vue';
import Body from '~/components/Body.vue';
import Footer from '~/components/Footer.vue';

export default {
    components: {
        Header,
        Body,
        Footer,
    }
}
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
  @apply min-h-screen flex justify-center items-center text-center mx-auto;
}

*/
/*SECTION 3 - Calendar*/
.calendar-event-start {
    background-color: #055E5B;
    color: white;
    border-radius: 5px;
}
.calendar-event-training {
    background-color: #044254;
    color: white;
    border-radius: 5px;
}
.calendar-event-launch {
    background-color: #0C617A;
    color: white;
    border-radius: 5px;
}
.calendar-event-competition {
    background-color: #004731;
    color: white;
    border-radius: 5px;
}
.calendar-event-results {
    background-color: #055E5B;
    color: white;
    border-radius: 5px;
}

div .vuecal__event-title {
    margin-top: 1rem;
}
</style>
