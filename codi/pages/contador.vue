<template>
    <div>
        <h1>{{titol}}</h1>
        {{contador}}
        <button v-on:click="augmentar()">augmentar</button>
        <button @click="disminuir()">disminuir</button>
    </div>
</template>

<script>
    export default {
        data:function(){
            return{
                titol:"Contador vue",
                contador:0
            }
        },
        methods:{
            augmentar:function(){
                this.contador++
                this.titol = "He augmentat"
            },
            disminuir:function(){
                this.contador--
                this.titol = "He disminuit"
            }
        }
    }
</script>