<template>
  <client-only>
    <div class="card2">
      
      <div class="card2-img">
        <!-- img -->
        <img src="../assets/images/food3.jpg" alt="" />
      </div>
      <div class="card2-contents">
        <!-- content -->
        <div class="card2-small">
          <small
            ><font-awesome-icon icon="fa-solid fa-clock" /> 30 minutes</small
          >
          <small
            ><font-awesome-icon icon="fa-solid fa-thumbs-up" /> Super
            easy</small
          >
        </div>
        <h1>Cheesy Pasta with cripsy bacon and mozzarella chees</h1>
        <p>
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dolorem
          soluta optio accusamus voluptatibus, culpa earum eaque, qui corrupti
          deleniti error ipsa?
        </p>

        <div class="card2-footer">
          <div class="card2-identity">
            <div>
              <img src="../assets/images/people1.jpg" alt="" />
            </div>
            <div>
              <h3>Pablo Emmanuel</h3>
              <small>May 13 2019</small>
            </div>
          </div>
          <div class="card2-footer-icons">
            <div id="share">
              <font-awesome-icon icon="fa-solid fa-share-nodes" />
            </div>
            <div id="bookmark">
              <font-awesome-icon icon="fa-solid fa-bookmark" />
            </div>
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
.card2 {
  display: grid;
  /* max-width: 450px; */
  gap: 1.5rem;
  transition: 0.4s;
    background-color: rgb(240, 236, 236);
}
.card2-img img {
  max-width: 450px;
  width: 100%;
  height: 250px;
  transition: 0.4s;
  object-fit: cover;
}

.card2-contents {
  display: flex;
  gap: 1rem;
  flex-direction: column;
  width: 100%;
  padding: 0 1rem .4rem ;
}

.card2-contents .card2-small {
  display: flex;
  gap: 1rem;
  flex-direction: row;
  align-items: center;
}

.card2-contents h1 {
  font-size: 20px;
}

.card2-contents p {
  color: rgb(160, 157, 157);
  font-size: 18px;
}

.card2-footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.card2-identity {
  display: flex;
  align-items: center;
  gap: 0.5rem;
}
.card2-contents img {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  object-fit: cover;
}

.card2-footer-icons {
  display: flex;
  gap: 1rem;
}

#share,
#bookmark {
  font-size: 25px;
  color: rgb(73, 72, 72);
  box-shadow: 0 0.25em 0.5em 0 rgb(0 0 0 / 10%);
  width: 40px;
  height: 40px;
  border-radius: 50%;
  display: flex;
  padding: 1rem;
  justify-content: center;
  align-items: center;
  /* border: 1px solid gray; */
}
#share:hover,
#bookmark:hover {
  color: rgb(218, 218, 218);
  box-shadow: 0 0.25em 0.5em 0 rgba(131, 131, 131, 0.1);
  text-shadow: 0 0.25em 0.5em rgb(0 0 0 / 10%);
  cursor: pointer;
}

@media screen and (max-width: 620px) {
  .card2 {
  gap: 1rem;

}
.card2 h1{
  font-size: 20px;
}
.card2 p{
  font-size: 17px;
}
.card2-img img{
  height: 200px;
}
.card2-footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.card2-identity {
  display: flex;
  align-items: center;
  gap: 0.5rem;
}
.card2-contents img {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  object-fit: cover;
}

.card2-footer-icons {
  display: flex;
  gap: .8rem;
}

#share,
#bookmark {
  font-size: 20px;
  /* width:30px;
  height: 30px; */
}

}
</style>