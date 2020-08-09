<template>
  <div class="container">
    <div class="align">
      <header>
        <img
          src="https://avatars3.githubusercontent.com/u/56445202?s=460&u=3f78715f7736242702ae3588db4102356c1bc082&v=4"
          alt="avatar"
        />
        <div class="infos">
          <p>{{infos.name}}</p>
          <small>Desenvolvimento</small>
        </div>
      </header>
      <main>
        <p>{{infos.description}}</p>
        <p>{{infos.bio}}</p>
      </main>
      <footer>
        <div class="cost">
          <span>Preço/hora:</span>
          <strong>R$ {{infos.cost}}</strong>
        </div>
        <div class="contact">
          <button type="button">
            <img src="@/assets/images/icons/whatsapp.svg" alt="whatsapp" />
            Entrar em contato
          </button>
        </div>
      </footer>
    </div>
  </div>
</template>

<script>
export default {
  props: ["infos"]
};
</script>

<style scoped>
.container {
  display: flex;
  justify-content: center;
  max-width: 100vw;
}
.align {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;
  margin: 1rem;
  padding: 1.5rem;
  border-radius: 0.8rem;
  max-width: 655px;

  background: var(--color-background-card);
}

.container header {
  display: flex;
  justify-content: center;
  align-items: center;
}

.container header img {
  width: 8rem;
  height: auto;
  border-radius: 50%;
  margin-right: 2.4rem;
}

.container header .infos p {
  font: 700 1.2rem Helvetica;
  margin: 0;
  margin-bottom: 0.5rem;
}
.container header .infos small {
  font: 500 0.8rem Helvetica;
  color: rgba(44, 44, 44, 0.692);
}

.container main {
  padding: 1rem 0;
  font: 400 1rem Helvetica;
  color: rgba(44, 44, 44, 0.966);
}

.container footer {
  display: flex;
  justify-content: space-between;
  align-items: center;

  width: 100%;
}

.container footer .cost span {
  font: 400 0.8rem Helvetica;
  margin-right: 0.5rem;
  color: rgba(44, 44, 44, 0.966);
}
.container footer .cost strong {
  font: 700 0.8rem Helvetica;
  color: var(--color-button);
}

.container footer .contact button {
  display: flex;
  justify-content: center;
  align-items: center;

  padding: 1rem;
  border: none;
  border-radius: 0.4rem;
  background: var(--color-button-contact);
  color: var(--color-text-in-primary);
}

.container footer .contact button img {
  margin-right: 15px;
}
</style>