<template>
  <section id="services" class="services">
    <div class="container">
      <h2 class="section-title">Our Services</h2>
      <p class="section-subtitle">Enterprise-Grade Internet Solutions</p>

      <div class="services-grid">
        <div v-for="service in services" :key="service.id" class="service-card">
          <!-- <div class="icon">{{ service.icon }}</div> -->
          <h3>{{ service.title }}</h3>
          <p>{{ service.description }}</p>
          <ul class="features">
            <li v-for="feature in service.features" :key="feature">{{ feature }}</li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const services = [
  {
    id: 1,
    icon: '⚡',
    title: 'Dedicated Internet Access',
    description: 'High-speed fiber optic connectivity from 10Gbps to 100Gbps',
    features: ['Low Latency', 'High Availability', 'Symmetric Bandwidth', '24/7 Monitoring']
  },
  {
    id: 2,
    icon: '🔒',
    title: 'Enterprise Security',
    description: 'Multi-layer protection ensures secure data transmission',
    features: ['DDoS Protection', 'Firewall Services', 'VPN Encryption', '24/7 Security Monitoring']
  },
  {
    id: 3,
    icon: '🌐',
    title: 'IP Transit',
    description: 'Global IP routing and Internet backbone connectivity',
    features: ['Multiple Carriers', 'BGP Routing', 'Full Route Table', 'Anycast Support']
  },
  {
    id: 4,
    icon: '📍',
    title: 'National Coverage',
    description: 'Present in 50+ cities for multi-point connectivity',
    features: ['Multi-Point Access', 'Flexible Expansion', 'Fast Deployment', 'Redundancy Guarantee']
  },
  {
    id: 5,
    icon: '💼',
    title: 'Professional Support',
    description: '24×7 technical support team always ready to assist',
    features: ['Technical Support', 'Troubleshooting', 'Performance Optimization', 'Regular Maintenance']
  },
  {
    id: 6,
    icon: '📊',
    title: 'Intelligent Management',
    description: 'Real-time monitoring and visual management platform',
    features: ['Traffic Analytics', 'Cost Optimization', 'Performance Reports', 'Smart Alerts']
  },
  {
    id: 7,
    icon: '🌍',
    title: 'Global Interconnection',
    description: 'Connect with global data centers and major carriers',
    features: ['International Routes', 'Cross-Border Access', 'Multiple Carriers', 'Low Latency']
  }
];
</script>

<style scoped>
.services {
  padding: 6rem 2rem;
  background: linear-gradient(180deg, #0f172a 0%, #1e293b 100%);
  position: relative;
}

.services::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background:
    radial-gradient(circle at 20% 50%, rgba(0, 212, 255, 0.1) 0%, transparent 50%),
    radial-gradient(circle at 80% 80%, rgba(124, 58, 237, 0.1) 0%, transparent 50%);
  pointer-events: none;
  z-index: 0;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  position: relative;
  z-index: 1;
}

.section-title {
  font-size: 3rem;
  font-weight: 800;
  text-align: center;
  color: #fff;
  margin-bottom: 1rem;
}

.section-subtitle {
  font-size: 1.2rem;
  text-align: center;
  color: rgba(255, 255, 255, 0.6);
  margin-bottom: 3rem;
}

.services-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
}

.service-card {
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid rgba(0, 212, 255, 0.2);
  border-radius: 12px;
  padding: 2rem;
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

.service-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(
    90deg,
    transparent,
    rgba(0, 212, 255, 0.2),
    transparent
  );
  animation: shine 3s ease-in-out infinite;
  z-index: -1;
}

@keyframes shine {
  0% { left: -100%; }
  50% { left: 100%; }
  100% { left: 100%; }
}

.service-card:hover {
  border-color: rgba(0, 212, 255, 0.5);
  background: rgba(255, 255, 255, 0.08);
  transform: translateY(-10px);
  box-shadow: 0 20px 40px rgba(0, 212, 255, 0.2);
}

.icon {
  font-size: 2.5rem;
  margin-bottom: 1rem;
  animation: bounce 2s ease-in-out infinite;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  width: 70px;
  height: 70px;
  background: linear-gradient(135deg, rgba(0, 212, 255, 0.1), rgba(124, 58, 237, 0.1));
  border-radius: 12px;
  font-weight: 600;
  color: #00d4ff;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-size: 0.8rem;
}

.service-card:nth-child(1) .icon { animation-delay: 0s; }
.service-card:nth-child(2) .icon { animation-delay: 0.2s; }
.service-card:nth-child(3) .icon { animation-delay: 0.4s; }
.service-card:nth-child(4) .icon { animation-delay: 0.6s; }
.service-card:nth-child(5) .icon { animation-delay: 0.8s; }
.service-card:nth-child(6) .icon { animation-delay: 1s; }

@keyframes bounce {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-10px); }
}

.service-card h3 {
  font-size: 1.5rem;
  color: #fff;
  margin-bottom: 1rem;
}

.service-card p {
  color: rgba(255, 255, 255, 0.7);
  margin-bottom: 1.5rem;
  font-size: 0.95rem;
}

.features {
  list-style: none;
  padding: 0;
  margin: 0;
}

.features li {
  color: rgba(255, 255, 255, 0.6);
  padding: 0.5rem 0 0.5rem 1.5rem;
  font-size: 0.9rem;
  position: relative;
}

.features li::before {
  content: '•';
  position: absolute;
  left: 0;
  color: #00d4ff;
  font-weight: bold;
}

@media (max-width: 768px) {
  .section-title {
    font-size: 2rem;
  }

  .services-grid {
    grid-template-columns: 1fr;
  }
}
</style>
