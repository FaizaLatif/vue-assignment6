<template>
  <form @submit.prevent="submitData">
  <div>
    <label>Name</label>
    <input type="text" v-model="name" />
  </div>
  <div>
    <label>Age</label>
    <input type="number" v-model="age" />
  </div>
    <button >Set User Data</button>

    <!-- <button @click="submitData">Set User Data</button> -->
  </form>
</template>
<script>
export default {
  emits: ['user-data'],
  data() {
    return {
        name: '',
        age: 0,
    }
  },
  methods: {
    submitData() {
      this.$emit('user-data', this.name, this.age)
    }
  }
};
</script>
