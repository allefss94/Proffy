<template>
  <div class="container">
    <div class="nav">
      <div class="link">
        <router-link to="/">
          <img src="@/assets/images/icons/back.svg" alt="Voltar" />
        </router-link>
      </div>
      <div>
        <img class="logo" src="@/assets/images/logo.svg" alt="Proffy" />
      </div>
    </div>

    <div class="main">
      <h1>{{title}}</h1>

      <span>{{subtitle}}</span>
    </div>
  </div>
</template>

<script>
export default {
  props: ["title", "subtitle"]
};
</script>

<style scoped>
.container {
  width: 100vw;
  min-height: 400px;
  background: var(--color-background);
}

.container .nav {
  margin: 0 5rem;
  padding-top: 3rem;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
}

.container .nav .logo {
  width: 5rem;
}

.container .main {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;

  text-align: left;
}

.container .main h1 {
  font: 500 2.6rem Helvetica;
  color: var(--color-text-in-primary);
  width: 450px;
}

.container .main span {
  font: 500 1rem Helvetica;
  color: var(--color-text-in-primary-dark);
  margin-left: -20px;
}

@media all and (max-width: 700px) {
  .container {
    min-height: 600px;
  }

  .container .main h1 {
    width: 80%;
  }

  .container .main span {
    width: 80%;
    margin: 0;
  }
}
</style>