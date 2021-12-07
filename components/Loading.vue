<template>
  <div class="loading__animation" v-show="!disableComponent">
    <span :class="{ transforrm: transformActive, blob: blobActive }">
      <p v-show="blobActive">{{ precent }}</p>
    </span>
    <h3 v-show="blobActive">جاري التحميل</h3>
  </div>
</template>

<script>
export default {
  data() {
    return {
      precent: 0,
      transformActive: false,
      blobActive: true,
      disableComponent: false,
    };
  },
  methods: {
    precentF() {
      if (this.precent < 100) {
        return this.precent++;
      }
    },
    tactive() {
      this.transformActive = !this.transformActive;
      this.blobActive = !this.blobActive;
    },
    Component() {
      this.disableComponent = !this.disableComponent;
    },
  },
  mounted() {
    setInterval(this.precentF, 40);
    setTimeout(this.tactive, 4000);
    setTimeout(this.Component, 5000);
    console.log("loading Mounted")

  },
};
</script>

<style lang="scss" scoped>
//animations

@keyframes blob {
  0%,
  100% {
    border-radius: 60% 40% 30% 70% / 60% 30% 70% 40%;
  }
  50% {
    border-radius: 30% 60% 70% 40% / 50% 60% 30% 60%;
  }
}

@keyframes transformm {
  0% {
    width: 7em;
    height: 86px;
  }
  100% {
    width: 500%;
    height: 500%;
  }
}

//vue methods classes
.blob {
  animation: blob 7s ease-in-out infinite both,
    movement 2s ease-in-out infinite both;
}
.transforrm {
  animation: transformm 900ms ease-in-out both;
}

.loading__animation {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  grid-area: 1 / 1 / 1 / 13;
  overflow: hidden;
  position: absolute;
  background-color: white;
  width: 100%;
  height: 100%;
  color: var(--text);
  top:0;

   span {
    background-color: #ded3f5;
    overflow: hidden;
    width: 7em;
    height: 86px;
    justify-content: center;
    display: flex;
    justify-content: center;
    align-items: center;
    position: absolute;
    border-radius: 30% 60% 70% 40% / 50% 60% 30% 60%;
    p {
      font-size: 1.5rem;
      font-weight: 800;
      transition: all 250ms ease-out;
    }
  }
  h3 {
    font-size: 1.5rem;
    margin-top: 12rem;
    font-weight: 800;
    z-index: 999999;
    transition: all 250ms ease-out;
  }
}
</style>
