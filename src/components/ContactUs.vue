<template>
  <div>
    <section class="intro">
      <div>
        <h1>We want to hear from you</h1>
      </div>
    </section>
    <section class="contact">
      <div class="row">
        <div class="col-12 col-lg-6 mt-5">
          <form class="mr-5">
            <div class="form-group">
              <label for="exampleFormControlInput1">Your Name</label>
              <input
                type="text"
                class="form-control"
                id="exampleFormControlInput1"
                placeholder="Name"
                required
              />
            </div>
            <div class="form-group">
              <label for="exampleFormControlInput1">Your Phone Number</label>
              <input
                type="text"
                class="form-control"
                id="exampleFormControlInput1"
                placeholder="Phone Number"
              />
            </div>

            <div class="form-group">
              <label for="exampleFormControlInput1">Email address</label>
              <input
                type="email"
                class="form-control"
                id="exampleFormControlInput1"
                placeholder="name@example.com"
                required
              />
            </div>

            <div class="form-group">
              <label for="exampleFormControlTextarea1">Your Message</label>
              <textarea class="form-control" id="exampleFormControlTextarea1" rows="3" required></textarea>
            </div>
            <button type="submit" class="btn btn-primary">Send</button>
          </form>
        </div>

        <div class="col-12 col-lg-6 mt-5">
          <p id="about-title">
            <i class="fas fa-phone fa-1x iconContact"></i> Call customer service
          </p>
          <div class="form-group">
            <label for="exampleFormControlSelect2" class="about-subtitle">Choose your country</label>
            <select v-model="selected" class="form-control" id="exampleFormControlSelect2">
              <option
                v-for="country in countries"
                :key="country.name"
                :selected="country.name === 'Chile'"
                :value="country.name"
              >{{country.name}}</option>
            </select>
            <h4 class="mt-3">{{currentCountryNumber}}</h4>
          </div>
        </div>
      </div>
    </section>
    <section></section>
  </div>
</template>

<script>
export default {
  name: "ContactUs",
  data: function() {
    return {
      selected: "Chile",
      countries: [
        { name: "Argentina", number: "+54 544235874" },
        { name: "Australia", number: "+61 25479651" },
        { name: "Austria", number: "+43 85554784" },
        { name: "Bolivia", number: "+591 66985478" },
        { name: "Brazil", number: "+55 36966585" },
        { name: "Chile", number: "+56 4474521452" },
        { name: "United States", number: "+01 8878935582" },
        { name: "Uruguay", number: "+598 66458444747" },
        { name: "Other countries", number: "+01 5555555754" }
      ]
    };
  },
  computed: {
    currentCountryNumber() {
      const selectedCountry = this.selected;
      const countriesFiltered = this.countries.filter(country => {
        return selectedCountry === country.name;
      });

      return countriesFiltered[0].number;
    }
  }
};
</script>

<style scoped>
.intro {
  background-image: url("../assets/images/img_Contact.jpg");
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
#about-title {
  font-weight: 550;
  margin-bottom: 16px;
}
.about-subtitle {
  font-size: 15px;
}

@media only screen and (max-width: 576px) {
  h1 {
    font-size: 2.75rem;
    margin-top: 60px;
  }
}
</style>