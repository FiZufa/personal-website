<template>
    <header class="header">

        <div class="menus">
            
            <button class="java-btn" :class="{ active: $route.path === '/' }" @click="gotoAnotherPage('/')">Home</button>

            <button class="user-btn" :class="{ active: $route.path === '/portofolio' }" @click="gotoAnotherPage('/portofolio')">Portfolio</button>

            <button class="error-btn" :class="{ active: $route.path === '/cv' }" @click="gotoAnotherPage('/cv')">CV</button>

            <button class="answer-btn" :class="{ active: $route.path === '/about' }" @click="gotoAnotherPage('/')">About me</button>

        </div>

    </header>

</template>
<script>
export default {
  methods: {
    gotoAnotherPage(path) {
      this.$router.push(path);
    },
  },
};

</script>
<style>

html, body {
    margin: 0;
    padding: 0;
    height: 100%;
    font-family: 'Lato', sans-serif;
}

.header {
    margin: 0;
    padding: 6px 180px;
    top: 0;
    color: #fff;
    background-color: #fff;
    
    text-align: center;
    align-items: center;
    display: flex;
    flex-direction: row;
    margin-top: 0;
    border-bottom: 1px solid #ccc;

  }

  .menus {
    display: flex;
    justify-content: space-around;
    align-items: center;
    flex-wrap: wrap;

  }

  .menu-container {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .menus button {
    display: flex;
    flex-direction: row;
    align-items: center;
    padding: 15px;
    background: none;
    border: none;
    cursor: pointer;
    font-size: 1em;
    gap: 0.1em;
    opacity: 60%;
  }

  .menus button:hover {
    opacity: 100%;
  }

  .menus button.active {
    opacity: 100%;
  }

</style>
