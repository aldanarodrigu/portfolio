<script setup lang="ts">
//
</script>

<template>
  <nav>
    <span class="nav-tag">ALDANA RODRIGUEZ</span>

    <div class="nav-links">
      <a href="#about">Sobre mí</a>
      <a href="#stack">Stack</a>
      <a href="#proyectos">Proyectos</a>
      <a href="#contacto">Contacto</a>
    </div>

    <a
      :href="`${import.meta.env.BASE_URL}Aldana_Rodriguez_CV.pdf`"
      download="Aldana_Rodriguez_CV.pdf"
      class="nav-cta"
    >
      Descargar CV
    </a>
  </nav>
</template>

<style scoped>
nav {
  display: flex;
  align-items: center;
  justify-content: space-between;

  padding: 22px 5vw;

  position: sticky;
  top: 0;
  z-index: 50;

  font-family: 'Plus Jakarta Sans', sans-serif;

  backdrop-filter: blur(12px);
}

.nav-tag {
  font-family: 'JetBrains Mono', monospace;

  font-size: 13px;
  font-weight: 700;

  color: var(--ink);

  white-space: nowrap;
}

.nav-links {
  display: flex;
  gap: 4px;

  background: rgba(255, 255, 255, 0.8);

  border: 1px solid var(--line);

  border-radius: 999px;

  padding: 5px;
}

.nav-links a {
  font-size: 14px;
  font-weight: 600;

  padding: 9px 18px;

  border-radius: 999px;

  color: var(--ink);

  text-decoration: none;

  transition: 0.2s ease;
}

.nav-links a:hover {
  background: var(--pink-light);
  color: var(--ink);
}

.nav-cta {
  font-family: 'JetBrains Mono', monospace;

  font-size: 13px;
  font-weight: 700;

  background: transparent;

  color: var(--ink);

  padding: 11px 20px;

  border-radius: 999px;

  border: 1px solid var(--ink);

  text-decoration: none;

  transition: 0.2s ease;

  white-space: nowrap;
}

.nav-cta:hover {
  background: var(--ink);
  color: white;
}

/* =========================
   TABLET
   ========================= */

@media (max-width: 1000px) {
  nav {
    flex-wrap: wrap;
    gap: 14px;
  }

  .nav-links {
    order: 3;
    width: 100%;
    justify-content: center;
  }
}

/* =========================
   MOBILE
   ========================= */

@media (max-width: 600px) {
  nav {
    padding: 16px 5vw;
    gap: 12px;
  }

  .nav-tag {
    font-size: 11px;
  }

  .nav-cta {
    font-size: 11px;
    padding: 9px 14px;
  }

  .nav-links {
    gap: 2px;
    padding: 4px;

    overflow-x: auto;
    justify-content: flex-start;

    scrollbar-width: none;
  }

  .nav-links::-webkit-scrollbar {
    display: none;
  }

  .nav-links a {
    font-size: 12px;
    padding: 8px 12px;

    white-space: nowrap;
  }
}
</style>
