<template>
    <section>
        <ion-header>
            <ion-toolbar>
                <ion-buttons slot="start">
      
                </ion-buttons>
                <ion-title>Home</ion-title>
            </ion-toolbar>
        </ion-header>
            <ion-button v-on:click="testClic()">
                Alerta
            </ion-button>     
            <ion-label>{{label1}}</ion-label>
          

        <Footer style="z-index:-1;"></Footer>
    </section>
</template>

<script>
import Footer from '../components/Footer.vue'

export default {
    components: {
        Footer,
    },
    data(){
        return{
            label1:'antes de hola',
        }
    },
    methods:{
        testClic(){
        this.label1=' despues de hola';
        },


    }
}
</script>

<style>

</style>