<template>
  <div class="container">
    <Popular />
    <div class="sections">
      <div class="">
        <div class="recent_header">
          <h2 class="">Recent Receipes</h2>
          <span />
        </div>
        <Recent v-for="i in 5" :key="i" />
      </div>
      <div>
        <div class="mb-[2rem]"><Category /></div>
        <div class="my-[2rem]"><Letter /></div>
        <div class="my-[2rem]"><Latest /></div>
        <div class="my-[2rem]"><Follow /></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "IndexPage",
};
</script>

<style scoped>
.recent_header {
  display: flex;
  position: relative;
}
.recent_header h2 {
  font-size: 18px;
  position: absolute;
  background-color: rgb(255, 255, 255);
  top: -0.75rem;
  padding: 0 1rem 0 0;
}
.recent_header span {
  display: inline-block;
  width: 100%;
  padding: 0.2rem;
  border-bottom: 1px solid rgb(223, 223, 223);
  border-top: 1px solid rgb(223, 223, 223);
}
.sections {
  display: grid;
  grid-template-columns: 70% 30%;
  margin: 3rem 1rem 3rem 0 ;
  gap: 1rem;
}

@media screen and (max-width: 768px) {
  .sections {
    grid-template-columns: 60% 40%;
  }
}

@media screen and (max-width: 568px) {
  .sections {
  margin: 3rem 0 ;
    grid-template-columns: 1fr;
  }
}
</style>

