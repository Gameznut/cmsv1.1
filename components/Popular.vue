<template>
  <div>
    <div class="popular relative">
      <h1 class="heading">
        <span><font-awesome-icon icon="fa-solid fa-bolt-lightning" /></span>
        popular
      </h1>
      <Card2 class="test" />
      <Card2 class="test" />
      <Card2 class="test" />
    </div>
  </div>
</template>

    <style scoped>

.popular {
  grid-template-columns: repeat(3, 1fr);
  display: grid;
  gap: 1.5rem;
  max-width: 1100px;
  margin: 0 auto;
}
.heading {
  display: flex;
  text-transform: uppercase;
  background-color: gold;
  gap: 0.8rem;
  padding: 0.7rem;
  font-size: 17px;
  font-weight: 500;
  width: max-content;
  position: absolute;
  z-index: 30;
}

@media screen and (max-width: 768px) {
  .popular {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 1rem;
  }
  .test:nth-child(3) {
    display: none;
  }
}

@media screen and (max-width: 425px) {
  .popular {
    display: grid;
    grid-template-columns: repeat(1, 1fr);
    gap: 1rem;
  }
  .test:nth-child(3) {
    display: block;
  }
}
</style>