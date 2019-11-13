<template>
    <section>
        
        <div style="text-align: center; position: absolute; top: 20%; width: 90%;"> <!-- Inicio Container  -->
        <b-button v-b-toggle.collapse-1.collapse-2 variant="light">Iniciar sesión</b-button>
        <b-button v-b-toggle.collapse-1.collapse-2 variant="light">Registarse</b-button>

        <div style="text-align: center; position: absolute; left:10%; width: 90%;"><!--  contenedor del formulario -->    
        <b-collapse visible id="collapse-1" class="mt-2"> <!-- Inicio register  -->
               
        
        <b-form @submit="onSubmit" @reset="onReset" v-if="show">
        <b-form-group
            id="input-group-1"
            label-for="input-1"
        >
            <b-form-input
            id="input-1"
            v-model="form.email"
            type="email"
            required
            placeholder="Enter email"
            ></b-form-input>
        </b-form-group>

        <b-form-group id="input-group-2" label-for="input-2">
            <b-form-input
            id="input-2"
            v-model="form.password"
            required
            placeholder="Enter password"
            ></b-form-input>
        </b-form-group>


        <b-button type="submit" block variant="dark">Entrar</b-button>
        <b-button type="reset" block variant="danger">Borrar</b-button>
        <br>
        <br>  
        <img src="../assets/separador.png" style="width:220px;"> 
        <br>  
        <img src="../assets/logos-g-f.png" style="width:70px;">
        </b-form>
        <b-card class="mt-3" header="Form Data Result">
           
        <pre class="m-0">{{ form }}</pre>
        </b-card>
        

        </b-collapse><!-- Fin register  -->
        </div>

<div style="text-align: center; position: absolute; left:10%; width: 90%;"><!--  contenedor del formulario -->    
        <b-collapse id="collapse-2" class="mt-2"> <!-- Inicio login  -->
             
        
    <b-form @submit="onSubmit2" @reset="onReset2" v-if="show">
      <b-form-group
        id="input-group-2"
        label-for="input-2"
      >
        <b-form-input
          id="input-2"
          v-model="form2.email"
          type="email"
          required
          placeholder="Enter email"
        ></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-2" label-for="input-2">
        <b-form-input
          id="input-2"
          v-model="form2.password"
          required
          placeholder="Enter password"
        ></b-form-input>
      </b-form-group>


      <b-button type="submit" block variant="dark">Entrar</b-button>
        <b-button type="reset" block variant="danger">Borrar</b-button>
        <br>
        <br>  
        <img src="../assets/separador.png" style="width:220px;"> 
        <br>  
        <img src="../assets/logos-g-f.png" style="width:70px;">
    </b-form>
    <b-card class="mt-3" header="Form Data Result">
      <pre class="m-0">{{ form2 }}</pre>
    </b-card>

        
        </b-collapse><!-- fin login  -->
</div>

        </div> <!-- Fin Container  -->
        <Footer style="z-index:-1;"></Footer>
    </section>
</template>



<script>
import Footer from '../components/Footer.vue'
  export default {
      components: {
        Footer,
    },
    data() {
      return {
        form: {
          email: '',
          password: '',        
        },
        form2: {
          email: '',
          password: '',        
        },
        show: true
      }
    },
    methods: {
      onSubmit(evt) {
        evt.preventDefault()
        alert(JSON.stringify(this.form))
      },
      onReset(evt) {
        evt.preventDefault()
        // Reset our form values
        this.form.email = ''
        this.form.password = ''
        this.show = false
        this.$nextTick(() => {
          this.show = true
        })
      },
      onSubmit2(evt) {
        evt.preventDefault()
        alert(JSON.stringify(this.form2))
      },
      onReset2(evt) {
        evt.preventDefault()
        // Reset our form values
        this.form2.email = ''
        this.form2.password = ''
        this.show = false
        this.$nextTick(() => {
          this.show = true
        })
      }
    }
  }
</script>