<template>
  <div class="recent2_content relative ">
    <client-only>
    <small class="recent2_heading flex"><font-awesome-icon icon="fa-solid fa-star" class="text-[#538eb1]" />Recent2 Blog</small></client-only>
    <div class="recent2_layout grid">
      <div class="recent2_card">
        <Card />
      </div>
      <div class="recent2_sidecard flex flex-col">
        <SideCard class="test" />
        <SideCard class="test" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Recent2',
}
</script>

<style scoped>
.recent2_layout {
    position: relative;
    grid-template-columns: 1fr 1fr;
}

.recent2_heading {
    position: absolute;
    top: 0;
    z-index: 30;
    background-color: rgb(233, 212, 21);
    border-bottom-right-radius: 30px;
    padding: 10px;
    align-items: center;
    gap: .3rem;
    font-size: 19px;
    color: black;
}

@media only screen and (max-width:990px) {
    .recent2_layout {
        grid-template-columns: 1fr; 
    }
}
</style>