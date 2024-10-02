<script setup>
</script>

<template>
  <footer class="footer">
    <p>&copy; {{ new Date().getFullYear() }} TechPulse Insights - Capturando o pulso da inovação tecnológica</p>
  </footer>
</template>

<style scoped>
.footer {
  background-color: #1e1e1e;
  color: #ffffff;
  text-align: center;
  padding: 1rem;
  width: 100%;
  box-sizing: border-box;
}

/* Ensure the footer doesn't cover content */
:global(body) {
  padding-bottom: 60px; /* Adjust this value based on your footer's height */
}

@media (max-width: 768px) {
  .footer p {
    font-size: 0.9rem;
  }
}

@media (max-width: 480px) {
  .footer p {
    font-size: 0.8rem;
  }
  
  .footer {
    padding: 0.75rem;
  }
}
</style>