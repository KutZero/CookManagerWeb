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
            <div>
                <input class="white_border_input" type="text">
                <p>Придумайте логин</p>
            </div>
            <div>
                <input class="white_border_input" type="text">
                <p>Придумайте пароль</p>
            </div>
            <div>
                <input class="white_border_input" type="text">
                <p>Больше 8 символов, хотя бы по одному спецсимволу, цифре, заглавной и строчной букве. (Молю, только не твой день рожденья)</p>
            </div>
            <button class="white_border_button" @click="router.push({ name: 'hello'})">Отмена</button>
            <button class="blue_button">Создать</button>
            <router-link :to="{ name: 'loginup', params: { scenario: 'login' } }">Уже есть аккаунт (я вас обманул)</router-link>
        </div>
    </BaseForm>
</template>

<style>
p{
    display: inline-block;
}
</style>