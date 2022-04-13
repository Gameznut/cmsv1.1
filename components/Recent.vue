<template>
  <client-only>
    <div>
      <div class="recent_layout">
        <div class="recent_img">
          <img src="../assets/images/food.jpg" alt="" />
        </div>
        <div class="recent_contents">
          <div class="recent_small">
            <small>
              <font-awesome-icon icon="fa-solid fa-clock" />
              30 minutes</small
            >
            <small><font-awesome-icon icon="fa-solid fa-tag" /> Healthy</small>
          </div>
          <h1>Vegan Beef</h1>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. In
            voluptate asperiores placeat ipsa rerum fuga nesciunt repellat
            labore quaerat officia!
          </p>
        </div>
      </div>
    </div>
  </client-only>
</template>

<script>
export default {};
</script>

<style scoped>
.recent_layout {
  display: flex;
  gap: 1.5rem;
  align-items: center;
  margin: 2rem 0 0;
}

.recent_img img {
  /* max-width: 650px; */
  width: 100%;
  height: 300px;
  transition: 0.4s;
  object-fit: cover;
}

.recent_contents {
  max-width: 600px;
}
.recent_contents .recent_small {
  display: flex;
  gap: 1rem;
  flex-direction: row;
  align-items: center;
}

.recent_contents h1 {
  font-size: 25px;
}

.recent_contents p {
  color: rgb(160, 157, 157);
  font-size: 18px;
}

@media screen and (max-width: 1024px) {
  .recent_img img {
    width: 100%;
    height: 250px;
  }
  .recent_contents {
    max-width: 350px;
  }
}

@media screen and (max-width: 768px) {
  .recent_layout {
    gap: 1rem;
  }
  .recent_img img {
    width: 100%;
    height: 200px;
  }
  .recent_contents {
    max-width: 300px;
  }
  .recent_contents p {
    font-size: 16px;
  }
}

@media screen and (max-width: 450px) {
  .recent_img img {
    width: 100%;
    height: 200px;
  }
  .recent_contents {
    max-width: 200px;
  }
  .recent_contents h1 {
    font-size: 18px;
  }
  .recent_contents p {
    font-size: 14px;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
  }
}

@media screen and (max-width: 393px) {
  .recent_contents .recent_small {
    flex-direction: row;
    align-items: flex-start;
    font-size: 14px;
  }
  .recent_img img {
    width: 100%;
    height: 150px;
  }
  .recent_contents {
    max-width: 150px;
  }
  .recent_contents p {
    display: none;
  }
}

@media screen and (max-width: 353px) {
  .recent_contents .recent_small {
    gap: 0;
    flex-direction: column;
    align-items: flex-start;
    font-size: 14px;
  }
  .recent_img img {
    width: 100%;
    height: 150px;
  }
  .recent_contents {
    max-width: 150px;
  }
  .recent_contents p {
    display: none;
  }
}

@media screen and (max-width: 290px) {
  .recent_layout {
    gap: 0.5rem;
  }

  .recent_img img {
    width: 100%;
    height: 100px;
  }
  .recent_contents {
    max-width: 100px;
  }
}
</style>>