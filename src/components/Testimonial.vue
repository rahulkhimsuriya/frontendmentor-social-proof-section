<template>
  <div class="testimonial">
    <div class="testimonial__header">
      <img
        class="testimonial__header--image"
        :src="testimonial.image"
        :alt="testimonial.name"
      />

      <div class="testimonial__header--user">
        <h3>{{ testimonial.name }}</h3>
        <p>{{ testimonial.type }}</p>
      </div>
    </div>

    <div class="testimonial__body">
      <p>"{{ testimonial.body }}"</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Testimonial',

  props: ['testimonial'],

  data() {
    return {};
  }
};
</script>

<style lang="css" scoped>
.testimonial {
  background-color: hsl(300, 43%, 22%);
  border-radius: 0.5rem;
  color: hsl(300, 24%, 96%);
  padding: 2rem;
  width: 22rem;
}

.testimonial__header {
  display: flex;
  align-items: center;
}

.testimonial__header--image {
  height: 3rem;
  width: 3rem;
  border-radius: 50px;
  margin-right: 1.5rem;
}

.testimonial__header--user {
  font-size: 0.9rem;
}

.testimonial__header--user > h3 {
  font-weight: 500;
  margin-bottom: 5px;
}

.testimonial__header--user > p {
  color: hsl(333, 80%, 67%);
}

.testimonial__body {
  margin-top: 2rem;
}

.testimonial__body > p {
  line-height: 25px;
}
</style>
