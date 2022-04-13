<template>
  <client-only>
    <div class="relative">
      <h2 class="latest_heading">Latest Posts</h2>
      <div class="latest_contents">
        <div class="section">
          <img src="../assets/images/food.jpg" alt="" />
          <div>
            <span
              ><font-awesome-icon icon="fa-solid fa-calendar" /> Feb 20
              2022</span
            >
            <small>Life is combination of magic and pasta.</small>
          </div>
        </div>
        <div class="section">
          <img src="../assets/images/food.jpg" alt="" />
          <div>
            <span
              ><font-awesome-icon icon="fa-solid fa-calendar" /> Feb 20
              2022</span
            >
            <small>Life is combination of magic and pasta.</small>
          </div>
        </div>
        <div class="section">
          <img src="../assets/images/food.jpg" alt="" />
          <div>
            <span
              ><font-awesome-icon icon="fa-solid fa-calendar" /> Feb 20
              2022</span
            >
            <small>Life is combination of magic and pasta.</small>
          </div>
        </div>
      </div>
    </div>
  </client-only>
</template>

<script>
export default {};
</script>

<style scoped>
.latest_heading {
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
.latest_contents {
  border: 1px solid black;
  display: grid;
  grid-template-columns: repeat(1, 1fr);
  padding: 1.3rem;
  gap: 1rem;
}
.section {
  display: flex;
  align-items: center;
  gap: 1rem;
  height: 100px;
  transition: 0.4s;
}

.section small {
  display: block;
  font-size: 16px;
  color: black;
  font-weight: 500;
}
.section span {
  font-size: 13px;
  color: gray;
}

.section img {
  object-fit: cover;
  max-width: 150px;
  width: 100%;
  height: 100%;
}

@media screen and (max-width: 1070px) {
  .section small {
    display: block;
    font-size: 14px;
  }
}

@media screen and (max-width: 540px) {
  .latest_contents {
    padding: 1rem;
    gap: 1rem;
  }
  .section small {
    font-size: 15px;
  }
  .section {
    gap: 0.5rem;
  }
}

@media screen and (max-width: 300px) {
  .section small {
    font-size: 14px;
  }
}
</style>