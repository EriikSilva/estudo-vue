<template>
    <div>
        <h2>Formulario: </h2>
        <form action="" @submit="enviarFormulario($event)">
            <div>
                <input type="text" v-model="name">
            </div>
            <div>
                <input type="text" v-model="email">
            </div>
            <button type="submit">Enviar</button>
        </form>
    </div>
</template>

<script>
export default {
   name:'Form',
   data(){
    return{
        name:'',
        email:''
    }
   },methods:{
    enviarFormulario(e){
        
        e.preventDefault();

        const email = this.email;
        const name = this.name;

        console.log("nome: " + this.name + " email: " + this.email)
        
    }
   }

}
</script>