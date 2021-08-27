<template>
  <div class="container">
    <p>You are not logged in</p>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  data() {
    return {
      message: ""
    };
  },
  async mounted() {
    const response = await fetch("http://localhost:8000/api/user", {
      headers: { "Content-Type": "application/json" },
      credentials: "include"
    });

    const content = await response.json();
    console.log(content);
  }
});
</script>

<style>
.form-signin {
  width: 100%;
  max-width: 330px;
  padding: 15px;
  margin: auto;
}

.form-signin .checkbox {
  font-weight: 400;
}

.form-signin .form-floating:focus-within {
  z-index: 2;
}

.form-signin input[type="email"] {
  margin-bottom: -1px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}

.form-signin input[type="password"] {
  margin-bottom: 10px;
  border-top-left-radius: 0;
  border-top-right-radius: 0;
}
</style>
