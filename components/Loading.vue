<template>
  <div class="container">
    <div class="loader">
      <span><p>100</p></span>
      <div class="h3__wrapper">
      <div class="h3__container">
        <h3>اضغط هنا لبدأ العظمة</h3>
      </div>
      <div class="h3__container">
        <h3>اضغط هنا لبدأ العظمة</h3>
      </div>
      <div class="h3__container">
        <h3>اضغط هنا لبدأ العظمة</h3>
      </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
};
</script>

<style lang="scss" scoped>
  .h3__container:nth-child(1){
     margin-left:2em;
   }
.loader {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  grid-area: 1 / 1 / 1 / 13;
  overflow:hidden;
  .h3__wrapper{
    display: flex;
  }
  .h3__container:nth-child(1){
margin-right:5em;
  }
  .h3__container:nth-child(3){
margin-left:5em;
  }
  .h3__container {
    display: flex;
    flex-direction: row;
    overflow: hidden;
    animation: scroll 8s linear infinite;
    h3 {
      font-size: 1.3rem;
      margin-top: 45px;
      font-weight: 300;
      white-space: nowrap;
    }
  }
  span {
    animation: blob 7s ease-in-out infinite both,
      movement 2s ease-in-out infinite both;
    background-color: #e7d3f5;
    overflow: hidden;
    width: 35%;
    height: 86px;
    justify-content: center;
    display: flex;
    justify-content: center;
    align-items: center;
    p {
      font-size: 1.8rem;
      font-weight: 200;
    }
  }
}

@keyframes blob {
  0%,
  100% {
    border-radius: 60% 40% 30% 70% / 60% 30% 70% 40%;
  }
  50% {
    border-radius: 30% 60% 70% 40% / 50% 60% 30% 60%;
  }
}
@keyframes movement {
  0%,
  100% {
    transform: rotateY(30deg);
  }
  50% {
    transform: rotateY(20deg);
  }
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
