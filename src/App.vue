<template>
  <section>
    <header>
      <h1>My assignment of Vue Component!</h1>
    </header>
    <user-data @add-user="addUser"></user-data>
    <active-user
      v-for="user in users"
      :key="user.username"
      :name="user.username"
      :age="user.age"
    ></active-user>
  </section>
</template>

<script>
export default {
  data() {
    return {
      users: [
        {
          username: 'Daniel Jordan',
          age: '27'
        },
        {
          username: 'Ariel Jockson',
          age: '33'
        }
      ]
    };
  },
  methods: {
    addUser(name, age) {
      const newUser = {
        username: name,
        age: age
      };
      this.users.push(newUser);
    }
  }
}
</script>