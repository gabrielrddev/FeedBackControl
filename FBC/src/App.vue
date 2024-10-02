<script setup>
import { RouterView } from 'vue-router'
import HeaderItem from './components/HeaderItem.vue'
import FooterItem from './components/FooterItem.vue'

</script>

<template>
  <HeaderItem />
  <RouterView />
  <FooterItem />
</template>

<style>
body {
            background-color: #121212;
            color: white;
        }
</style>

