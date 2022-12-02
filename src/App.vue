<template lang="">
  <div class="container">
    <user-data v-on:emit-user-data="getUserData" />
    <div id="list" class="d-flex justify-content-evenly flex-wrap">
      <active-user
        v-for="user in users"
        :key="user.name"
        :name="user.name"
        :age="user.age"
      />
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      users: [],
    };
  },
  methods: {
    getUserData(ageUser, nameUser) {
      console.log(ageUser, nameUser);
      this.user = { name: nameUser, age: ageUser };
      this.users.push(this.user);
    },
  },
};
</script>
<style lang="">

</style>
