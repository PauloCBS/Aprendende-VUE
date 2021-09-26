<template>
    <div class="meu-contador">
        <h2>Meu contador</h2>
        <p><strong>contador:</strong>{{contador}}</p>
        <button @click="subtraiUm" >-</button>
        <button @click="somarUm">+</button>
    </div>
  
</template>
	
<script>
export default{ 
    name: 'MeuContador',

    data(){
        return{
            contador:0
        }
    },
    methods: {
        somarUm(){
            this.contador++;
        },
        subtraiUm(){
            this.contador--;
        }
    }
}
</script>

<style scoped>
</style>
