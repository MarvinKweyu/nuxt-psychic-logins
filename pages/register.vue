<template>
  <form>
    <h1 class="h3 mb-3 fw-normal">Please register</h1>
    <div class="form-floating mb-2">
      <input type="text" class="form-control" placeholder="Name" required />
    </div>

    <div class="form-floating mb-2">
      <input
        type="email"
        class="form-control"
        placeholder="name@example.com"
        required
      />
    </div>
    <div class="form-floating mb-2">
      <input
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

export default Vue.extend({});
</script>
