<template>
  <div>
    <div class="letter_contents">
      <h1>never miss a post!</h1>
      <p>Signup for free and be the first to get notified on new updates.</p>
      <form @submit.prevent>
        <div class="form">
          <input type="text" v-model="newsletter" placeholder="Your Email *" />
          <button>Suscribe</button>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return{
      newsletter: ""
    }
  }
};
</script>

<style scoped>
.letter_contents {
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 1rem;
  text-align: center;
  background-color: rgb(216, 216, 216);
  padding: 3rem 2rem;
}
h1 {
  font-size: 30px;
  text-transform: capitalize;
}
h1,
p,
.form {
  max-width: 250px;
  margin: 0 auto;
}
.form {
  display: inline-flex;
  flex-direction: column;
  width: 100%;
  gap: 0.7rem;
}
button,
input {
  width: 100%;
  padding: 0.75rem 1.2rem;
  outline: 0;
}
button {
  background-color: black;
  color: white;
  transition: 0.4s;
}

button:hover {
  background-color: rgb(235, 235, 235);
  color: rgb(0, 0, 0);
}

@media screen and (max-width: 320px) {
  .letter_contents {
    padding: 2rem 1rem;
  }
}
</style>