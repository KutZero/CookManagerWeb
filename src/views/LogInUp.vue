<script>
import Footer from '../components/Footer.vue'
import CodeInputForm from '../components/forms/CodeInputForm.vue'
import LogInForm from '../components/forms/LogInForm.vue' 
import LogUpForm from '../components/forms/LogUpForm.vue' 
import MessageForm from '../components/forms/MessageForm.vue' 
import NewPasswordForm from '../components/forms/NewPasswordForm.vue' 
import { RouterLink, RouterView } from 'vue-router'

export default {
    components: {Footer, CodeInputForm, LogInForm, LogUpForm, 
        MessageForm, NewPasswordForm, RouterLink, RouterView}

}
</script>

<template>
    <div v-if="$route.params.scenario == 'login'">
        <LogInForm v-if="$route.params.stage == 'init'" title="Вход"></LogInForm>
    </div>
    <div v-if="$route.params.scenario == 'logup'">
        <LogUpForm v-if="$route.params.stage == 'init'" title="Давайте создадим вам аккаунт"></LogUpForm>
    </div>
    <!-- 
    <CodeInputForm v-else-if="$route.params.scenario == 'forgot_password'" title="Сброс пароля"></CodeInputForm>
    <NewPasswordForm v-else-if="$route.params.scenario == 'create_password'" title="Создание нового пароля"></NewPasswordForm>
    <MessageForm v-else-if="$route.params.scenario == 'success'" title="Создание нового пароля"></MessageForm> -->
    <RouterLink to="/">Назад</RouterLink>
    <Footer/>
</template>

<style>
</style>