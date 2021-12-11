<template>
  <div class="container py-3 d-flex flex-column">
    <the-header />

    <section class="mt-3"></section>

    <router-view></router-view>

    <section class="mb-3"></section>

    <the-footer />
  </div>
</template>

<script>
import TheHeader from "./components/TheHeader.vue";
import TheFooter from "./components/TheFooter.vue";

export default {
  name: "App",
  components: {
    TheHeader,
    TheFooter,
  },
};
</script>

<style lang="scss">
// 1. Include functions first (so you can manipulate colors, SVGs, calc, etc)
@import "~bootstrap/scss/functions"; // Required

// 2. Include any default variable overrides here

// $primary: white;

// 3. Include remainder of required Bootstrap stylesheets
@import "~bootstrap/scss/variables"; // Required
@import "~bootstrap/scss/mixins"; // Required
@import "~bootstrap/scss/utilities";

// 4. Include any optional Bootstrap components as you like
@import "~bootstrap/scss/root";
@import "~bootstrap/scss/reboot";
@import "~bootstrap/scss/type";
@import "~bootstrap/scss/images";
@import "~bootstrap/scss/containers";
@import "~bootstrap/scss/grid";
// @import "~bootstrap/scss/tables";
@import "~bootstrap/scss/forms";
@import "~bootstrap/scss/buttons";
@import "~bootstrap/scss/transitions";
// @import "~bootstrap/scss/dropdown";
// @import "~bootstrap/scss/button-group";
@import "~bootstrap/scss/nav";
@import "~bootstrap/scss/navbar";
@import "~bootstrap/scss/card";
// @import "~bootstrap/scss/accordion";
// @import "~bootstrap/scss/breadcrumb";
// @import "~bootstrap/scss/pagination";
// @import "~bootstrap/scss/badge";
// @import "~bootstrap/scss/alert";
// @import "~bootstrap/scss/progress";
// @import "~bootstrap/scss/list-group";
// @import "~bootstrap/scss/close";
// @import "~bootstrap/scss/toasts";
@import "~bootstrap/scss/modal";
// @import "~bootstrap/scss/tooltip";
// @import "~bootstrap/scss/popover";
// @import "~bootstrap/scss/carousel";
@import "~bootstrap/scss/spinners";
// @import "~bootstrap/scss/offcanvas";

// Helpers
@import "~bootstrap/scss/helpers";

// Utilities
@import "~bootstrap/scss/utilities/api";
// scss-docs-end import-stack

// 5. Add additional custom code here
html,
body {
  height: 100%;
  background-color: #333;
}

body {
  display: flex;
  justify-content: center;
  color: #fff;
  text-shadow: 0 0.05rem 0.1rem rgba(0, 0, 0, 0.5);
  box-shadow: inset 0 0 5rem rgba(0, 0, 0, 0.5);
}

/* Links */
a,
a:focus,
a:hover {
  color: #fff;
}

/* Buttons */
.btn-secondary,
.btn-secondary:hover,
.btn-secondary:focus {
  color: #333;
  text-shadow: none; /* Prevent inheritance from `body` */
  background-color: #fff;
  border: 0.05rem solid #fff;
}

.btn-lg {
  padding: 0.75rem 1.25rem;
  font-weight: 700;
}
</style>
