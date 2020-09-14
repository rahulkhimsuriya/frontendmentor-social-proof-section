<template>
  <section class="container hero-section">
    <div>
      <h1>
        10,000+ of our <br />
        users love our <br />
        products.
      </h1>
      <p>
        We only provide great products combined with excellent customer service.
        See what our satisfied customers are saying about our services.
      </p>
    </div>
    <div>
      <Review
        v-for="(review, index) in reviews"
        :key="index"
        :review="review"
        :class="`lg:ml-${(index + 1) * 2}`"
      />
    </div>
  </section>
</template>

<script>
import Review from '@/components/Review.vue';

export default {
  name: 'HeroSection',

  components: {
    Review
  },

  data() {
    return {
      reviews: [
        {
          star: 5,
          body: 'Rated 5 Stars in Reviews'
        },
        {
          star: 5,
          body: 'Rated 5 Stars in Report Guru'
        },
        {
          star: 5,
          body: 'Rated 5 Stars in BestTech'
        }
      ]
    };
  }
};
</script>

<style lang="css" scoped>
.hero-section {
  padding-top: 4rem;
}

h1 {
  color: hsl(300, 43%, 22%);
  font-size: 2.5rem;
  font-weight: 700;
}

p {
  color: hsl(303, 10%, 53%);
  font-size: 1rem;
  margin-top: 1rem;
  width: 70%;
}

@media only screen and (min-width: 992px) {
  .lg\:ml-2 {
    margin-left: 2rem;
  }

  .lg\:ml-4 {
    margin-left: 4rem;
  }

  .lg\:ml-6 {
    margin-left: 6rem;
  }
}

@media screen and (max-width: 1020px) {
  .hero-section {
    text-align: center;
  }

  p {
    width: 100%;
  }
}
</style>
