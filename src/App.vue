<script setup>
import Item from './components/item.vue'
</script>


<script>
import Dados from './Dados/Services.json';
export default {
  data(){
    return {
      servicos: null
    }
  },
  mounted(){
    this.servicos = Dados;
  }

}

</script>

<template>
  <header>
    <img src="https://github.com/cardrocha.png" alt="logo vue"/>
  <h1>Ricardo Rocha</h1>
  </header>

<hr>
<div class="items">
  <Item
  v-for="servico, index in servicos"
  :key="index"
  :item="servico" />
</div>
<footer>
  <p>Ricardo Rocha - Adaptado de <a target="_blank" href="https://www.youtube.com/@yurimarcon">Yuri Marcon</a></p>
</footer>
</template>

<style>
#app{
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  text-align: center;
  color: #2c3e50;
}

h1 {
  text-align: center;
}

body{
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
  overflow-x: hidden;
  overflow-y: auto;
  background-image: url("https://img.freepik.com/fotos-gratis/copie-a-tecnologia-sem-fio-do-espaco-no-fundo-de-madeira_23-2148223229.jpg?w=740&t=st=1676932739~exp=1676933339~hmac=e05553320ab399930357939616e5b30d59a5ae7869d47c606140a02c9fee29a6");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  margin-bottom: 50px;
}

img {
    width: 150px;
    border-radius: 50%;
    margin: auto;
    display: block;
    margin-top: 50px;
}

.items{
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}

footer {
  position: fixed;
  bottom: 0;
  width: 100%;
  height: 50px;
  background-color: rgb(99, 135, 206);
  text-align: center;
  color: #000;
}

a {
  list-style: none;
  text-decoration: none;
  color: #000;
  font-weight: bold;
}
</style>
