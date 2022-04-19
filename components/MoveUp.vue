<template>
  <client-only>
    <div class="container">
      <div class="move-up">
        <span @click="top" class="arrow-up"
          ><font-awesome-icon id="arrow-up" icon="fa-solid fa-angles-up"
        /></span>
      </div>
    </div>
  </client-only>
</template>

<script>
export default {
  methods: {
    top() {
      if (process.browser) {
        window.scrollTo({
          top: 0,
          behavior: "smooth",
        });
      }
    },
  },
};
</script>

<style scoped>
.move-up {
  float: right;
  margin-top: -5rem;
}
.arrow-up {
  padding: 1rem;
  background-color: rgb(134, 223, 134);
  margin-bottom: 2rem;
  margin-right: 2rem;
  display: block;
  border-radius: 0.5rem;
  transition: 0.4s;
  cursor: pointer;
}

.arrow-up:hover {
  background-color: rgb(58, 172, 58);
}

@media screen and (max-width: 780px) {
  .move-up {
    margin-top: -3rem;
  }

  .arrow-up {
    margin-bottom: 2rem;
    margin-right: 1rem;
  }
}
</style>