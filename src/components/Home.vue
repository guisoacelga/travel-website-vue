<template>
  <div>
    <Slider />
    <!-- ****** Cards ***** -->
    <div class="row mt-20">
      <Card
        v-for="card in filteredCards"
        :key="card.id"
        :image="card.image"
        :title="card.title"
        :text="card.text"
      />
    </div>
  </div>
</template>

<script>
import Slider from "./Slider.vue";
import Card from "./Card.vue";
export default {
  name: "Home",
  components: {
    Slider,
    Card
  },
  props: {
    searchText: {
      type: String
    }
  },
  data: function() {
    return {
      cards: [
        {
          id: 1,
          image: "img-1.jpg",
          title: "Eiffel Tower",
          text:
            "The Eiffel Tower is a wrought iron lattice tower on the Champ de Mars in Paris, France."
        },
        {
          id: 2,
          image: "img-2.jpg",
          title: "Big Ben",
          text:
            "Big Ben is the nickname for the Great Bell of the clock at the north end of the Palace of Westminster in London."
        },
        {
          id: 3,
          image: "img-3.jpg",
          title: "Statue of Liberty",
          text:
            "The Statue of Liberty is a colossal neoclassical sculpture on Liberty Island in New York Harbor in New York City, in the United States."
        },
        {
          id: 4,
          image: "img-4.jpg",
          title: "Sydney Opera House",
          text:
            "The Sydney Opera House is a multi-venue performing arts centre in Sydney, Australia. It is one of the 20th century's most famous and distinctive buildings."
        },
        {
          id: 5,
          image: "img-5.jpg",
          title: "Parliament Hill",
          text:
            "Parliament Hill, colloquially known as The Hill, is an area of Crown land on the southern banks of the Ottawa River in downtown Ottawa, Ontario."
        },
        {
          id: 6,
          image: "img-6.jpg",
          title: "Great Wall of China",
          text:
            "The Great Wall of China is a series of fortifications made of stone, brick, rammed earth, wood, and other materials, generally built to protect the Chinese states and empires against the raids and invasions."
        }
      ]
    };
  },
  computed: {
    filteredCards() {
      if (this.searchText === "") {
        return this.cards;
      }
      return this.cards.filter(card => {
        return (
          card.title.toLowerCase().includes(this.searchText.toLowerCase()) ||
          card.text.toLowerCase().includes(this.searchText.toLowerCase())
        );
      });
    }
  }
};
</script>
