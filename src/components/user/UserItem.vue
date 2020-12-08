<template>
  <div>
    <p>Id: {{ id }}</p>
    <p>FullName: {{ fullName }}</p>
    <p>Age: {{ age }}</p>
    <button @click="removeUser">Remove User</button>
  </div>
</template>

<script>
export default {
  emits: ['delete-user'],
  computed: {
    fullName() {
      return `${this.firstName} ${this.lastName}`;
    },
  },
  props: {
    id: { type: Number, required: true },
    firstName: { type: String, required: true },
    lastName: { type: String, required: true },
    age: { type: Number, required: true },
  },
  methods: {
    removeUser() {
      this.$emit('delete-user', this.id);
    },
  },
};
</script>

<style scoped>
div {
  border-radius: 20px;
  border: 1px solid grey;
  margin: 2rem;
}
button {
  background-color: rgb(241, 154, 154);
  color: white;
  font-weight: bold;
}
</style>