<template>
        <div><!--  Principal -->
            <div class="history" style="height:100vh; overflow:hidden;"><!--  History -->
            <div style="text-align: center; position: absolute; top: 45%; width: 100%;">
                <img src="../assets/logocraze.png" style="width:220px;"><br>
            </div>
                <div style="text-align: center; position: absolute; bottom: 10%; width: 100%;"><!--  Center -->    
                <b-button variant="light" style="width:80%;" to="/auth">Iniciar sesión</b-button>            
                    <br>  
                    <img src="../assets/separador.png" style="width:220px;"> 
                    <br>  
                    <img src="../assets/logos-g-f.png" style="width:70px;">
                    <br>
                    <ion-label style="color:white;">Registrarse</ion-label>
                </div><!--  Center -->
                    
            </div><!--  History -->
        </div><!--  Principal -->
</template>
<script>
import Footer from '../components/Footer.vue'

export default {
    components: {
        Footer,
        },    
        methods: {
        }
}
</script>

<style>
.history {
  background-image:linear-gradient(
      rgba(0, 0, 0, 0.5),
      rgba(0, 0, 0, 0.5)
    ), url('../assets/fondo.png');
  background-repeat: no-repeat;
  background-size:cover;  
}
</style>