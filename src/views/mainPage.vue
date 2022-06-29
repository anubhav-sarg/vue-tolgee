<style>






    @import url('https://fonts.googleapis.com/css2?family=Raleway:wght@500&display=swap');
    .main-body{
        font-family: 'Rubik', sans-serif;
        font-size: 55px;
        margin-top: 7.5rem;
        text-align: left;
        color: white !important;
        padding-left: 7rem;
        padding-right: 45rem;
        font-weight: 650;
    }

    .select-css{
        font-family: 'Rubik', sans-serif;
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
        font-family: 'Rubik', sans-serif;
        font-weight: 650;
        font-size: 55px;
        text-align: left;
        padding-left: 7rem;
        padding-right: 45rem;
    }

    .heading{
        font-family: 'Rubik', sans-serif;
        color: rgb(250, 250, 112);
        margin-top: 0.9rem;
        font-size: 30px;
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
        padding-bottom: 14rem;
    }

    .image-css{
        height: 4rem;
        width: auto;
        margin-top: 2.5rem;
        margin-bottom: -1.3rem;
        margin-left: -1rem;
    }

    .select-inner-css{
        color: white;
        background-color: black;
        font-family: 'Rubik', sans-serif;
        text-align: right;
        margin-left: 38rem;
        margin-top: -2rem;
        font-size: 25px;
        border: none !important;
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
                <select v-model="language" class="lang-selector select-inner-css">
                    <option value="en" selected> English</option>
                    <option value="es-ES"> Spanish </option>
                    <option value="fr-FR"> French </option>
                </select>
            </div>
        </div>
        <br />
        <T keyName="main_content">
            <div class="main-body">
                All in One localization for your project. Integrate in less than one minute and it is open source !
            </div>
        </T>


    </div>
</template>
