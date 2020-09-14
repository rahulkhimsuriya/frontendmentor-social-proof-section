<template>
  <div class="review">
    <div class="review__star">
      <Star
        v-for="(star, index) in review.star"
        :key="index"
        :style="`margin-right:0.5rem;`"
      />
    </div>
    <p class="review__body">{{ review.body }}</p>
  </div>
</template>

<script>
import Star from './Star.vue';

export default {
  name: 'Review',

  props: {
    review: {
      required: true
    }
  },

  components: {
    Star
  },

  data() {
    return {};
  }
};
</script>

<style lang="css" scoped>
.review {
  display: flex;
  align-items: center;
  background-color: hsl(300, 24%, 96%);
  border-radius: 0.5rem;
  padding: 1rem 1.5rem;
  width: 25rem;
  margin-top: 1rem;
}

.review__star {
}

.review__body {
  color: hsl(300, 43%, 22%);
  font-size: 0.8rem;
  font-weight: 700;
  margin-left: 1rem;
}
</style>
