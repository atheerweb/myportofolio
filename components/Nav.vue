<template>
     <nav class="nav__container">
        <h1>يوسف مصطفي</h1>
        <div class="navBar">
          <div class="bar"></div>
          <div class="bar"></div>
          <div class="bar"></div>
        </div>
      </nav>
</template>

<script>
export default {
mounted(){
    console.log("nav Mounted")
}
}
</script>

<style lang="scss" scoped>
.nav__container {
    grid-area: 1/1/2/13;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  h1 {
    font-family: "Rakkas", cursive;
    font-size: 2.08rem;
    margin-top: 0.8em;
  }
  .navBar {
    margin-top: 0.8em;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    .bar:nth-child(1) {
      width: 1.5em;
      background-color: black;
      height: 0.31em;
      border-radius: 5em;
      margin-bottom: 0.28em;
    }
    .bar:nth-child(2) {
      width: 2.3em;
      background-color: black;
      height: 0.19em;
      border-radius: 10em;
      margin-bottom: 0.28em;
    }
    .bar:nth-child(3) {
      width: 3em;
      background-color: black;
      height: 0.3em;
      border-radius: 5em;
    }
  }
</style>