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
        :style="{ 'margin-left': index * 2 + 'rem' }"
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
  padding-bottom: 1rem;
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
</style>
