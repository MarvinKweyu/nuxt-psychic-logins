<template>
  <div>
    <nav class="navbar navbar-expand-md navbar-dark bg-dark mb-4">
      <div class="container-fluid">
        <NuxtLink to="/" class="navbar-brand">Home</NuxtLink>

        <div>
          <ul class="navbar-nav me-auto mb-2 mb-md-0">
            <li class="nav-item">
              <NuxtLink to="/login" class="nav-link active">Login</NuxtLink>
            </li>

            <li class="nav-item">
              <NuxtLink to="/register" class="nav-link" aria-current="page"
                >Register</NuxtLink
              >
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <main class="form-signin">
      <Nuxt />
    </main>
  </div>
</template>

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
