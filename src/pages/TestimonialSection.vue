<template>
  <section class="container testimonial-section">
    <Testimonial
      v-for="(testimonial, index) in testimonials"
      :key="index"
      :testimonial="testimonial"
      :class="`lg:mt-${(index + 1) * 2}`"
    />
  </section>
</template>

<script>
import Testimonial from '@/components/Testimonial.vue';

export default {
  name: 'TestimonialSection',

  components: {
    Testimonial
  },

  data() {
    return {
      testimonials: [
        {
          image: require('../assets/images/image-colton.jpg'),
          name: 'Colton Smith',
          type: 'Verified Buyer',
          body:
            'We needed the same printed design as the one we had ordered a week prior.Not only did they find the original order, but we also received it in time. Excellent!'
        },
        {
          image: require('../assets/images/image-irene.jpg'),
          name: 'Irene Roberts',
          type: 'Verified Buyer',
          body:
            'Customer service is always excellent and very quick turn around. Completely delighted with the simplicity of the purchase and the speed of delivery.'
        },
        {
          image: require('../assets/images/image-anne.jpg'),
          name: 'Anne Wallace',
          type: 'Verified Buyer',
          body:
            'Put an order with this company and can only praise them for the very high standard. Will definitely use them again and recommend them to everyone!'
        }
      ]
    };
  }
};
</script>

<style lang="css" scoped>
.testimonial-section {
  padding: 2rem 0;
}

@media only screen and (min-width: 1080px) {
  .lg\:mt-2 {
    margin-top: 2rem;
  }

  .lg\:mt-4 {
    margin-top: 4rem;
  }

  .lg\:mt-6 {
    margin-top: 6rem;
  }
}
</style>
