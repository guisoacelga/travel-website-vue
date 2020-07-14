<template>
  <div class="col-12 col-lg-4 col-sm-6">
    <div class="card mb-4 shadow-lg">
      <img class="card-img-top" :src="imageSrc" alt="Card image" />
      <div class="card-body">
        <h4 class="card-title">{{ title }}</h4>
        <p
          class="card-text"
        >
        {{ text }}</p>
        <button class="btn btn-primary">Details</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    image: String,
    title: String,
    text: String
  },
  data() {
    return {
      imageSrc: require('@/assets/images/' + this.image)
    };
  }
};
</script>