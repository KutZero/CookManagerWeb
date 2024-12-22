<script>
import BaseForm from './BaseForm.vue'
import {useRouter  } from 'vue-router'

const router = useRouter()

export default{
    components: {BaseForm},
    props: {
        title: {
            type: String,
            required: true
        }
    }
}
</script>

<template>
    <BaseForm v-bind:title="title" >
        <div>
            <h2>Введите ваши учетные данные</h2>
            <input class="white_border_input" type="text">
            <input class="white_border_input" type="text">
            <button class="blue_button" @click="router.push({ name: 'projects'})">Войти</button>
            <RouterLink to="/">Отмена</RouterLink>
            <router-link :to="{ name: 'hello'}">Отмена</router-link>
            <router-link :to="{ name: 'loginup', params: { scenario: 'forgot_password' } }">Не помню пароль</router-link>
        </div>
    </BaseForm>
</template>

<style>

</style>