<template>
  <q-page class="home-page">
    <!-- ================= HERO ================= -->
    <section class="hero-section">
      <!-- Animated background -->
      <div class="hero-grid"></div>
      <div class="glow glow-1"></div>
      <div class="glow glow-2"></div>
      <div class="glow glow-3"></div>

      <!-- Floating particles -->
      <span
        v-for="n in 25"
        :key="n"
        class="particle"
        :style="particleStyle(n)"
      ></span>

      <div class="container hero-container">
        <div class="row items-center q-col-gutter-xl">
          <!-- Hero Content -->
          <div class="col-12 col-md-6">
            <div class="hero-content">
              <div class="welcome-badge">
                <q-icon name="auto_awesome" size="18px" />
                <span>WELCOME TO OUR WEBSITE</span>
              </div>

              <h1 class="hero-title">
                Build Something
                <span>Amazing</span>
                With Us
              </h1>

              <p class="hero-description">
                We create modern, simple and powerful digital solutions that
                help businesses grow, succeed and stand out.
              </p>

              <div class="hero-buttons">
                <q-btn
                  unelevated
                  label="Get Started"
                  icon-right="arrow_forward"
                  class="btn-main"
                  size="lg"
                />

                <q-btn
                  outline
                  label="Learn More"
                  icon="play_circle"
                  class="btn-learn"
                  size="lg"
                />
              </div>

              <!-- Stats -->
              <div class="stats-row">
                <div class="stat">
                  <strong>500+</strong>
                  <span>Happy Clients</span>
                </div>

                <div class="stat">
                  <strong>100+</strong>
                  <span>Projects Done</span>
                </div>

                <div class="stat">
                  <strong>24/7</strong>
                  <span>Support</span>
                </div>
              </div>
            </div>
          </div>

          <!-- Hero Visual -->
          <div class="col-12 col-md-6">
            <div class="hero-visual">
              <div class="orbit orbit-1"></div>
              <div class="orbit orbit-2"></div>

              <div class="main-visual">
                <q-icon name="rocket_launch" size="110px" class="rocket-icon" />
              </div>

              <div class="floating-card card-top">
                <q-icon name="code" />
                <span>Clean Code</span>
              </div>

              <div class="floating-card card-right">
                <q-icon name="favorite" />
                <span>Modern Design</span>
              </div>

              <div class="floating-card card-bottom">
                <q-icon name="trending_up" />
                <span>Business Growth</span>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="scroll-indicator">
        <q-icon name="keyboard_arrow_down" size="34px" />
      </div>
    </section>

    <!-- ================= FEATURES ================= -->
    <section class="features-section">
      <div class="background-circle circle-1"></div>
      <div class="background-circle circle-2"></div>

      <div class="container">
        <div class="section-heading text-center">
          <div class="section-label">
            <q-icon name="auto_awesome" />
            OUR FEATURES
          </div>

          <h2 class="section-title">Everything You Need</h2>

          <p class="section-description">
            Simple and powerful features designed to make your work easier.
          </p>
        </div>

        <div class="row q-col-gutter-lg">
          <!-- Feature 1 -->
          <div
            v-for="(feature, index) in features"
            :key="feature.title"
            class="col-12 col-sm-6 col-md-4"
          >
            <q-card
              flat
              class="feature-card"
              :style="{ animationDelay: `${index * 0.1}s` }"
            >
              <q-card-section>
                <div class="feature-icon">
                  <q-icon :name="feature.icon" size="35px" />
                </div>

                <h3>{{ feature.title }}</h3>

                <p>
                  {{ feature.description }}
                </p>

                <q-btn
                  flat
                  no-caps
                  label="Learn more"
                  icon-right="arrow_forward"
                  class="feature-link"
                />
              </q-card-section>
            </q-card>
          </div>
        </div>
      </div>
    </section>

    <!-- ================= CTA ================= -->
    <section class="cta-section">
      <div class="container">
        <div class="cta-box">
          <div class="cta-glow"></div>

          <div class="row items-center q-col-gutter-xl">
            <div class="col-12 col-md-8">
              <div class="section-label light">
                <q-icon name="rocket_launch" />
                LET'S BUILD TOGETHER
              </div>

              <h2>Ready to Get Started?</h2>

              <p>
                Start your journey with us today and create something amazing.
              </p>
            </div>

            <div class="col-12 col-md-4 text-md-right">
              <q-btn
                unelevated
                label="Start Now"
                icon-right="arrow_forward"
                size="lg"
                class="cta-button"
              />
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- ================= FOOTER ================= -->
    <footer class="footer">
      <div class="container">
        <div class="row items-center justify-between">
          <div>
            <div class="footer-logo">Quasar Fardaus</div>

            <div class="footer-copy">
              © 2026 Quasar Fardaus. All Rights Reserved.
            </div>
          </div>

          <div class="social-links">
            <q-btn flat round icon="facebook" />

            <q-btn flat round icon="language" />

            <q-btn flat round icon="email" />
          </div>
        </div>
      </div>
    </footer>
  </q-page>
</template>

<script setup>
const features = [
  {
    icon: "speed",
    title: "Fast Performance",
    description: "Enjoy a fast and smooth experience on every device.",
  },
  {
    icon: "devices",
    title: "Responsive Design",
    description: "Our website works perfectly on mobile, tablet and desktop.",
  },
  {
    icon: "security",
    title: "Secure & Reliable",
    description:
      "Your data and information are protected with modern security.",
  },
  {
    icon: "support_agent",
    title: "24/7 Support",
    description: "Get help anytime you need it from our dedicated team.",
  },
  {
    icon: "trending_up",
    title: "Business Growth",
    description: "Powerful tools designed to help your business grow faster.",
  },
  {
    icon: "settings",
    title: "Easy Customization",
    description: "Customize and manage everything easily from one place.",
  },
];

const particleStyle = (index) => {
  const left = (index * 37) % 100;
  const delay = (index * 0.35) % 6;
  const duration = 5 + (index % 5);

  return {
    left: `${left}%`,
    animationDelay: `${delay}s`,
    animationDuration: `${duration}s`,
  };
};
</script>

<style scoped>
/* ========================================
   GLOBAL
======================================== */

.home-page {
  overflow: hidden;
  background: #f7f9ff;
  color: #172033;
}

.container {
  width: 90%;
  max-width: 1200px;
  margin: 0 auto;
}

/* ========================================
   HERO
======================================== */

.hero-section {
  position: relative;
  min-height: 780px;
  display: flex;
  align-items: center;
  overflow: hidden;
  color: white;
  background:
    radial-gradient(circle at 80% 20%, rgba(79, 70, 229, 0.8), transparent 35%),
    radial-gradient(
      circle at 15% 80%,
      rgba(14, 165, 233, 0.5),
      transparent 30%
    ),
    linear-gradient(135deg, #07133f 0%, #102d91 45%, #1554d1 100%);
}

.hero-grid {
  position: absolute;
  inset: 0;
  opacity: 0.15;
  background-image:
    linear-gradient(rgba(255, 255, 255, 0.15) 1px, transparent 1px),
    linear-gradient(90deg, rgba(255, 255, 255, 0.15) 1px, transparent 1px);
  background-size: 55px 55px;
  mask-image: linear-gradient(to bottom, black, transparent);
}

.glow {
  position: absolute;
  border-radius: 50%;
  filter: blur(10px);
  animation: glowMove 8s ease-in-out infinite alternate;
}

.glow-1 {
  width: 300px;
  height: 300px;
  background: rgba(59, 130, 246, 0.25);
  top: -100px;
  left: -80px;
}

.glow-2 {
  width: 400px;
  height: 400px;
  background: rgba(139, 92, 246, 0.2);
  right: -150px;
  top: 100px;
  animation-delay: 2s;
}

.glow-3 {
  width: 250px;
  height: 250px;
  background: rgba(6, 182, 212, 0.2);
  bottom: -100px;
  left: 40%;
  animation-delay: 4s;
}

.hero-container {
  position: relative;
  z-index: 5;
}

.hero-content {
  animation: fadeUp 1s ease both;
}

.welcome-badge {
  width: fit-content;
  display: flex;
  align-items: center;
  gap: 9px;
  padding: 10px 18px;
  margin-bottom: 25px;
  border: 1px solid rgba(255, 255, 255, 0.25);
  border-radius: 50px;
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(15px);
  font-size: 13px;
  font-weight: 700;
  letter-spacing: 1px;
}

.hero-title {
  margin: 0 0 25px;
  font-size: clamp(45px, 5vw, 68px);
  line-height: 1.05;
  font-weight: 800;
  letter-spacing: -2px;
}

.hero-title span {
  display: inline-block;
  background: linear-gradient(90deg, #67e8f9, #a78bfa, #f0abfc);
  background-size: 200% auto;
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  animation: gradientText 4s linear infinite;
}

.hero-description {
  max-width: 570px;
  margin-bottom: 30px;
  color: rgba(255, 255, 255, 0.75);
  font-size: 18px;
  line-height: 1.8;
}

.hero-buttons {
  display: flex;
  flex-wrap: wrap;
  gap: 14px;
}

.btn-main {
  padding: 0 30px;
  border-radius: 12px;
  background: linear-gradient(90deg, #06b6d4, #6366f1, #a855f7);
  box-shadow: 0 12px 30px rgba(79, 70, 229, 0.4);
  transition: 0.3s ease;
}

.btn-main:hover {
  transform: translateY(-4px);
  box-shadow: 0 18px 40px rgba(79, 70, 229, 0.5);
}

.btn-learn {
  padding: 0 25px;
  color: white !important;
  border-color: rgba(255, 255, 255, 0.5);
  border-radius: 12px;
}

.stats-row {
  display: flex;
  gap: 45px;
  margin-top: 55px;
}

.stat {
  display: flex;
  flex-direction: column;
}

.stat strong {
  font-size: 28px;
  font-weight: 800;
}

.stat span {
  margin-top: 5px;
  color: rgba(255, 255, 255, 0.6);
  font-size: 13px;
}

/* ========================================
   HERO VISUAL
======================================== */

.hero-visual {
  position: relative;
  width: 500px;
  height: 500px;
  max-width: 100%;
  margin: auto;
  display: flex;
  align-items: center;
  justify-content: center;
  animation: fadeIn 1.2s ease both;
}

.main-visual {
  width: 260px;
  height: 260px;
  display: flex;
  align-items: center;
  justify-content: center;
  border: 1px solid rgba(255, 255, 255, 0.35);
  border-radius: 45px;
  background: linear-gradient(
    135deg,
    rgba(255, 255, 255, 0.25),
    rgba(255, 255, 255, 0.08)
  );
  backdrop-filter: blur(20px);
  box-shadow:
    0 30px 80px rgba(0, 0, 0, 0.25),
    inset 0 1px rgba(255, 255, 255, 0.4);
  transform: rotate(-5deg);
  animation: floating 5s ease-in-out infinite;
}

.rocket-icon {
  filter: drop-shadow(0 15px 20px rgba(255, 255, 255, 0.3));
}

.orbit {
  position: absolute;
  border: 1px solid rgba(255, 255, 255, 0.18);
  border-radius: 50%;
}

.orbit-1 {
  width: 390px;
  height: 390px;
  animation: rotate 12s linear infinite;
}

.orbit-2 {
  width: 470px;
  height: 470px;
  animation: rotateReverse 18s linear infinite;
}

.floating-card {
  position: absolute;
  z-index: 10;
  min-width: 145px;
  display: flex;
  align-items: center;
  gap: 10px;
  padding: 15px 18px;
  border: 1px solid rgba(255, 255, 255, 0.3);
  border-radius: 16px;
  background: rgba(255, 255, 255, 0.12);
  backdrop-filter: blur(18px);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
  font-size: 14px;
  font-weight: 600;
}

.floating-card q-icon {
  font-size: 25px;
}

.card-top {
  top: 55px;
  left: 10px;
  animation: floating 4s ease-in-out infinite;
}

.card-right {
  right: 0;
  top: 170px;
  animation: floating 4.5s ease-in-out infinite 1s;
}

.card-bottom {
  bottom: 50px;
  left: 80px;
  animation: floating 5s ease-in-out infinite 2s;
}

.scroll-indicator {
  position: absolute;
  z-index: 10;
  bottom: 20px;
  left: 50%;
  transform: translateX(-50%);
  animation: bounce 2s infinite;
}

/* ========================================
   PARTICLES
======================================== */

.particle {
  position: absolute;
  top: 100%;
  width: 4px;
  height: 4px;
  border-radius: 50%;
  background: white;
  opacity: 0.7;
  animation: particleMove linear infinite;
}

/* ========================================
   FEATURES
======================================== */

.features-section {
  position: relative;
  padding: 110px 0;
  overflow: hidden;
  background:
    radial-gradient(
      circle at 20% 30%,
      rgba(59, 130, 246, 0.08),
      transparent 30%
    ),
    #f8faff;
}

.background-circle {
  position: absolute;
  border-radius: 50%;
  background: rgba(59, 130, 246, 0.06);
}

.circle-1 {
  width: 350px;
  height: 350px;
  left: -180px;
  top: 100px;
}

.circle-2 {
  width: 280px;
  height: 280px;
  right: -130px;
  bottom: 50px;
}

.section-heading {
  position: relative;
  z-index: 2;
  margin-bottom: 60px;
}

.section-label {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  color: #2563eb;
  font-size: 13px;
  font-weight: 800;
  letter-spacing: 1.5px;
}

.section-title {
  margin: 12px 0;
  color: #111b3d;
  font-size: clamp(34px, 4vw, 48px);
  font-weight: 800;
}

.section-description {
  max-width: 600px;
  margin: auto;
  color: #64748b;
  font-size: 17px;
}

.feature-card {
  position: relative;
  height: 100%;
  overflow: hidden;
  border: 1px solid rgba(59, 130, 246, 0.12);
  border-radius: 22px;
  background: rgba(255, 255, 255, 0.85);
  box-shadow: 0 10px 35px rgba(30, 64, 175, 0.06);
  transition:
    transform 0.4s ease,
    box-shadow 0.4s ease;
  animation: cardAppear 0.7s ease both;
}

.feature-card::before {
  content: "";
  position: absolute;
  width: 120px;
  height: 120px;
  right: -50px;
  top: -50px;
  border-radius: 50%;
  background: rgba(59, 130, 246, 0.07);
  transition: 0.4s ease;
}

.feature-card:hover {
  transform: translateY(-12px);
  box-shadow: 0 25px 60px rgba(30, 64, 175, 0.13);
}

.feature-card:hover::before {
  transform: scale(2);
}

.feature-card q-card-section {
  padding: 35px 30px;
}

.feature-icon {
  width: 72px;
  height: 72px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 25px;
  border-radius: 20px;
  color: #2563eb;
  background: linear-gradient(135deg, #eff6ff, #dbeafe);
  transition: 0.4s ease;
}

.feature-card:hover .feature-icon {
  transform: rotate(-8deg) scale(1.08);
}

.feature-card h3 {
  margin: 0 0 12px;
  color: #172554;
  font-size: 21px;
  font-weight: 800;
}

.feature-card p {
  min-height: 50px;
  margin: 0;
  color: #64748b;
  line-height: 1.7;
}

.feature-link {
  margin-top: 20px;
  padding-left: 0;
  color: #2563eb;
  font-weight: 700;
}

/* ========================================
   CTA
======================================== */

.cta-section {
  padding: 30px 0 100px;
  background: #f8faff;
}

.cta-box {
  position: relative;
  overflow: hidden;
  padding: 60px;
  border-radius: 30px;
  color: white;
  background:
    radial-gradient(
      circle at 90% 20%,
      rgba(168, 85, 247, 0.5),
      transparent 35%
    ),
    linear-gradient(135deg, #1d4ed8, #4338ca, #7c3aed);
  box-shadow: 0 30px 70px rgba(67, 56, 202, 0.25);
}

.cta-glow {
  position: absolute;
  width: 250px;
  height: 250px;
  right: -80px;
  bottom: -120px;
  border-radius: 50%;
  background: rgba(255, 255, 255, 0.12);
}

.section-label.light {
  color: rgba(255, 255, 255, 0.85);
}

.cta-box h2 {
  position: relative;
  margin: 15px 0 10px;
  font-size: clamp(32px, 4vw, 44px);
  font-weight: 800;
}

.cta-box p {
  position: relative;
  margin: 0;
  color: rgba(255, 255, 255, 0.75);
  font-size: 17px;
}

.cta-button {
  padding: 0 30px;
  border-radius: 12px;
  color: #3730a3;
  background: white;
  transition: 0.3s ease;
}

.cta-button:hover {
  transform: translateY(-4px) scale(1.03);
  box-shadow: 0 15px 35px rgba(0, 0, 0, 0.2);
}

/* ========================================
   FOOTER
======================================== */

.footer {
  padding: 35px 0;
  background: white;
  border-top: 1px solid #e5e7eb;
}

.footer-logo {
  color: #172554;
  font-size: 20px;
  font-weight: 800;
}

.footer-copy {
  margin-top: 6px;
  color: #94a3b8;
  font-size: 13px;
}

.social-links {
  display: flex;
  gap: 5px;
}

.social-links .q-btn {
  color: #2563eb;
  background: #eff6ff;
}

/* ========================================
   ANIMATIONS
======================================== */

@keyframes fadeUp {
  from {
    opacity: 0;
    transform: translateY(35px);
  }

  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: scale(0.9);
  }

  to {
    opacity: 1;
    transform: scale(1);
  }
}

@keyframes floating {
  0%,
  100% {
    transform: translateY(0) rotate(-5deg);
  }

  50% {
    transform: translateY(-15px) rotate(-3deg);
  }
}

@keyframes gradientText {
  to {
    background-position: 200% center;
  }
}

@keyframes glowMove {
  from {
    transform: translate(0, 0) scale(1);
  }

  to {
    transform: translate(40px, 30px) scale(1.15);
  }
}

@keyframes rotate {
  to {
    transform: rotate(360deg);
  }
}

@keyframes rotateReverse {
  to {
    transform: rotate(-360deg);
  }
}

@keyframes bounce {
  0%,
  100% {
    transform: translateX(-50%) translateY(0);
  }

  50% {
    transform: translateX(-50%) translateY(10px);
  }
}

@keyframes particleMove {
  from {
    transform: translateY(0) scale(0);
    opacity: 0;
  }

  15% {
    opacity: 0.8;
  }

  85% {
    opacity: 0.5;
  }

  to {
    transform: translateY(-900px) scale(1);
    opacity: 0;
  }
}

@keyframes cardAppear {
  from {
    opacity: 0;
    transform: translateY(30px);
  }

  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ========================================
   RESPONSIVE
======================================== */

@media (max-width: 900px) {
  .hero-section {
    min-height: auto;
    padding: 100px 0 80px;
  }

  .hero-visual {
    width: 430px;
    height: 430px;
    margin-top: 40px;
  }

  .stats-row {
    gap: 25px;
  }

  .cta-box {
    padding: 45px 35px;
  }
}

@media (max-width: 600px) {
  .container {
    width: 92%;
  }

  .hero-section {
    padding: 70px 0;
  }

  .hero-title {
    font-size: 43px;
    letter-spacing: -1px;
  }

  .hero-description {
    font-size: 16px;
  }

  .hero-buttons {
    flex-direction: column;
  }

  .btn-main,
  .btn-learn {
    width: 100%;
  }

  .stats-row {
    justify-content: space-between;
    gap: 10px;
    margin-top: 40px;
  }

  .stat strong {
    font-size: 22px;
  }

  .stat span {
    font-size: 11px;
  }

  .hero-visual {
    width: 320px;
    height: 350px;
  }

  .main-visual {
    width: 190px;
    height: 190px;
    border-radius: 30px;
  }

  .rocket-icon {
    font-size: 75px !important;
  }

  .orbit-1 {
    width: 270px;
    height: 270px;
  }

  .orbit-2 {
    width: 320px;
    height: 320px;
  }

  .floating-card {
    min-width: auto;
    padding: 11px 13px;
    font-size: 11px;
  }

  .card-top {
    left: 0;
    top: 40px;
  }

  .card-right {
    right: -5px;
    top: 130px;
  }

  .card-bottom {
    left: 25px;
    bottom: 30px;
  }

  .features-section {
    padding: 80px 0;
  }

  .section-heading {
    margin-bottom: 40px;
  }

  .feature-card q-card-section {
    padding: 30px 25px;
  }

  .cta-section {
    padding-bottom: 70px;
  }

  .cta-box {
    padding: 40px 25px;
    border-radius: 24px;
  }

  .cta-button {
    width: 100%;
    margin-top: 25px;
  }

  .footer {
    text-align: center;
  }

  .footer .row {
    gap: 20px;
    justify-content: center;
  }

  .social-links {
    justify-content: center;
  }
}
</style>
