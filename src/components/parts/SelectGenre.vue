 <template>
  <div class="container-input">
    <select
      v-model="selectVal"
      name="Select Genre"
      @change="$emit('change', selectVal)"
    >
      <option value="">Seleziona un genere</option>
      <option value="Rock">Rock</option>
      <option value="Pop">Pop</option>
      <option value="Metal">Metal</option>
      <option value="Jazz">Jazz</option>
    </select>
    <button @click.prevent="$emit('change', '')">View All</button>
  </div>
</template>

<script>
export default {
  name: "SelectGenre",
  data() {
    return {
      selectVal: "",
    };
  },
};
</script>

<style lang="scss" scoped>
.container-input {
  text-align: center;
  select,
  button {
    background-color: #2e3a46;
    margin: 0 10px;
    padding: 10px 15px;
    border: none;
    color: white;
    font-weight: bold;
    border-radius: 20px;
    cursor: pointer;
  }
  button {
    margin-top: 20px;
    background-color: #59d860;
    border-radius: 20px;
    cursor: pointer;
  }
}
</style>