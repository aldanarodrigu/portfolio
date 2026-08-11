<script setup lang="ts">
interface Project {
  num: string
  title: string
  description: string
  tags: string[]
  link: string
}

const projects: Project[] = [
  {
    num: '01',
    title: 'Sistema de Gestión de Servicios Profesionales',
    description:
      'Sistema web construido con Laravel (PHP) y Vue.js, diseñado para facilitar la administración de ofertas y reservas. Incluye autenticación y autorización de usuarios, gestión de disponibilidad y turnos, APIs REST para integraciones y persistencia de datos con PostgreSQL.',
    tags: ['Laravel', 'PHP', 'Vue.js', 'PostgreSQL', 'AWS', 'RESTful APIs', 'Autenticación'],
    link: 'https://github.com/aldanarodrigu/taller-php',
  },
  {
    num: '02',
    title: 'Arquitectura de Microservicios',
    description:
      'Arquitectura de microservicios diseñada y desplegada en AWS utilizando Docker y Kubernetes (EKS). Incluye una API REST desarrollada con Django, un microservicio de notificaciones, integración con Amazon RDS PostgreSQL, API Gateway y balanceadores de carga, aplicando buenas prácticas de seguridad e infraestructura cloud.',
    tags: ['Docker', 'Kubernetes', 'AWS', 'Python', 'Django', 'RDS PostgreSQL', 'API Gateway'],
    link: '#',
  },
  {
    num: '03',
    title: 'Aplicación de Comunicación Corporativa',
    description:
      'Plataforma de comunicación corporativa desarrollada con Java EE para mensajería en tiempo real mediante WebSockets, gestión de comunidades y canales, y autenticación segura de usuarios. Incluye persistencia con PostgreSQL, Hibernate y JPA, además de cifrado de extremo a extremo (E2E).',
    tags: ['Java EE', 'WebSockets', 'PostgreSQL', 'Hibernate', 'JPA', 'Cifrado E2E'],
    link: 'https://github.com/aldanarodrigu/taller-javaee',
  },
]
</script>

<template>
  <section id="proyectos">
    <div class="proj-header">
      <span class="section-label">03 — Proyectos</span>
      <h2>Proyectos</h2>
    </div>

    <div class="proj-list">
      <article v-for="project in projects" :key="project.num" class="proj-card">
        <span class="proj-num">{{ project.num }}</span>

        <div class="proj-content">
          <h3>{{ project.title }}</h3>

          <div class="proj-tags">
            <span v-for="tag in project.tags" :key="tag">
              {{ tag }}
            </span>
          </div>

          <p>{{ project.description }}</p>
        </div>

        <a
          v-if="project.link !== '#'"
          class="proj-link"
          :href="project.link"
          target="_blank"
          rel="noopener noreferrer"
        >
          Ver repo
        </a>

        <span v-else class="proj-link proj-link-disabled"> Repo </span>
      </article>
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

.proj-header {
  text-align: center;
  margin-bottom: 60px;
}

.proj-header h2 {
  font-size: clamp(30px, 4vw, 44px);
  font-weight: 800;
}

/* PROJECT LIST */

.proj-list {
  display: flex;
  flex-direction: column;
  gap: 22px;
}

.proj-card {
  background: var(--paper);
  border: 1px solid var(--line);
  border-radius: var(--radius-lg);
  padding: 34px 36px;

  display: grid;
  grid-template-columns: 45px 1fr auto;
  gap: 24px;

  align-items: start;

  transition:
    transform 0.2s ease,
    box-shadow 0.2s ease,
    border-color 0.2s ease;
}

.proj-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 20px 40px -20px rgba(0, 0, 0, 0.18);
  border-color: rgba(217, 138, 163, 0.45);
}

/* NUMBER */

.proj-num {
  font-family: 'JetBrains Mono', monospace;
  font-size: 13px;
  color: var(--pink-dark);
  padding-top: 6px;
}

/* CONTENT */

.proj-content {
  min-width: 0;
}

.proj-card h3 {
  font-size: 23px;
  font-weight: 800;
  margin: 0 0 14px;
  line-height: 1.25;
}

.proj-card p {
  color: var(--text-soft);
  font-size: 15px;
  line-height: 1.7;
  margin: 16px 0 0;
  max-width: 720px;
}

/* TAGS */

.proj-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 7px;
}

.proj-tags span {
  font-family: 'JetBrains Mono', monospace;
  font-size: 11.5px;
  background: var(--pink-light);
  color: var(--ink);
  padding: 5px 10px;
  border-radius: 6px;
  border: 1px solid rgba(217, 138, 163, 0.25);
}

/* LINK */

.proj-link {
  font-family: 'JetBrains Mono', monospace;
  font-size: 13px;
  font-weight: 600;

  color: var(--ink);
  border: 1px solid var(--line);

  padding: 10px 16px;
  border-radius: 999px;

  white-space: nowrap;
  height: fit-content;

  text-decoration: none;

  transition: 0.2s ease;
}

.proj-link:hover {
  background: var(--ink);
  color: white;
}

.proj-link-disabled {
  color: #aaa;
  cursor: default;
}

.proj-link-disabled:hover {
  background: transparent;
  color: #aaa;
}

/* RESPONSIVE */

@media (max-width: 760px) {
  section {
    padding: 90px 6vw;
  }

  .proj-header {
    margin-bottom: 40px;
  }

  .proj-card {
    grid-template-columns: 1fr;
    gap: 12px;
    padding: 28px;
  }

  .proj-num {
    padding-top: 0;
  }

  .proj-card h3 {
    font-size: 20px;
  }

  .proj-link {
    justify-self: start;
    margin-top: 6px;
  }
}
</style>
