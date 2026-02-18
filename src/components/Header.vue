<template>
  <header class="header">
    <div class="container">
      <div class="logo">
        <span class="logo-text">NETCORN</span>
      </div>
      <nav class="nav">
        <a href="#services" class="nav-link">Services</a>
        <a href="#features" class="nav-link">Features</a>
        <a href="#about" class="nav-link">About</a>
        <a href="#contact" class="nav-link">Contact</a>
      </nav>
    </div>
  </header>
</template>

<script setup>
</script>

<style scoped>
.header {
  position: sticky;
  top: 0;
  z-index: 1000;
  background: rgba(15, 23, 42, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid rgba(255, 255, 255, 0.1);
  padding: 1rem 0;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  display: flex;
  align-items: center;
  gap: 0.8rem;
  font-size: 1.5rem;
  font-weight: 700;
  color: #fff;
  transition: transform 0.3s ease;
}

.logo:hover {
  transform: scale(1.05);
}

.nav {
  display: flex;
  gap: 2rem;
}

.nav-link {
  color: rgba(255, 255, 255, 0.8);
  text-decoration: none;
  transition: color 0.3s ease;
  position: relative;
}

.nav-link::after {
  content: '';
  position: absolute;
  bottom: -5px;
  left: 0;
  width: 0;
  height: 2px;
  background: linear-gradient(90deg, #00d4ff, #0099ff);
  transition: width 0.3s ease;
}

.nav-link:hover {
  color: #00d4ff;
}

.nav-link:hover::after {
  width: 100%;
}

@media (max-width: 768px) {
  .nav {
    gap: 1rem;
    font-size: 0.9rem;
  }
}
</style>
