<template>
  <div class="card">
    <img :src="info.poster" :alt="info.title" />
    <h3>{{ info.title }}</h3>
    <p>{{ info.author }}</p>
    <p>{{ info.year }}</p>
  </div>
</template>

<script>
export default {
  name: "DiskCard",
  props: {
    info: Object,
  },
};
</script>

<style lang="scss" scoped>
.card {
  background-color: #2e3a46;
  text-align: center;
  padding: 20px;
  border-radius: 40px;
  img {
    width: 100%;
    border-radius: 40px;
  }
  h3 {
    color: #fff;
    text-transform: uppercase;
    margin-top: 10px;
    margin-bottom: 20px;
  }
  p {
    color: #7e7f7d;
  }
}
</style>