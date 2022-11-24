<template>
  <div class="card">
    <div class="card__image">
      <img :src="props.image" alt="coffee" />
    </div>
    <div class="card__content">
      <h2 class="card__title">{{ props.name }}</h2>
      <p class="card__price">{{ props.price }}</p>
      <p blabla>{{ props.isCold ? "Cold" : "Hot" }}</p>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  name: String,
  price: Number,
  image: String,
  isCold: Boolean,
});
</script>

<style scoped>
.card {
  width: 300px;
  height: 400px;
  background-color: #fff;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  overflow: hidden;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
  margin: 20px;
}

.card__image {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.card__image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.card__content {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
}

.card__title {
  font-size: 1.5rem;
  font-weight: 500;
  text-align: center;
}

.card__price {
  font-size: 1.2rem;
  font-weight: 500;
  text-align: center;
}

.card__isCold {
  font-size: 1.2rem;
  font-weight: 500;
  text-align: center;
}
</style>
