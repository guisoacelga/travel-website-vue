<template>
  <header>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <div class="container">
        <button
          class="navbar-toggler"
          type="button"
          data-toggle="collapse"
          data-target="#navbarTogglerDemo03"
          aria-controls="navbarTogglerDemo03"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <router-link class="navbar-brand" to="/">Let's Travel</router-link>
        <div class="collapse navbar-collapse" id="navbarTogglerDemo03">
          <ul class="navbar-nav mr-auto mt-2 mt-lg-0">
            <li :class="[currentPage.includes('/Home') ? 'active' : '', 'nav-item']">
              <router-link class="nav-link" to="/">Home</router-link>
            </li>
            <li :class="[currentPage.includes('AboutUs') ? 'active' : '', 'nav-item']">
              <router-link class="nav-link" to="/AboutUs">About Us</router-link>
            </li>
            <li :class="[currentPage.includes('ContactUs') ? 'active' : '', 'nav-item']">
              <router-link class="nav-link" to="/ContactUs">Contacts</router-link>
            </li>
          </ul>
          <form :class="[currentPage.includes('/Home') ? 'form-inline my-2 my-lg-0' : 'd-none']">
            <input
              v-on:input="$emit('input', $event.target.value)"
              class="form-control mr-sm-2"
              type="search"
              placeholder="Destination"
              aria-label="Search"
            />
          </form>
        </div>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
  computed: {
    currentPage() {
      return this.$route.path;
    }
  }
};
</script>