<script setup lang="ts">
//
</script>

<template>
  <div class="hero-wrap">
    <div class="hero">
      <h1>ALDANA<br />RODRIGUEZ</h1>
      <p class="sub">Backend Developer — Estudiante avanzada de Tecnólogo en Informática</p>
      <div class="scroll-cue">scroll para ver más ↓</div>
    </div>
  </div>
</template>

<style scoped>
.hero-wrap {
  padding: 0;
  overflow: hidden;
}
.hero {
  padding: 180px 5vw 200px;
  margin-top: 40px;

  text-align: center;
  position: relative;
  overflow: hidden;
}
@media (max-width: 820px) {
  .hero {
    border-radius: 50% 50% 0 0 / 70px 70px 0 0;
    padding: 70px 6vw 100px;
  }
}
.hero::before {
  content: '';
  position: absolute;
  inset: 0;
  pointer-events: none;
}
.eyebrow {
  font-family: 'JetBrains Mono', monospace;
  font-size: 13px;
  color: var(--teal);
  display: inline-block;
  background: var(--paper);
  border: 1px solid var(--line);
  padding: 6px 14px;
  border-radius: 999px;
  margin-bottom: 28px;
}
.hero h1 {
  font-size: clamp(48px, 8vw, 96px);
  font-weight: 800;
  line-height: 0.98;
  letter-spacing: -0.02em;
}
.hero p.sub {
  margin-top: 26px;
  font-size: 18px;
  color: var(--olive);
  max-width: 520px;
  margin-left: auto;
  margin-right: auto;
  font-weight: 500;
}
.arrow-row {
  margin-top: 44px;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 16px;
}
.arrow-line {
  width: 120px;
  height: 2px;
  background: var(--ink);
  position: relative;
}
.arrow-line::after {
  content: '';
  position: absolute;
  right: -1px;
  top: -5px;
  border: 6px solid transparent;
  border-left-color: var(--ink);
  border-right: 0;
}
.status-pill {
  background: var(--ink);
  color: var(--cream);
  font-family: 'JetBrains Mono', monospace;
  font-size: 14px;
  font-weight: 600;
  padding: 12px 24px;
  border-radius: 999px;
}
.scroll-cue {
  margin-top: 60px;
  font-family: 'JetBrains Mono', monospace;
  font-size: 12px;
  color: var(--pink-dark);
}
</style>
