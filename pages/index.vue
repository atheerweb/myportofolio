<template>
  <div class="main">
    <div class="container">
      <Nav />
    </div>
     <Loading />
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
//theme colors

:root {
  --primary: #ded3f5;
  --text: #000000;
}

// Main Rules
* {
  margin: 0;
  padding: 0;
  background-size: cover;
  font-family: "Noto Kufi Arabic", sans-serif;
  direction: rtl;
}
.container {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  grid-template-rows: 5em;
  grid-column-gap: 1fr;
  grid-row-gap: 0px;
  background-color: var(--primary);
  padding: 0 1em;
  height: 100vh;
}
.main{
  width:100%;
  height: 100%;
}
// animations

@keyframes scroll {
  0% {
    transform: translateX(170vw);
  }
  100% {
    transform: translateX(-170vw);
  }
}
</style>
