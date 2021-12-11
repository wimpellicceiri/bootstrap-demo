<template>
  <header class="mb-auto sticky-top">
    <nav class="navbar navbar-dark navbar-expand-sm">
      <div class="container-fluid">
        <router-link
          class="navbar-brand"
          :class="{ active: $route.name === 'Home' }"
          :to="{ name: 'Home' }"
          ><img
            width="50"
            src="https://coursereport-s3-production.global.ssl.fastly.net/uploads/school/logo/259/original/mark.png"
        /></router-link>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarLinks"
          aria-controls="navbarLinks"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarLinks">
          <div class="navbar-nav fw-bolder text-end">
            <router-link
              class="nav-link"
              :class="{ active: $route.name === 'Home' }"
              :to="{ name: 'Home' }"
              >Home</router-link
            >
            <router-link
              class="nav-link"
              :class="{ active: $route.name === 'Portfolio' }"
              :to="{ name: 'Portfolio' }"
              >Portfolio</router-link
            >
            <router-link
              class="nav-link"
              :class="{ active: $route.name === 'Contact' }"
              :to="{ name: 'Contact' }"
              >Contact</router-link
            >
          </div>
        </div>
      </div>
    </nav>
  </header>
</template>
