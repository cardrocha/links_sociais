<script>
export default {
  props: ['item']

}

</script>

<template>
  <div class="card">
    <a target="_blank" :href="item.href">
      <img :src="item.img" alt="Icone do serviços">
    </a>
    <span>{{ item.titulo }}</span>
  </div>

</template>

<style scoped>
div {
  text-align: center;
  display: block;
  width: 100px;
  margin: 20px 50px 20px 50px;
}

img {
  width: 100px;
  margin-bottom: 20px;
}

span {
  font-weight: 900;
}

.card {
  display: flex;
  justify-content: center;
  flex-direction: column;
  min-width: 120px;
  min-height: 150px;
  border: 1px solid #f9f9f9;
  border-radius: 5%;
  opacity: .9;
  box-shadow: 0 0 2em #1d1c1c;
  transition: box-shadow .5s;
}

.card a {
  margin-top: -45px;
}

.card:hover {
  box-shadow: 0 0 4em #1d1c1c;
  opacity: 1;
}
</style>
