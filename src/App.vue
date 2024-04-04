<script setup>
import { ref } from 'vue'
import axios from 'axios'
import headers from './components/header.vue';
import coffeinfo from './components/coffeinfo.vue';
import slider from './components/slider.vue';
import sliderFooter from './components/sliderFooter.vue';
import best from './components/best.vue';
import footers from './components/footer.vue';
</script>

<template>
<headers/>
<coffeinfo/>
<slider/>
<best/>
<sliderFooter/>
<footers/>
</template>

<style scoped>

</style>
