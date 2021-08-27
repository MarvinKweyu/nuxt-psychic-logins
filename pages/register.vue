<template>
  <form @submit.prevent="submit">
    <h1 class="h3 mb-3 fw-normal">Please register</h1>
    <div class="form-floating mb-2">
      <input
        v-model="name"
        type="text"
        class="form-control"
        placeholder="Name"
        required
      />
    </div>

    <div class="form-floating mb-2">
      <input
        v-model="email"
        type="email"
        class="form-control"
        placeholder="name@example.com"
        required
      />
    </div>
    <div class="form-floating mb-2">
      <input
        v-model="password"
        type="password"
        class="form-control"
        placeholder="Password"
        required
      />
    </div>
    <button class="w-100 btn btn-lg btn-primary" type="submit">
      Submit
    </button>
  </form>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  data() {
    return {
      name: "",
      email: "",
      password: ""
    };
  },
  methods: {
    async submit() {
      await fetch("http://localhost:8000/api/register", {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({
          nae: this.name,
          email: this.email,
          password: this.password
        })
      });

      await this.$router.push("/login");
    }
  }
});
</script>
