<template>
  <section class="hero">
    <div class="background">
      <div class="animated-bg"></div>
      <div class="grid"></div>
    </div>
    <div class="content">
      <h1 class="title">
        <span class="gradient-text">CORNSEED LIMITED</span>
        <br />
        <span class="sub-title">Global Leading ISP Provider</span>
      </h1>
      <p class="subtitle">High-speed, Reliable, and Secure Enterprise Network Solutions</p>
      <div class="cta-buttons">
        <button class="btn btn-primary">Get Started</button>
        <button class="btn btn-secondary">Learn More</button>
      </div>
      <div class="stats">
        <div class="stat">
          <span class="stat-number">99.99%</span>
          <span class="stat-label">Uptime</span>
        </div>
        <div class="stat">
          <span class="stat-number">50+</span>
          <span class="stat-label">Cities Coverage</span>
        </div>
        <div class="stat">
          <span class="stat-number">10Gbps+</span>
          <span class="stat-label">Bandwidth Capacity</span>
        </div>
      </div>
    </div>
    <div class="floating-objects">
      <div class="float-item float-1"></div>
      <div class="float-item float-2"></div>
      <div class="float-item float-3"></div>
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
.hero {
  position: relative;
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
  background: #0f172a;
}

.background {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 0;
}

.animated-bg {
  position: absolute;
  width: 200%;
  height: 200%;
  background: linear-gradient(
    45deg,
    #0f172a 0%,
    #1e293b 25%,
    #0f172a 50%,
    #0d1b2a 75%,
    #0f172a 100%
  );
  animation: gradientShift 15s ease infinite;
}

@keyframes gradientShift {
  0% { transform: translate(0, 0); }
  50% { transform: translate(-50px, -50px); }
  100% { transform: translate(0, 0); }
}

.grid {
  position: absolute;
  width: 100%;
  height: 100%;
  background-image:
    linear-gradient(rgba(0, 212, 255, 0.1) 1px, transparent 1px),
    linear-gradient(90deg, rgba(0, 212, 255, 0.1) 1px, transparent 1px);
  background-size: 50px 50px;
  animation: gridMove 20s linear infinite;
}

@keyframes gridMove {
  0% { transform: translateY(0); }
  100% { transform: translateY(50px); }
}

.content {
  position: relative;
  z-index: 10;
  max-width: 900px;
  padding: 2rem;
  text-align: center;
  color: #fff;
}

.title {
  font-size: 4rem;
  font-weight: 800;
  margin-bottom: 1rem;
  line-height: 1.2;
}

.gradient-text {
  background: linear-gradient(135deg, #00d4ff, #0099ff, #7c3aed);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  animation: shimmer 3s ease-in-out infinite;
}

@keyframes shimmer {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.8; }
}

.sub-title {
  background: linear-gradient(135deg, #fbbf24, #f97316);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  font-size: 2rem;
}

.subtitle {
  font-size: 1.3rem;
  color: rgba(255, 255, 255, 0.7);
  margin-bottom: 2rem;
}

.cta-buttons {
  display: flex;
  gap: 1rem;
  justify-content: center;
  margin-bottom: 3rem;
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
  position: relative;
  overflow: hidden;
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

.stats {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  gap: 2rem;
  margin-top: 3rem;
}

.stat {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.5rem;
}

.stat-number {
  font-size: 2rem;
  font-weight: 700;
  background: linear-gradient(135deg, #00d4ff, #7c3aed);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.stat-label {
  color: rgba(255, 255, 255, 0.6);
  font-size: 0.9rem;
}

.floating-objects {
  position: absolute;
  width: 100%;
  height: 100%;
  z-index: 1;
  pointer-events: none;
}

.float-item {
  position: absolute;
  border-radius: 50%;
  opacity: 0.1;
}

.float-1 {
  width: 300px;
  height: 300px;
  background: linear-gradient(135deg, #00d4ff, #0099ff);
  top: 10%;
  right: 10%;
  animation: float1 20s ease-in-out infinite;
}

.float-2 {
  width: 200px;
  height: 200px;
  background: linear-gradient(135deg, #7c3aed, #0099ff);
  bottom: 20%;
  left: 10%;
  animation: float2 25s ease-in-out infinite;
}

.float-3 {
  width: 150px;
  height: 150px;
  background: linear-gradient(135deg, #fbbf24, #f97316);
  top: 50%;
  left: 50%;
  animation: float3 30s ease-in-out infinite;
}

@keyframes float1 {
  0%, 100% { transform: translate(0, 0); }
  50% { transform: translate(30px, -30px); }
}

@keyframes float2 {
  0%, 100% { transform: translate(0, 0); }
  50% { transform: translate(-30px, 30px); }
}

@keyframes float3 {
  0%, 100% { transform: translate(0, 0); }
  50% { transform: translate(20px, 20px); }
}

@media (max-width: 768px) {
  .title {
    font-size: 2rem;
  }

  .sub-title {
    font-size: 1.3rem;
  }

  .subtitle {
    font-size: 1rem;
  }

  .cta-buttons {
    flex-direction: column;
  }

  .btn {
    width: 100%;
  }
}
</style>
