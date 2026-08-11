<script setup lang="ts">
//
</script>
<template>
  <section id="about">
    <div class="about-container">
      <div class="about-grid">
        <div>
          <span class="section-label">01 — Sobre mí</span>

          <h2>Hola, soy Aldana.</h2>

          <p>
            En 2023 decidí adentrarme en el mundo de la informática y, desde entonces, quedé
            fascinada con todo lo que hay detrás de la tecnología y con la cantidad de cosas que se
            pueden crear y aprender.
          </p>

          <p>
            Actualmente estoy cursando el último semestre del Tecnólogo en Informática en UTEC, una
            etapa en la que busco seguir creciendo y llevar todo lo aprendido un paso más allá.
          </p>
          <p>
            Me encuentro en constante aprendizaje, explorando nuevas áreas y, sobre todo, buscando
            proyectos que me permitan salir de lo académico, enfrentar problemas reales y entender
            cómo se construyen y mantienen sistemas más allá del entorno de estudio.
          </p>
          <p>
            Este portfolio es parte de ese proceso: un espacio donde reúno algunos de los proyectos
            en los que fui aprendiendo, experimentando y descubriendo cada vez mas sobre este mundo.
          </p>
        </div>

        <div class="photo">
          <img src="../assets/me.jpeg" alt="Foto de Aldana" />
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
section {
  padding: 120px 0;
}

.about-container {
  max-width: 1180px;
  margin: 0 auto;
  padding: 0 6vw;
}

.about-grid {
  display: grid;
  grid-template-columns: 1.1fr 0.9fr;
  gap: 70px;
  align-items: center;
}

@media (max-width: 900px) {
  .about-grid {
    grid-template-columns: 1fr;
  }
}

.section-label {
  font-family: 'JetBrains Mono', monospace;
  font-size: 13px;
  color: var(--pink-dark);
  text-transform: uppercase;
  letter-spacing: 0.08em;
  margin-bottom: 18px;
  display: block;
}

.about-grid h2 {
  font-size: clamp(32px, 4vw, 46px);
  font-weight: 800;
  line-height: 1.05;
  margin-bottom: 24px;
}

.about-grid p {
  font-size: 17px;
  color: #3a3a2e;
  line-height: 1.7;
  margin-bottom: 16px;
  max-width: 480px;
}

/* FOTO */
.photo {
  width: 100%;
  overflow: hidden;
}

.photo img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>
