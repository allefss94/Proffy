<template>
  <div class="container">
    <header>
      <div class="logo">
        <img src="@/assets/images/logo.svg" alt />

        <p>
          Sua plataforma de
          <br />estudos online.
        </p>
      </div>
      <div class="landing">
        <img src="@/assets/images/landing.svg" alt />
      </div>
    </header>

    <main class="info">
      <div class="buttons">
        <router-link to="/about">
          <img src="@/assets/images/icons/study.svg" alt="estudar" />
          Estudar
        </router-link>
        <router-link to="/">
          <img src="@/assets/images/icons/give-classes.svg" alt="Dar Aulas" />
          Dar aulas
        </router-link>
      </div>

      <span>A cada dia desenvolvendo mais projetos.</span>
    </main>
  </div>
</template>

<script>
// @ is an alias to /src

export default {};
</script>
<style scoped>
.container {
  height: 100vh;
  width: 100vw;
  overflow: hidden;

  background: var(--color-background);

  display: flex;
  flex-direction: column;
  align-items: center;
}

.container header {
  margin-top: 3rem;
  display: flex;
  justify-content: center;
  align-items: center;
}

.container header img {
  width: 100%;
}

.container header .logo {
  width: 80%;
  margin: 0 4rem;
}

.container header .logo p {
  font: 700 2rem Helvetica;
  color: var(--color-text-in-primary);
}

.container header .landing {
  width: 130%;
}

.container main {
  margin-top: 3rem;
  width: 100vw;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
}

.container main .buttons {
  width: 50%;

  display: flex;
  justify-content: flex-start;
}

.container main .buttons a {
  width: 40%;
  height: 5rem;
  background: var(--color-button);

  border: none;
  border-radius: 0.4rem;

  font: 400 1.6rem Helvetica;
  text-decoration: none;
  color: var(--color-text-in-primary);

  display: flex;
  justify-content: center;
  align-items: center;

  transition: background-color 0.2s;
}

.container main .buttons a:hover {
  background: var(--color-button-dark);
}

.container main .buttons a img {
  margin-right: 15px;
}

.container main .buttons a:first-child {
  margin-right: 10%;
}

.container main span {
  color: var(--color-text-in-primary);
}

@media all and (max-width: 700px) {
  .container {
    width: 100%;
    height: 100vh;
    overflow: hidden;
  }
  .container header {
    flex-direction: column;
  }

  .container header .logo {
    width: 70%;
    text-align: center;
  }

  .container header .landing {
    width: 90%;
  }

  .container main {
    width: 100%;
    flex-direction: column;
    margin-top: 0;
    margin-bottom: 2rem;
  }

  .container main .buttons {
    width: 100%;
    justify-content: center;
    align-items: center;
    margin: 2rem 0;
  }
}
</style>