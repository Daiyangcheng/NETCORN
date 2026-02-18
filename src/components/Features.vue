<template>
  <section id="features" class="features">
    <div class="container">
      <h2 class="section-title">Core Advantages</h2>

      <div class="features-content">
        <div v-for="(feature, index) in features" :key="feature.id" class="feature-item" :class="{ 'right': index % 2 === 1 }">
          <div class="feature-image">
            <div class="image-placeholder">{{ feature.icon }}</div>
          </div>
          <div class="feature-text">
            <h3>{{ feature.title }}</h3>
            <p>{{ feature.description }}</p>
            <ul>
              <li v-for="point in feature.points" :key="point">{{ point }}</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const features = [
  {
    id: 1,
    icon: 'SPEED',
    title: 'Ultra-Low Latency',
    description: 'Optimized network architecture ensures data transmission latency below 10ms',
    points: ['Direct Backbone Connection', 'Intelligent Routing', 'Real-Time Transfer']
  },
  {
    id: 2,
    icon: 'SECURE',
    title: 'High Reliability',
    description: '99.99% uptime guarantee ensures business continuity',
    points: ['Multi-Route Redundancy', 'Automatic Failover', 'Real-Time Backup']
  },
  {
    id: 3,
    icon: 'ECONOMY',
    title: 'Cost Optimization',
    description: 'Flexible billing model to save costs on your terms',
    points: ['Pay-as-You-Go', 'Long-term Discounts', 'No Hidden Fees']
  },
  {
    id: 4,
    icon: 'EASY',
    title: 'Simple Deployment',
    description: 'Quick launch with completion in as little as 24 hours',
    points: ['One-Click Configuration', 'No Installation Required', 'Fast Delivery']
  }
];
</script>

<style scoped>
.features {
  padding: 6rem 2rem;
  background: #0f172a;
  position: relative;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

.section-title {
  font-size: 3rem;
  font-weight: 800;
  text-align: center;
  color: #fff;
  margin-bottom: 4rem;
}

.features-content {
  display: flex;
  flex-direction: column;
  gap: 4rem;
}

.feature-item {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 3rem;
  align-items: center;
}

.feature-item.right {
  grid-template-columns: 1fr 1fr;
  direction: rtl;
}

.feature-item.right > * {
  direction: ltr;
}

.feature-image {
  display: flex;
  justify-content: center;
  align-items: center;
}

.image-placeholder {
  width: 300px;
  height: 300px;
  background: linear-gradient(135deg, rgba(0, 212, 255, 0.2), rgba(124, 58, 237, 0.2));
  border: 2px solid rgba(0, 212, 255, 0.3);
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 2rem;
  font-weight: 700;
  color: #00d4ff;
  text-transform: uppercase;
  letter-spacing: 2px;
  transition: all 0.3s ease;
}

.feature-item:hover .image-placeholder {
  border-color: rgba(0, 212, 255, 0.6);
  background: linear-gradient(135deg, rgba(0, 212, 255, 0.3), rgba(124, 58, 237, 0.3));
  transform: scale(1.05);
}

.feature-text h3 {
  font-size: 2rem;
  color: #fff;
  margin-bottom: 1rem;
}

.feature-text p {
  color: rgba(255, 255, 255, 0.7);
  font-size: 1.1rem;
  margin-bottom: 1.5rem;
  line-height: 1.6;
}

.feature-text ul {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  flex-direction: column;
  gap: 0.8rem;
}

.feature-text li {
  color: rgba(255, 255, 255, 0.6);
  padding-left: 2rem;
  position: relative;
}

.feature-text li::before {
  content: '▸';
  position: absolute;
  left: 0;
  color: #00d4ff;
  font-weight: bold;
}

@media (max-width: 968px) {
  .feature-item,
  .feature-item.right {
    grid-template-columns: 1fr;
  }

  .image-placeholder {
    width: 200px;
    height: 200px;
    font-size: 5rem;
  }

  .section-title {
    font-size: 2rem;
  }
}
</style>
