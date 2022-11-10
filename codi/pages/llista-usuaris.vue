<template>
    <v-container class="contenidor">
        <v-row class="fila">
            <v-col 
                class="columna"
                v-for="(usuari,posicio) in usuaris"
                :key="posicio"
            >
                {{usuari.firstName}}

                <v-img v-bind:src="usuari.image"></v-img>

                
                
            </v-col>
        </v-row>
        <v-row>
            <v-col>
                <pre>{{usuaris}}</pre>
            </v-col>
        </v-row>
    </v-container>
</template>
<script>
export default{
    created(){
        console.log("S'ha creat la pagina")
    },
    mounted(){
        console.log(this.laClasse)
        console.log("S'ha muntat la pagina")
        this.descarregarUsuaris()

    },
    data(){
        return{
            laClasse:"columna",
            usuaris:[],
            jordi:"hola"
        }
    },
    methods:{
        async descarregarUsuaris(){
             console.log('Descarregant usuaris...')
            var resposta = await fetch('https://dummyjson.com/users')
            var json = await resposta.json()
            this.usuaris = json.users
            console.log(json)
        }
    }
}


</script>

<style>
    .columna{
        background-color: bisque;
        margin:20px;
    }
    .fila{
        background-color: rgb(108, 101, 90);
        margin:20px;
    }
    .contenidor{
        background-color: rgb(153, 135, 170);
    }
</style>