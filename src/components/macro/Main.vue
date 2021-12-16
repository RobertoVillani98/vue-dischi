<template>
  <main>
    <div class="disk-list row">
      <DiskCard v-for="(disk, index) in disks" :key="index" :info="disk" />
    </div>
  </main>
</template>

<script>
import axios from "axios";
import DiskCard from "../parts/DiskCard.vue";

export default {
  name: "Main",
  components: {
    DiskCard,
  },
  data() {
    return {
      disks: null,
    };
  },
  created() {
    // get disks array
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((response) => {
        // handle success
        this.disks = response.data.response;
      })
      .catch(function (error) {
        // handle error
        console.log(error);
      });
  },
};
</script>

<style lang="scss" scoped>
.container {
  max-width: 1200px;
  margin: 0 auto;
}
main {
  background-color: #1e2d3b;
  min-height: calc(100vh - 80px);
}

.disk-list > * {
  width: calc(100% / 5 - 40px);
  margin: 30px 20px;
}
</style>