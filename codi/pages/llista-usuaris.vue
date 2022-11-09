<template>
    <v-container class="contenidor">
        <v-row class="fila">
            <v-col 
                class="columna"
                v-for="usuari in usuaris"
                :key="usuari"
            >
                {{usuari}}
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
    data(){
        return{
            usuaris:["Jordi","Joan","Laura"]
        }
    },

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