<template>
  <form @submit.prevent="submitData">
    <div>
      <label for="name">Name</label>
      <input type="text" placeholder="Your name" v-model="enteredName">
    </div>
    <div>
      <label for="age">Age</label>
      <input type="number" placeholder="Your age" v-model="enteredAge">
    </div>
    <div>
      <button>Add User</button>
    </div>
  </form>
</template>

<script>
export default {
  emits: ['add-user'],
  data() {
    return {
      enteredName: '',
      enteredAge: ''
    }
  },
  methods: {
    submitData() {
      this.$emit(
      'add-user',
      this.enteredName,
      this.enteredAge
      );
    }
  }
}
</script>