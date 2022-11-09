<template>
    <div>
        <v-btn @click="descarregarUsuaris()">descarregar</v-btn>   
        <pre>
            {{usuaris}}
        </pre>
    </div>
</template>

<script>
export default{
    data:function(){
        return{
            usuaris:[]
        }
    },
    methods:{
        descarregarUsuaris(){
            
            var f = fetch('https://dummyjson.com/users')
        
            var j = f.then(function(resposta){
                return resposta.json()
            })


            var self = this

            j.then(function(dades){
                console.log(dades)
                self.usuaris = dades
            })


            /*
            .then(res =>{
            
            return  res.json()
            } )
            .then((usuaris)=>{

                console.log(usuaris)
            });
            */
        }
    }
}
</script>