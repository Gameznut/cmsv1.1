<template>
  <div class="relative">
    <h2 class="categories_heading">Categories</h2>
    <div class="categories_contents">
      <div class="section">
        <img src="" alt="" />
        <small>Salads</small>
      </div>
      <div class="section">
        <img src="" alt="" />
        <small>Salads</small>
      </div>
      <div class="section">
        <img src="" alt="" />
        <small>Salads</small>
      </div>
      <div class="section">
        <img src="" alt="" />
        <small>Salads</small>
      </div>
      <div class="section">
        <img src="" alt="" />
        <small>Salads</small>
      </div>
      <div class="section">
        <img src="" alt="" />
        <small>Salads</small>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.categories_heading {
  position: absolute;
  top: -0.75rem;
  font-size: 14px;
  left: 50%;
  /* right: 50%; */
  background-color: rgb(255, 255, 255);
  padding: 0 1rem;
  z-index: 300;
  transform: translateX(-50%);
}
.categories_contents {
  border: 1px solid black;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  padding: 1.3rem;
}
.section:nth-child(1),
.section:nth-child(3),
.section:nth-child(4) {
  background-color: rgb(230, 126, 126);
}
.section:nth-child(2),
.section:nth-child(5),
.section:nth-child(6) {
  background-color: rgb(230, 185, 126);
}

.section {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100px;
}

@media screen and (max-width: 768px) {
  .categories_contents {
    border: 1px solid black;
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    padding: 1rem;
  }
}


/* @media screen and (max-width: 520px) {
  .categories_contents {
    border: 1px solid black;
    display: grid;
    grid-template-columns: repeat(1, 1fr);
    padding: 1rem;
  }
} */
</style>