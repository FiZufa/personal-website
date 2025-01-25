<template>
    <Header />
    <div class="porto-body">
        <h1 style="font-weight: 550;">Portfolio</h1>
        <PortoCourse />
    </div>

    <Footer />
    

</template>
<script>
import Header from '@/components/Header.vue'
import { PortoCourse } from '#components';
import { Footer } from '#components';

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

@media screen and (max-width: 1024px) {
    .porto-body {
        margin: 0 3% ;
    }
}

</style>