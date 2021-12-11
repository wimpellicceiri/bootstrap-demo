<template>
  <main>
    <div v-if="success" class="m-auto">Thank you for your message.</div>
    <div v-else-if="sending" class="m-auto">
      <div class="spinner-border text-light" role="status">
        <span class="visually-hidden">Sending...</span>
      </div>
    </div>
    <div v-else class="row container-fluid m-auto">
      <div class="col-md-8 col-lg-6 m-auto">
        <h4 class="mb-3">Send me a line...</h4>

        <form novalidate="true" v-on:submit="submit">
          <div class="row">
            <div class="col-md-6 mb-3">
              <label for="firstName">
                First name <span class="text-muted">(Optional)</span>
              </label>
              <input type="text" class="form-control" id="firstName" />
            </div>

            <div class="col-md-6 mb-3">
              <label for="lastName">
                Last name <span class="text-muted">(Optional)</span>
              </label>
              <input type="text" class="form-control" id="lastName" />
            </div>
          </div>

          <div class="mb-3">
            <label for="email">Email</label>
            <input
              type="email"
              class="form-control"
              id="email"
              placeholder="you@example.com"
              required
              pattern="[a-zA-Z0-9_.+-]+@[a-zA-Z0-9-]+.[a-zA-Z0-9-.]+"
            />
            <div class="invalid-feedback">
              Please enter a valid email address.
            </div>
          </div>

          <div class="mb-3">
            <label for="subject">Subject</label>
            <input type="text" class="form-control" id="subject" required />
            <div class="invalid-feedback">Please enter your subject.</div>
          </div>

          <div class="mb-3">
            <label for="subject">Message</label>
            <textarea type="text" class="form-control" id="message" required>
            </textarea>
            <div class="invalid-feedback">Please enter your message.</div>
          </div>

          <hr class="mb-3" />

          <button class="mx-2 btn btn-primary btn-lg float-end" type="submit">
            Send
          </button>
        </form>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  data() {
    return {
      sending: false,
      success: false,
    };
  },
  methods: {
    submit(event) {
      const form = event.currentTarget;
      form.classList.add("was-validated");

      if (!form.checkValidity()) {
        event.preventDefault();
        return;
      }

      this.sending = true;

      setTimeout(() => {
        this.success = true;
        this.sending = false;
        form.reset();
      }, 1000); // Artificial delay for effect.
    },
  },
};
</script>
