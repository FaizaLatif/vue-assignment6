<template>
  <div>
    <active-user :name="user.name" :age="user.age"></active-user>
    <user-data @user-data="updateUserData"></user-data>
  </div>
</template>
<script>
export default {
  data() {
    return {
      user: {
        name: 'faiza latif',
        age: 25
      }
    }
  },
  methods: {
    updateUserData(name, age) {
      this.user = {
        name,
        age
      }
    }
  }
};
</script>
