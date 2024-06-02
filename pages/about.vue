<template>
  <div class="about-us">
    <div class="container">
      <section class="company-info">
        <h2>Nasza firma</h2>
        <button @click="toggleText" class="button">Poznaj nas</button>
        <p v-if="showText">
          Jesteśmy dynamiczną firmą działającą na rynku od ponad 10 lat. Nasza
          misja to zapewnienie naszym klientom najlepszych produktów z całego
          świata w konkurencyjnych cenach. Specjalizujemy się w szerokim
          zakresie produktów, od elektroniki po modę i artykuły domowe.
        </p>
      </section>
      <section class="team">
        <h2>Nasz zespół</h2>
        <div class="team-member">
          <img src="http://localhost:3000/waldek.jpg" alt="Zdjęcie pracownika" />
          <h3>Jan Kowalski</h3>
          <p>Specjalista ds. elektroniki</p>
        </div>
        <div class="team-member">
          <img src="http://localhost:3000/ania.jpg" alt="Zdjęcie pracownika" />
          <h3>Anna Nowak</h3>
          <p>Specjalistka ds. mody</p>
        </div>
        <div class="team-member">
          <img src="http://localhost:3000/tomek.jpg" alt="Zdjęcie pracownika" />
          <h3>Paweł Wiśniewski</h3>
          <p>Specjalista ds. artykułów domowych</p>
        </div>
      </section>
    
    </div>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  setup() {
    const showText = ref(false);

    const toggleText = () => {
      showText.value = !showText.value;
    };

    return { showText, toggleText };
  },
};
</script>

<style scoped>
.about-us {
  padding: 50px 0;
}

.container {
  max-width: 800px;
  margin: 0 auto;
  text-align: center;
}

.company-info,
.team {
  margin-bottom: 40px;
}

h2 {
  margin-bottom: 20px;
}

.team-member {
  margin-top: 30px;
}

.team-member img {
  width: 150px;
  border-radius: 50%;
}

.team-member h3 {
  margin-top: 10px;
}

.team-member p {
  font-style: italic;
}
</style>
