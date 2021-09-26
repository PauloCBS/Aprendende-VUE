<template>
    <div class="sites-favoritos">
        <h2>Sites favoritos</h2>
        <ul>
            <li v-for="site of SitesFavoritos" :key="site.id" >
                <a href="google.com">{{site.nome}}</a>
            </li>
           
        </ul>
    </div>
</template>

<script>
export default {
    name: 'SitesFavoritos',
    data(){
        return{
            SitesFavoritos: [] 
            }
        },
        created(){
            fetch('https://hackthon-decola.firebaseio.com/sites-favoritos.json')
            .then(resultado => resultado.json())
            .then(json => { this.SitesFavoritos = json;});
        }
    }
</script>

<style scoped>

</style>
