<template>
  <div class="home">
    <div class="inputs">
      <label>First Name:</label>
      <input v-model="firstName" />
      <label>Last Name:</label>
      <input v-model="lastName" />
    </div>
    <h1>Hello<span v-if="firstName || lastName">, {{ fullName }}</span>!</h1>
    <h2>Welcome to VueJs</h2>
  </div>
</template>

<script>

export default {
  name: 'Home',
  components: {
  },
  data(){
    return {
      firstName: null,
      lastName: null,
    };
  },
  computed: {
    fullName() {
      if (this.firstName && !this.lastName) {
        return this.firstName;
      } else if (this.lastName && !this.firstName) {
        return this.lastName;
      }
      return `${this.firstName} ${this.lastName}`
    }
  }
}
</script>

<style lang="sass">
.home
  display: flex
  flex-direction: column
  justify-content: center
  align-items: center
  .inputs
    display: flex
    flex-direction: column
    justify-content: flex-start
    align-items: flex-start
    input
      margin: 0 0 12px 0  
</style>
