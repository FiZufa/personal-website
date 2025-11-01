<template>
  <header class="header">
    <div class="menus">
      <button class="home-btn" :class="{ active: $route.path === '/' }" @click="gotoAnotherPage('/')">Home</button>
      <button class="porto-btn" :class="{ active: $route.path === '/portfolio' }" @click="gotoAnotherPage('/portfolio')">Portfolio</button>
      <!-- <button class="cv-btn" :class="{ active: $route.path === '/cv' }" @click="gotoAnotherPage('/cv')">CV</button> -->
      <button class="about-btn" :class="{ active: $route.path === '/' && $route.hash === '#about-me' }" @click="gotoAnotherPage('/#about-me')">About me🍃</button>
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

  .menus {
    display: flex;
    justify-content: space-around;
    align-items: center;
    flex-wrap: wrap;
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

  @media screen and (max-width: 1024px) {
    .header {
        padding: 1% 3%; /* Reduced padding */
        justify-content: center;
    }

    .burger-btn{
      display: block;
    }
    
    .menus button {
      gap: 0.05em;
      color: #318CE7;
      opacity: 0.7;
    }
    .menus button.active {
      opacity: 1.0;
    }

    .menus{
      
    }


}

</style>
