<template>
<div class="main__page">
 <Loading/>
</div>
</template>

<script>
export default {
};
</script>

<style lang="scss">


//theme colors

:root {
  --primary: #ded3f5;
  --text: #000000;
}
*{
  margin:0;
  padding: 0;
  background-size: cover;
  font-family: 'Noto Kufi Arabic', sans-serif;
}
.container {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  grid-template-rows: 100vh ;
  grid-column-gap: 1fr;
  grid-row-gap: 0px;
  background-color:red;
}
@keyframes scroll {
  0% {
    transform: translateX(170vw);
  }
  100% {
    transform: translateX(-170vw);
  }
}
</style>
