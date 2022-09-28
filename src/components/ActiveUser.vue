<template>
  <div>
    <h2>Name: {{ name }}</h2>
    <h3>Age: {{ age }}</h3>
  </div>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      require: true
    },
    age: {
      type: Number,
      requiresd: true
    }
  },
  data() {
    return {
      hello: 'This is component!'
    }
  }
}
</script>