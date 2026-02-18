<template>
  <div class="maintenance-container">
    <div class="maintenance-icon">🔧</div>
    <div class="logo">NETCORN</div>
    <h1>网站维护中</h1>
    <div class="maintenance-message">
      Our website is currently under scheduled maintenance, Please come back after Feb 18th UTC 14:00
    </div>
    <div class="timer">
      <div class="timer-label">预计恢复时间</div>
      <div class="timer-text">{{ recoveryTime }}</div>
    </div>
    <p class="thanks-text">感谢您的耐心等待</p>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const recoveryTime = ref('2026-02-18 14:00 UTC')
</script>

<style scoped>
.maintenance-container {
  text-align: center;
  padding: 40px 20px;
  max-width: 600px;
  background: rgba(255, 255, 255, 0.95);
  border-radius: 10px;
  box-shadow: 0 10px 40px rgba(0, 0, 0, 0.3);
}

.logo {
  font-size: 48px;
  font-weight: bold;
  color: #667eea;
  margin-bottom: 30px;
  letter-spacing: 2px;
}

h1 {
  font-size: 32px;
  color: #333;
  margin-bottom: 20px;
  font-weight: 600;
}

.maintenance-message {
  font-size: 18px;
  color: #666;
  line-height: 1.8;
  margin-bottom: 40px;
}

.maintenance-icon {
  font-size: 80px;
  margin-bottom: 20px;
  opacity: 0.8;
  animation: bounce 2s infinite;
}

@keyframes bounce {
  0%, 100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-10px);
  }
}

.timer {
  background: #f0f4ff;
  padding: 20px;
  border-radius: 8px;
  margin-bottom: 30px;
  border-left: 4px solid #667eea;
}

.timer-label {
  font-size: 14px;
  color: #999;
  margin-bottom: 10px;
  text-transform: uppercase;
  letter-spacing: 1px;
}

.timer-text {
  font-size: 24px;
  font-weight: bold;
  color: #667eea;
  font-family: 'Courier New', monospace;
}

.thanks-text {
  color: #999;
  font-size: 14px;
}

@media (max-width: 600px) {
  .maintenance-container {
    padding: 30px 20px;
  }

  h1 {
    font-size: 24px;
  }

  .maintenance-message {
    font-size: 16px;
  }

  .logo {
    font-size: 36px;
  }

  .maintenance-icon {
    font-size: 60px;
  }
}
</style>