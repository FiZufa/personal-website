<template>
    <header class="header">

        <div class="menus">
            
            <button class="java-btn" @click="gotoAnotherPage('/')">Home</button>

            <button class="user-btn" @click="gotoAnotherPage('/')">Portfolio</button>

            <button class="error-btn" @click="gotoAnotherPage('/')">CV</button>

            <button class="answer-btn" @click="gotoAnotherPage('/')">About me</button>

        </div>

    </header>

</template>
<script>

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

  button {
    display: flex;
    flex-direction: row;
    align-items: center;
    padding: 15px;
    background: none;
    border: none;
    cursor: pointer;
    font-size: 1em;
    gap: 0.1em;
    opacity: 70%;
  }

  button:hover {
    opacity: 100%;
  }

</style>
