<script setup>
import Footer from '../components/Footer.vue'
import {
    useRouter
  } from 'vue-router'
  const router = useRouter()
</script>

<template>
  <div class="wrapper">
    <h1>Сложнейшую таску осилит лишь сильнейший. Или любой трудяга с CookManager</h1>
    <p>Простой, удобный и единственный инструмент нужный вам для планирования</p>
    <img src="../assets/business.png">
    <button @click="router.push({ name: 'logup' })">Начать бесплатно</button>
    <!-- <router-link :to="{ name: 'login' }">Войти в аккаунт</router-link> -->
    <RouterLink to="/login">Войти в аккаунт</RouterLink>

    <Footer/>
  </div>
</template>

<style scoped>
img{
  display: block;
  width: 40%;
  margin-left: auto;
  margin-right: auto;
}
h1{
  margin-top: 10%;
  margin-bottom: 1%;
  font-size: 30;
  font-weight: 600;
  text-align: center;
}
p{
  margin-top: 0%;
  margin-bottom: 1%;
  font-size: 20;
  text-align: center;
}
button{
  color: black;
  background: white;
  border-radius: 5px;
  width: 30%;
  padding: 10px;
  margin-left: auto;
  margin-right: auto;
  margin-top: 5%;
  font-size: 30;
  cursor: pointer;
  transition: transform 500ms ease;
}
button:hover {
  transform: scale(1.1) translateY(-2px);
}
</style>
