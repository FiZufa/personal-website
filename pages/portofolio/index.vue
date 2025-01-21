<template>
    <Header />
    <div class="porto-body">
        <h1>Portofolio</h1>
        <PortoCourse />
    </div>
    

</template>
<script>
import Header from '@/components/Header.vue'
import { PortoCourse } from '#components';

</script>
<style>
html, body {
    margin: 0;
    padding: 0;
    height: 100%;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;

}

.porto-body {
    margin: 0 180px;
}

</style>