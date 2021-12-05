<template>
  <Loading />
</template>

<script>
export default {
};
</script>

<style lang="scss">


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
}
</style>
