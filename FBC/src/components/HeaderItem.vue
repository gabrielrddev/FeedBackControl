<script setup>
import { RouterLink } from 'vue-router';
</script>

<template>
  <div>
    <nav class="navbar">
      <div class="navbar-logo">FBC</div>
      <input type="checkbox" id="navbar-toggle" class="navbar-toggle">
      <label for="navbar-toggle" class="navbar-toggle-label">
        <span></span>
      </label>
      <ul class="navbar-menu">
        <li><RouterLink to="/">Home</RouterLink></li>
        <li><RouterLink to="/faq">FAQ</RouterLink></li>
        <li><RouterLink to="/feed">Feedback</RouterLink></li>
      </ul>
    </nav>
  </div>
</template>

<style scoped>
body {
  font-family: Arial, sans-serif;
  background-color: #121212;
  color: #e0e0e0;
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.navbar {
  background-color: #1e1e1e;
  padding: 1rem;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  z-index: 1000;
}

.navbar-logo {
  color: #ffffff;
  font-weight: bold;
  font-size: 1.2rem;
}

.navbar-menu {
  list-style-type: none;
  margin: 0;
  padding: 0;
  display: flex;
}

.navbar-menu li {
  margin-left: 1.5rem;
}

.navbar-menu a {
  color: #ffffff;
  text-decoration: none;
  font-weight: bold;
  transition: color 0.3s ease;
}

.navbar-menu a:hover {
  color: #bdbdbd;
}

.navbar-toggle {
  display: none;
}

.navbar-toggle-label {
  display: none;
  cursor: pointer;
}

@media (max-width: 768px) {
  .navbar-menu {
    display: none;
    flex-direction: column;
    position: absolute;
    top: 100%;
    left: 0;
    right: 0;
    background-color: #1e1e1e;
    padding: 1rem;
  }

  .navbar-menu li {
    margin: 0.5rem 0;
  }

  .navbar-toggle-label {
    display: block;
    padding: 0.5rem;
  }

  .navbar-toggle-label span,
  .navbar-toggle-label span::before,
  .navbar-toggle-label span::after {
    display: block;
    background-color: #ffffff;
    height: 2px;
    width: 24px;
    position: relative;
  }

  .navbar-toggle-label span::before,
  .navbar-toggle-label span::after {
    content: '';
    position: absolute;
  }

  .navbar-toggle-label span::before {
    bottom: 8px;
  }

  .navbar-toggle-label span::after {
    top: 8px;
  }

  .navbar-toggle:checked ~ .navbar-menu {
    display: flex;
  }
}
</style>