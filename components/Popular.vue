<template>
  <client-only>
    <div>
      <div class="popular relative">
        <h1 class="heading">
          <span><font-awesome-icon icon="fa-solid fa-bolt-lightning" /></span>
          popular
        </h1>
        <Card2  v-for="(popular, i) in populars.slice(0,3)" :popular="popular" :key="i" class="test" />
      </div>
    </div>
  </client-only>
</template>


<script>
export default {
  data(){
    return{
      populars: [
        {
          imgs: "food",
          name: "Emmanuel Apabiekun",
          profile: "people4",
          title: "Egg salad",
          difficult: "Super Easy",
          description: `Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dolorem
            soluta optio accusamus voluptatibus, culpa earum eaque, qui corrupti
            deleniti error ipsa?`,
          date : new Date().toDateString(),
          duration: 40
        },
        {
          imgs: "food1",
          name: "Emmanuel Apabiekun",
          profile: "people1",
          title: "Cake",
          difficult: "Super Easy",
          description: `Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dolorem
            soluta optio accusamus voluptatibus, culpa earum eaque, qui corrupti
            deleniti error ipsa?`,
          date : new Date().toDateString(),
          duration: 35

        },
        {
          imgs: "food2",
          name: "Emmanuel Apabiekun",
          profile: "peopl2",
          title: "Chesse cake",
          difficult: "Super Easy",
          description: `Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dolorem
            soluta optio accusamus voluptatibus, culpa earum eaque, qui corrupti
            deleniti error ipsa?`,
          date : new Date().toDateString(),
          duration: 20

        },
        {
          imgs: "food3",
          name: "Apabiekun Emmanuel",
          profile: "people3",
          title: "Chesse cake",
          difficult: "Super Easy",
          description: `Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dolorem
            soluta optio accusamus voluptatibus, culpa earum eaque, qui corrupti
            deleniti error ipsa?`,
          date : new Date().toDateString(),
          duration: 40

        },
      ],
    }
  },
}
</script>

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
  background-color: rgb(219, 190, 22);
  gap: 0.8rem;
  padding: 0.7rem;
  font-size: 17px;
  font-weight: 500;
  width: max-content;
  position: absolute;
  z-index: 30;
}
.heading span {
  color: azure;
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