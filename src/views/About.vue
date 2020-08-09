<template>
  <div class="container">
    <Header title="Estes são os
proffys disponíveis." subtitle />
    <div class="main">
      <div class="input-box">
        <div class="inputs">
          <label for="name">Matéria</label>
          <select type="select" name="name">
            <option value selected disabled hidden>Selecione uma matéria</option>
            <option value="matematica">Matemática</option>
            <option value="portugues">Português</option>
            <option value="Filosofia">Filosofia</option>
            <option value="Artes">Artes</option>
          </select>
        </div>
        <div class="inputs">
          <label for="name">Dia da semana</label>
          <select type="select" name="week_day">
            <option value selected disabled hidden>Selecione uma dia</option>
            <option value="segunda">Segunda-feira</option>
            <option value="terca">Terça-feira</option>
            <option value="quarta">Quarta-feira</option>
            <option value="quinta">Quinta-feira</option>
          </select>
        </div>
        <div class="inputs">
          <label for="name">horario</label>
          <input type="time" name="time" />
        </div>
      </div>
    </div>
    <section>
      <ProffyItem v-for="proffy in proffyData" :key="proffy.name" :infos="proffy" />
    </section>
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import ProffyItem from "@/components/ProffyItem.vue";

export default {
  components: { Header, ProffyItem },
  data() {
    return {
      proffyData: [
        {
          name: "Allef Sousa",
          description: "Desenvolvedor Web",
          bio:
            "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum",
          cost: "50,00"
        },
        {
          name: "Anderson Carlos",
          description: "Desenvolvedor Web",
          bio:
            "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum",
          cost: "40,00"
        },
        {
          name: "Atila Sousa",
          description: "Desenvolvedor Web",
          bio:
            "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum",
          cost: "60,00"
        }
      ]
    };
  }
};
</script>

<style scoped>
.container .main {
  display: flex;
  justify-content: center;

  max-width: 100%;
}

.container .main .input-box {
  margin-top: -4.5rem;
  display: flex;
  border-radius: 5px 5px 0 0;
}

.container .main .inputs {
  display: flex;
  flex-direction: column;
  padding: 1.4rem;
}

.container .main .inputs label {
  color: var(--color-text-in-primary);
  font: 500 1rem Helvetica;
  margin-bottom: 0.5rem;
}

.container .main .inputs input {
  padding: 1rem;
  border-radius: 0.6rem;
  border: none;
  width: 180px;
}

.container .main .inputs select {
  padding: 1rem;
  border-radius: 0.6rem;
  border: none;
  width: 200px;
  text-align: center;
}

@media all and (max-width: 700px) {
  .container .main .input-box {
    margin-top: -17rem;
    display: flex;
    flex-direction: column;
    justify-content: center;

    width: 80%;
  }

  .container .main .inputs {
    padding: 0;
    margin-bottom: 12px;
  }
  .container .main .inputs input {
    width: 92%;
  }
  .container .main .inputs select {
    width: 100%;
  }
}
</style>
