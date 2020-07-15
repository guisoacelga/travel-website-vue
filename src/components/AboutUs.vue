<template>
  <div>
    <section class="intro">
      <div>
        <h1>Love your destination</h1>
      </div>
    </section>
    <section class="about">
      <div class="row">
        <div class="col-12 col-lg-6 mt-5">
          <img class="img-fluid" src="@/assets/images/johanna-about.jpg" alt="Johanna Rojas" />
        </div>
        <div class="col-12 col-lg-6 mt-5">
          <h2 class="about-title">Meet Johanna Rojas, founder of Let's Travel</h2>
          <p>
            Welcome to your number one source for booking holiday packages.
            We're dedicated to giving you the very best of the travel experience.
            Founded in 2009, Let's Travel has come a long way from its beginnings in a home office in Santiago, Chile.
          </p>
          <p>
            When Johanna first started out, her passion for providing the best holiday experience drove her to quit her day job, and gave her the impetus to turn hard work and inspiration into to a booming online travel agency.
            We now serve customers all over Latin America, and are thrilled to be a part of the eco-friendly wing of the travel industry.
            We hope you enjoy our carfeully selected tours as much as we enjoy offering them to you. If you have any questions or comments, please don't hesitate to contact us.
          </p>
          <p>
            Sincerely,
            Let's Travel Team
          </p>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "AboutUs"
};
</script>

<style scoped>
.intro {
  background-image: url("../assets/images/img_About.jpg");
  background-size: cover;
  background-position: center;
  height: 50vh;
  display: flex;
  justify-content: center;
  align-items: top;
}
h1 {
  font-size: 4rem;
  font-weight: 500;
  color: white;
  margin-top: 170px;
  text-shadow: 2px 2px gray;
}
@media only screen and (max-width: 576px) {
  h1 {
    font-size: 2.75rem;
    margin-top: 60px;
  }
}

p {
  display: block;
  text-align: justify;
}

</style>