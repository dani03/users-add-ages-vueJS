<template>
  <div class="card col-md-3 m-3" style="width: 200px">
    <div class="card-body">
      <h4 class="card-title">{{ name }}</h4>
      <p class="card-text">{{ age }} ans</p>
    </div>
  </div>
</template>

<script>
export default {
  props: ["age", "name"],
  data() {
    return {};
  },
};
</script>

<style></style>
