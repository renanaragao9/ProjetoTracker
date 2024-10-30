<template>
    <div class="box">
        <slot></slot>
    </div>
</template>

<script lang="ts">
    import { defineComponent } from 'vue';

    export default defineComponent ({
        name: 'BoxProjeto'
    })
</script>

<style>
    .box {
        background: #fafafa;
        color: #000;
        font-weight: bold
    }
</style>