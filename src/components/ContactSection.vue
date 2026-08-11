<script setup lang="ts">
//
</script>

<template>
  <section id="contacto">
    <div class="contact-container">
      <div class="contact-block">
        <span class="section-label">04 — Contacto</span>

        <h2>Hablemos</h2>

        <p>
          Estoy buscando oportunidades para seguir creciendo. Si tenés una propuesta o simplemente
          querés conectar, escribime.
        </p>

        <div class="contact-links">
          <a href="mailto:aldanarodriguez0707@gmail.com" target="_blank"> Email</a>
          <a
            href="https://github.com/aldanarodrigu"
            class="outline"
            target="_blank"
            rel="noopener noreferrer"
            >GitHub</a
          >
          <a
            href="https://www.linkedin.com/in/aldana-rodriguez-02b315209/"
            class="outline"
            target="_blank"
          >
            LinkedIn
          </a>
        </div>
      </div>
    </div>
  </section>
</template>
<style scoped>
section {
  padding: 120px 0;
}

.contact-container {
  max-width: 1180px;
  margin: 0 auto;
  padding: 0 6vw;
}

.contact-block {
  background: var(--paper);

  border: 1px solid var(--line);

  border-radius: var(--radius-lg);

  padding: 80px 6vw;

  text-align: center;

  position: relative;

  overflow: hidden;

  box-shadow: 0 20px 50px -30px rgba(0, 0, 0, 0.18);
}

.section-label {
  position: relative;

  font-family: 'JetBrains Mono', monospace;

  font-size: 13px;

  color: var(--pink-dark);

  text-transform: uppercase;

  letter-spacing: 0.08em;

  margin-bottom: 18px;

  display: block;
}

.contact-block h2 {
  position: relative;

  font-size: clamp(32px, 5vw, 54px);

  font-weight: 800;

  margin-bottom: 20px;
}

.contact-block p {
  position: relative;

  color: var(--text-soft);

  max-width: 500px;

  margin: 0 auto 40px;

  font-size: 17px;

  line-height: 1.7;
}

.contact-links {
  position: relative;

  display: flex;

  flex-wrap: wrap;

  gap: 14px;

  justify-content: center;
}

.contact-links a {
  font-family: 'JetBrains Mono', monospace;

  font-size: 14px;

  font-weight: 600;

  background: var(--ink);

  color: white;

  padding: 14px 26px;

  border-radius: 999px;

  text-decoration: none;

  transition: 0.2s ease;
}

.contact-links a:hover {
  transform: translateY(-3px);
}

.contact-links a.outline {
  background: transparent;

  color: var(--ink);

  border: 1px solid var(--line);
}

.contact-links a.outline:hover {
  background: var(--pink-light);

  border-color: var(--pink);
}
</style>
