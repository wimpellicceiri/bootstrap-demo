<template>
  <section>
    <div class="card mb-4" :id="id">
      <a href="#" data-bs-toggle="modal" :data-bs-target="`#${id}-modal`">
        <img
          class="card-img-top img-fluid"
          alt="Thumbnail"
          :src="item.imgSrc"
        />
      </a>
      <div class="card-body">
        <p class="card-text">{{ item.text }}</p>
        <div class="d-flex justify-content-between align-items-center">
          <button type="button" class="btn btn-sm btn-outline-secondary">
            View Gallery
          </button>
          <small class="text-muted">{{ item.gallerySize }} photos</small>
        </div>
      </div>
    </div>

    <aside
      class="modal fade"
      :id="`${id}-modal`"
      tabindex="-1"
      aria-hidden="true"
    >
      <div class="modal-dialog modal-lg">
        <div class="modal-content">
          <div class="modal-body">
            <img
              class="card-img-top img-fluid"
              alt="Thumbnail"
              :src="item.imgSrc"
            />
          </div>
        </div>
      </div>
    </aside>
  </section>
</template>

<script>
export default {
  props: {
    id: {
      type: String,
      required: true,
    },
    item: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style scoped>
.card {
  text-shadow: 0 0 black;
}
.card-text {
  color: #000;
}
</style>
