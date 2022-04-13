<template>
  <div class="container">
    <Popular />
    <div class="sections">
      <div></div>
      <div >
        <div class="my-[2rem]"><Category /></div>
        
        <div class="my-[2rem]"><Letter/></div>
        <div class="my-[2rem]"><Latest/></div>
        <div class="my-[2rem]"><Follow/></div>
        <div class="my-[2rem]"></div>

        

      </div>
    </div>
  </div>
</template>

<script>
export default {
    name: "NextPage",
};
</script>

<style scoped>
.sections {
  display: grid;
  grid-template-columns: 70% 30%;
  margin: 3rem 0
}

@media screen and (max-width: 768px) {
  .sections {
    grid-template-columns: 60% 40%;
  }
}

@media screen and (max-width: 520px) {
  .sections {
    grid-template-columns: 1fr;
  }
}
</style>

