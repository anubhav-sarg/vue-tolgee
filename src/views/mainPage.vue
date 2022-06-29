<style>

    @import url('https://fonts.googleapis.com/css2?family=Anek+Malayalam:wght@300;400&family=Dongle:wght@300&family=Indie+Flower&family=Montserrat:wght@300;400&family=Poppins:wght@300;400;500&family=Ubuntu:wght@500&family=Zen+Kurenaido&display=swap');
    .main-body{
        font-family: 'Anek Malayalam', sans-serif;
        font-size: 55px;
        margin-top: 7.5rem;
        text-align: left;
        color: white !important;
        padding-left: 7rem;
        padding-right: 45rem;
        font-weight: 650;
    }

    .select-css{
        font-family: 'Anek Malayalam', sans-serif;
        background-color: black;
        color: white;
        text-align: right;
        margin-left: 20rem;
        margin-top: -2rem;
        font-size: 25px;
        border: none !important;
        padding: 0rem 0px 10px 15rem;
        float: left;
        width: 30%;
    }

    .parent-css{
        background-color: black;
        margin: -8px;
        padding-bottom: 40rem;
        color: white;
        font-family: 'Anek Malayalam', sans-serif;
        font-weight: 650;
        font-size: 55px;
        text-align: left;
        padding-left: 7rem;
        padding-right: 45rem;
    }

    .heading{
        font-family: 'Anek Malayalam', sans-serif;
        color: rgb(250, 250, 112);
        margin-top: 0.9rem;
        font-size: 30px;
        padding-left: 20px;
        float: left;
        width: 70%;
    }
/*
    .container-name div {
        display: inline-block;
        width: 500px;
        min-height: 50px;
        height: auto;
        margin-top: 2.5rem;
    }*/

    .container-name ::after{
        content: "";
        display: table;
        clear: both;
    }

    .container-name{
        color: white;
        padding-bottom: 12.5rem;
    }

    .image-css{
        height: 4rem;
        width: auto;
        margin-top: 2.5rem;
        margin-left: 5rem;
        margin-bottom: -1.3rem;
    }

</style>


<script>
import { defineComponent } from 'vue';
import { useLanguage } from '@tolgee/vue';
import { T } from "@tolgee/vue";


export default defineComponent({
    components: { T },
    setup() {
        const language = useLanguage();
        return {language};
    },
});



</script>

<template>
    <div class="parent-css">
        <div class="container-name">
            <div class="heading">
                <img src="../assets/tolgee.png" class="image-css">
            </div>
            <div class="select-css">
                <select v-model="language" class="lang-selector select-css">
                    <option value="en" selected> English</option>
                    <option value="es-ES"> Spanish </option>
                    <option value="fr-FR"> French </option>
                </select>
            </div>
        </div>
        <br />
        <T keyName="main_content">
            <div class="main-body">
                This is a demo to showcase how to translate web apps using Tolgee with VueJS.
            </div>
        </T>


    </div>
</template>
