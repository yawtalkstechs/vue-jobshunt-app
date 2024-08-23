<script>
export default {
    data() {
      return {
        name: "JoHn Noah",
        status: "pending",
        fruits: ["Apple", "Banana", "Orange"],
        urls: "https://www.google.com"
      };
    },
    methods: {
      toggleStatus() {
        if (this.status === 'active'){
          this.status = 'pending';
        }
        else if (this.status === 'pending'){
          this.status = 'inactive'
        }
        else {
          this.status = 'active'
        }
      }
    }
}
</script>

<template>
  <h1>{{ name }}</h1>
  <p v-if="status==='active'">User is active</p>
  <p v-else-if="status==='pending'">User is pending</p>
  <p v-else>User is inactive</p>

  <h3>Fruits: </h3>
  <ul>
    <li v-for="fruit in fruits" :key="fruit">{{ fruit }}</li>
  </ul>
  <a :href="link">Google</a>

  <button @click="toggleStatus">Change status</button>
</template>
