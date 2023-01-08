<template>
  <div class="reviews container" id="reviews">
    <h2 class="reviews__title">отзывы наших клиентов</h2>
    <div class="reviews__block">
      <div class="reviews__item" v-for="review in data" :key="review.id">
        <div class="reviews__item_img">
          <img
            :src="require(`../assets/images/reviews/${review.image}.png`)"
            :alt="review.title"
          />
        </div>
        <div class="reviews__item_info">
          <div class="reviews__item_title">
            <p>{{ review.title }}</p>
          </div>
          <div class="reviews__item_text">
            <p>{{ review.text }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
    props: {
        data: {
            type: Array,
            default: () => [],
        },
    },
}
</script>
