<template>
  <header class="header">
    <div class="menus">
      <button class="home-btn" :class="{ active: $route.path === '/' }" @click="gotoAnotherPage('/')">Home</button>

      <div class="menus-three" :class="{ 'show-menu': menuVisible }">
        <button class="porto-btn" :class="{ active: $route.path === '/portfolio' }" @click="gotoAnotherPage('/portfolio')">Portfolio</button>
        <button class="cv-btn" :class="{ active: $route.path === '/cv' }" @click="gotoAnotherPage('/cv')">CV</button>
        <button class="about-btn" :class="{ active: $route.path === '/' && $route.hash === '#about-me' }" @click="gotoAnotherPage('/#about-me')">About me🍃</button>
      </div>
    </div>

    <div class="right-header">
      <img class="burger-btn" src="assets/icon_burger.png" @click="toggleMenu" alt="Menu">
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      menuVisible: false, // To control the visibility of the menu
    };
  },
  methods: {
    gotoAnotherPage(path) {
      this.$router.push(path);
    },
    toggleMenu() {
      this.menuVisible = !this.menuVisible; // Toggle menu visibility
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

  .menus, .menus-three {
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

  .burger-btn {
    width: 3.5rem;
    height: auto;
    display: none;
    cursor: pointer;
  }

  .right-header {
    display: flex;
    justify-content: flex-end;
    align-items: center;
    position: absolute; 
    top: 10px;
    right: 20px;
  }

  @media screen and (max-width: 1024px) {
    .header {
        padding: 1% 3%; /* Reduced padding */
    }

    .burger-btn{
      display: block;
    }
    
    .menus button {
      color: #318CE7;
      opacity: 0.7;
    }
    .menus button.active {
      opacity: 1.0;
    }

    .menus-three {
      display: none;
    }


    .menus-three.show-menu{
      display: flex;
      flex-direction: row;
      padding: 0;
    }


}

</style>
