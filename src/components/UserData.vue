<template lang="">
  <form v-on:submit.prevent="submitData" class="form-control m-4">
    <div class="form-group">
      <label for="name">name</label>
      <input
        v-model="name"
        id="name"
        class="form-control form-control-sm"
        type="text"
      />
    </div>
    <div class="form-group">
      <label for="age">age</label>
      <input
        id="age"
        v-model="age"
        class="form-control form-control-sm w-10"
        type="number"
      />
    </div>

    <button class="btn btn-primary m-2">submit</button>
  </form>
</template>
<script>
export default {
  emits: ["emit-user-data"],
  data() {
    return {
      name: "",
      age: "",
    };
  },
  methods: {
    submitData() {
      this.$emit("emit-user-data", this.age, this.name);
      this.name = "";
      this.age = "";
    },
  },
};
</script>
<style lang=""></style>
