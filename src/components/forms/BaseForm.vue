<script>
export default{
    props: {
        title: {
            type: String,
            required: true
        }
    }
}
</script>

<template>
<div class="form_window">
    <div class="title_box">
        <h1 class="form_h1">{{title}}</h1>
    </div>
    <div class="content_box">
        <slot/>
    </div>
</div>
</template>

<style>
</style>