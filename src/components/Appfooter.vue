<script setup lang="ts">
//
</script>

<template>
  <footer>
    <span>Aldana Rodriguez</span>
    <span> · </span>
    <span>hecho con Vue 3</span>
  </footer>
</template>

<style scoped>
footer {
  background: var(--paper);

  color: var(--text-soft);

  text-align: center;

  padding: 40px 6vw;

  font-family: 'JetBrains Mono', monospace;
  font-size: 12.5px;

  letter-spacing: 0.02em;

  border-top: 1px solid var(--line);
}

footer span:first-child {
  color: var(--ink);
  font-weight: 700;
}

footer span:last-child {
  color: var(--pink-dark);
}
</style>
