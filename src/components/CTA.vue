<template>
  <section class="cta">
    <div class="background">
      <div class="gradient"></div>
    </div>
    <div class="content">
      <h2>Ready to Accelerate Your Business?</h2>
      <p>Contact us to learn how NETCORN's premium internet connectivity can boost your business efficiency</p>
      <div class="buttons">
        <button class="btn btn-primary">Get Started</button>
        <button class="btn btn-secondary">Request Trial</button>
      </div>
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
.cta {
  position: relative;
  padding: 6rem 2rem;
  overflow: hidden;
}

.background {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 0;
}

.gradient {
  width: 100%;
  height: 100%;
  background: linear-gradient(
    135deg,
    rgba(0, 212, 255, 0.15) 0%,
    rgba(124, 58, 237, 0.15) 50%,
    rgba(249, 115, 22, 0.1) 100%
  );
}

.content {
  position: relative;
  z-index: 1;
  max-width: 800px;
  margin: 0 auto;
  text-align: center;
  color: #fff;
}

h2 {
  font-size: 2.5rem;
  font-weight: 800;
  margin-bottom: 1rem;
  background: linear-gradient(135deg, #00d4ff, #7c3aed);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

p {
  font-size: 1.2rem;
  color: rgba(255, 255, 255, 0.8);
  margin-bottom: 2rem;
  line-height: 1.6;
}

.buttons {
  display: flex;
  gap: 1rem;
  justify-content: center;
  flex-wrap: wrap;
}

.btn {
  padding: 1rem 2.5rem;
  font-size: 1rem;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  font-weight: 600;
  transition: all 0.3s ease;
}

.btn-primary {
  background: linear-gradient(135deg, #00d4ff, #0099ff);
  color: #fff;
  box-shadow: 0 0 20px rgba(0, 212, 255, 0.4);
}

.btn-primary:hover {
  transform: translateY(-3px);
  box-shadow: 0 10px 30px rgba(0, 212, 255, 0.6);
}

.btn-secondary {
  background: transparent;
  color: #00d4ff;
  border: 2px solid #00d4ff;
}

.btn-secondary:hover {
  background: rgba(0, 212, 255, 0.1);
  transform: translateY(-3px);
}

@media (max-width: 768px) {
  h2 {
    font-size: 1.8rem;
  }

  p {
    font-size: 1rem;
  }

  .buttons {
    flex-direction: column;
  }

  .btn {
    width: 100%;
  }
}
</style>
