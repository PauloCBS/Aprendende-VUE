
 <template>
      <div class="teste-for">
        <h2>TesteFor</h2>
        <ul>
            <li v-for="animal of animais" :key="animal.id" >
                <img :src="animal.url" :alt="animal.nome">
            </li>
        </ul>

    </div>
  </template>
	
<script>
export default{
    name:'TesteFor',
    data() {
        return{
            animais:[
            {
                id: 1,
                nome: 'Gatinho',
                url: 'https://inovaveterinaria.com.br/wp-content/uploads/2015/04/gato-sem-raca-INOVA-1536x1024.jpg'
            },
             {
                 id: 2,
                nome: 'Cachorrinho',
                url: 'https://matsudapet.com.br/blog/wp-content/uploads/2019/08/shutterstock_559799125-compressed.jpg'
            }
            ]
        }
    }
}
</script>

<style scoped>
</style>