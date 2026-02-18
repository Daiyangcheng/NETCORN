<template>
  <footer class="footer">
    <div class="container">
      <div class="footer-content">
        <div class="footer-section">
          <h4>About NETCORN</h4>
          <p>Global Leading ISP Provider for Premium Internet Connectivity</p>
          <div class="social-links">
            <!-- <a href="#" class="social-link">LinkedIn</a>
            <a href="#" class="social-link">Phone</a>
            <a href="#" class="social-link">Twitter</a> -->
          </div>
        </div>

        <div class="footer-section">
          <h4>Products & Services</h4>
          <ul>
            <li><a href="#services">Dedicated Access</a></li>
            <li><a href="#services">IP Transit</a></li>
            <li><a href="#services">Enterprise Security</a></li>
            <li><a href="#services">Professional Support</a></li>
          </ul>
        </div>

        <div class="footer-section">
          <h4>Company</h4>
          <ul>
            <li><a href="#about">About Us</a></li>
            <li><a href="#">News</a></li>
            <li><a href="#">Careers</a></li>
            <li><a href="#">Contact</a></li>
          </ul>
        </div>

        <div class="footer-section">
          <h4>Contact Us</h4>
          <p>Phone: +44 7763 181183</p>
          <p>Email: shawnliu@netcorn.net</p>
          <p>Address: London, UK</p>
        </div>
      </div>

      <div class="footer-bottom">
        <p>&copy; 2026 NETCORN | CORNSEED LIMITED. All Rights Reserved.</p>
      </div>
    </div>
  </footer>
</template>

<script setup>
</script>

<style scoped>
.footer {
  background: #0a0f1e;
  border-top: 1px solid rgba(0, 212, 255, 0.1);
  color: rgba(255, 255, 255, 0.8);
  padding: 4rem 2rem 2rem;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

.footer-content {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
  margin-bottom: 2rem;
}

.footer-section h4 {
  color: #fff;
  font-size: 1.1rem;
  margin-bottom: 1rem;
  font-weight: 600;
}

.footer-section p {
  line-height: 1.6;
  margin-bottom: 0.5rem;
  font-size: 0.95rem;
}

.footer-section ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.footer-section li {
  margin-bottom: 0.8rem;
}

.footer-section a {
  color: rgba(255, 255, 255, 0.6);
  text-decoration: none;
  transition: color 0.3s ease;
}

.footer-section a:hover {
  color: #00d4ff;
}

.social-links {
  display: flex;
  gap: 1rem;
  margin-top: 1rem;
}

.social-link {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background: rgba(0, 212, 255, 0.1);
  transition: all 0.3s ease;
  font-size: 1.2rem;
}

.social-link:hover {
  background: rgba(0, 212, 255, 0.3);
  transform: translateY(-3px);
}

.footer-bottom {
  border-top: 1px solid rgba(255, 255, 255, 0.1);
  padding-top: 2rem;
  text-align: center;
  color: rgba(255, 255, 255, 0.5);
  font-size: 0.9rem;
}

@media (max-width: 768px) {
  .footer-content {
    grid-template-columns: 1fr;
  }
}
</style>
