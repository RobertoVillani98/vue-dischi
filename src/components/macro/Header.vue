<template>
  <header>
    <div class="container">
      <img src="../../assets/img/logo.png" alt="" />
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style lang="scss" scoped>
.container {
  height: 80px;
  background-color: #2e3a46;
  line-height: 80px;

  img {
    height: 80%;
    vertical-align: middle;
    margin-left: 20px;
  }
}
</style>