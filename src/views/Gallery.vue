<template>
    <ion-app>
    <ion-content v-if="posts.length != 0" style="bottom:20px;">   
        <ion-card style="height:80%; top:10px;">
            <ion-slides  pager="true">
                <ion-slide v-for="post in posts" :key="post.id">
                    <img :src="post.url" alt>
                </ion-slide>                
            </ion-slides>            
        </ion-card> 

        <div style="text-align: center; margin-top:10%;">
        <b-button variant="success" style="">Me gusta</b-button>
        <b-button variant="outline-primary">No me gusta</b-button>
        </div>               
    </ion-content>

    <Footer style="z-index:-1;"></Footer>
    </div>
    </ion-app>
    
</template>

<script>
import axios from 'axios';
import Footer from '../components/Footer.vue'
export default {
    components: {
        Footer,
        }, 
  data(){
    return{
      posts: []
    }
  },
  async mounted(){
     const response = await axios.get("https://backend-app-laravel.herokuapp.com/api/getGallery")
     this.posts = response.data;
     console.log(response);
     
  },
  
  methods:{
      
  },
}

</script>