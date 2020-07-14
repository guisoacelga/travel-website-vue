<template>
  <div id="carouselExampleIndicators" class="carousel slide mt-20" data-ride="carousel">
          <ol class="carousel-indicators">
            <li data-target="#carouselExampleIndicators" data-slide-to="0" class="active"></li>
            <li data-target="#carouselExampleIndicators" data-slide-to="1"></li>
            <li data-target="#carouselExampleIndicators" data-slide-to="2"></li>
          </ol>
          <div class="carousel-inner">
            <div class="carousel-item active">
              <img class="d-block w-100" src="@/assets/images/slider-1.jpg" alt="First slide" />
              <div class="carousel-caption d-none d-md-block">
                <h5>Golden Gate Bridge</h5>
                <p>San Francisco, U.S.</p>
              </div>
            </div>
            <div class="carousel-item">
              <img class="d-block w-100" src="@/assets/images/slider-2.jpg" alt="Second slide" />
              <div class="carousel-caption d-none d-md-block">
                <h5>Niagara Falls</h5>
                <p>Border of Ontario, Canada, and New York, United States</p>
              </div>
            </div>
            <div class="carousel-item">
              <img class="d-block w-100" src="@/assets/images/slider-3.jpg" alt="Third slide" />
              <div class="carousel-caption d-none d-md-block">
                <h5>Stonehenge</h5>
                <p>Wiltshire, England</p>
              </div>
            </div>
          </div>
          <a
            class="carousel-control-prev"
            href="#carouselExampleIndicators"
            role="button"
            data-slide="prev"
          >
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="sr-only">Previous</span>
          </a>
          <a
            class="carousel-control-next"
            href="#carouselExampleIndicators"
            role="button"
            data-slide="next"
          >
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="sr-only">Next</span>
          </a>
        </div>
</template>

<script>
export default {
  name: "Slider"
};
</script>
