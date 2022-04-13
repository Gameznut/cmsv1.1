<template>
  <client-only>
    <div>
      <div class="card2">
        <div class="card2-img">
          <!-- img -->
          <img :src="require(`~/assets/images/${popular.imgs}.jpg`)" alt="" />
        </div>
        <div class="card2-contents">
          <!-- content -->
          <div class="card2-small">
            <small>
              <font-awesome-icon icon="fa-solid fa-clock" /> {{ popular.duration }} minutes</small
            >
            <small
              ><font-awesome-icon icon="fa-solid fa-thumbs-up" />
              {{ popular.difficult }}</small
            >
          </div>
          <h1>{{ popular.title }}</h1>
          <p>{{ popular.description }}</p>

          <div class="card2-footer">
            <div class="card2-identity">
              <div>
                <img
                  :src="require(`~/assets/images/${popular.profile}.jpg`)"
                  alt=""
                />
              </div>
              <div>
                <h3>{{ popular.name }}</h3>
                <small>{{ popular.date }}</small>
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
    </div>
  </client-only>
</template>

<script>
export default {
  data() {
    return {
      
    };
  },
  props: ['popular']
};
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
  padding: 0 1rem 0.4rem;
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
  .card2 h1 {
    font-size: 20px;
  }
  .card2 p {
    font-size: 17px;
  }
  .card2-img img {
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
    gap: 0.8rem;
  }

  #share,
  #bookmark {
    font-size: 20px;
    /* width:30px;
  height: 30px; */
  }
}

@media screen and (max-width: 540px) {
 .card2-footer {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    gap: 0.9rem;
  }
}

@media screen and (max-width: 380px) {
  .card2-footer {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    gap: 0.9rem;
  }

}
</style>