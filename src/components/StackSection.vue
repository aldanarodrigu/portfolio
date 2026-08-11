<script setup lang="ts">
interface StackGroup {
  title: string
  items: string[]
}

const stackGroups: StackGroup[] = [
  {
    title: 'Lenguajes',
    items: ['Java', 'PHP', 'C++', 'C', 'Bash'],
  },
  {
    title: 'Backend',
    items: ['Spring Boot', 'Laravel', 'REST APIs'],
  },
  {
    title: 'Frontend',
    items: ['Vue.js', 'TypeScript', 'HTML', 'CSS'],
  },
  {
    title: 'Bases de Datos',
    items: ['PostgreSQL', 'SQL'],
  },
  {
    title: 'Infraestructura & Cloud',
    items: ['Docker', 'Kubernetes', 'AWS', 'Linux'],
  },
  {
    title: 'Herramientas',
    items: ['Git', 'GitHub', 'CI/CD'],
  },
]
</script>

<template>
  <section id="stack">
    <div class="stack-header">
      <span class="section-label" style="text-align: center">02 — Stack técnico</span>
      <h2>Stack</h2>
    </div>
    <div class="stack-grid">
      <div class="stack-card" v-for="group in stackGroups" :key="group.title">
        <h3>{{ group.title }}</h3>
        <ul>
          <li v-for="item in group.items" :key="item">{{ item }}</li>
        </ul>
      </div>
    </div>
  </section>
</template>
<style scoped>
section {
  padding: 120px 6vw;
  max-width: 1180px;
  margin: 0 auto;
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

.stack-header {
  text-align: center;
  margin-bottom: 60px;
}

.stack-header h2 {
  font-size: clamp(30px, 4vw, 44px);
  font-weight: 800;
}

.stack-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 22px;
}

@media (max-width: 820px) {
  .stack-grid {
    grid-template-columns: 1fr 1fr;
  }
}

@media (max-width: 560px) {
  .stack-grid {
    grid-template-columns: 1fr;
  }
}

.stack-card {
  background: var(--paper);

  border: 1px solid var(--line);

  border-radius: var(--radius-md);

  padding: 26px;

  transition:
    transform 0.2s ease,
    box-shadow 0.2s ease;
}

.stack-card:hover {
  transform: translateY(-4px);

  box-shadow: 0 20px 40px -18px rgba(0, 0, 0, 0.18);
}

.stack-card .tag {
  font-family: 'JetBrains Mono', monospace;

  font-size: 12px;

  color: var(--pink-dark);

  margin-bottom: 10px;

  display: block;
}

.stack-card h3 {
  font-size: 19px;

  font-weight: 700;

  margin-bottom: 12px;
}

.stack-card ul {
  list-style: none;

  display: flex;

  flex-wrap: wrap;

  gap: 8px;

  padding: 0;
}

.stack-card li {
  font-family: 'JetBrains Mono', monospace;

  font-size: 12.5px;

  background: var(--pink-light);

  color: var(--ink);

  padding: 5px 10px;

  border-radius: 6px;

  border: 1px solid rgba(217, 138, 163, 0.25);
}
</style>
