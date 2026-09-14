<template>
  <q-page class="home-page">
    <!-- Hero Section -->
    <section class="hero-section">
      <div class="container">
        <div class="row items-center q-col-gutter-xl">
          <!-- Left Content -->
          <div class="col-12 col-md-6">
            <div class="hero-content">
              <div class="text-primary text-weight-bold q-mb-md">
                WELCOME TO OUR WEBSITE
              </div>

              <h1 class="hero-title">
                Build Something
                <span class="text-primary">Amazing</span>
                With Us
              </h1>

              <p class="hero-description">
                We create modern, simple and powerful digital solutions that
                help businesses grow and succeed.
              </p>

              <div class="q-gutter-sm">
                <q-btn
                  color="primary"
                  label="Get Started"
                  unelevated
                  size="lg"
                  class="btn-primary"
                />

                <q-btn outline color="primary" label="Learn More" size="lg" />
              </div>
            </div>
          </div>

          <!-- Right Image -->
          <div class="col-12 col-md-6">
            <div class="hero-image">
              <div class="image-box">
                <q-icon name="web" size="150px" color="primary" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Features Section -->
    <section class="features-section">
      <div class="container">
        <div class="section-heading text-center">
          <div class="text-primary text-weight-bold">OUR FEATURES</div>

          <h2 class="section-title">Everything You Need</h2>

          <p class="section-description">
            Simple and powerful features designed to make your work easier.
          </p>
        </div>

        <div class="row q-col-gutter-lg">
          <div class="col-12 col-sm-6 col-md-4">
            <q-card class="feature-card">
              <q-card-section class="text-center">
                <q-icon name="speed" color="primary" size="55px" />

                <h3>Fast Performance</h3>

                <p>Enjoy a fast and smooth experience on every device.</p>
              </q-card-section>
            </q-card>
          </div>

          <div class="col-12 col-sm-6 col-md-4">
            <q-card class="feature-card">
              <q-card-section class="text-center">
                <q-icon name="devices" color="primary" size="55px" />

                <h3>Responsive Design</h3>

                <p>
                  Our website works perfectly on mobile, tablet and desktop.
                </p>
              </q-card-section>
            </q-card>
          </div>

          <div class="col-12 col-sm-6 col-md-4">
            <q-card class="feature-card">
              <q-card-section class="text-center">
                <q-icon name="security" color="primary" size="55px" />

                <h3>Secure & Reliable</h3>

                <p>
                  Your data and information are protected with modern security.
                </p>
              </q-card-section>
            </q-card>
          </div>
        </div>
      </div>
    </section>

    <!-- About / CTA Section -->
    <section class="cta-section">
      <div class="container">
        <div class="cta-box">
          <div class="row items-center q-col-gutter-lg">
            <div class="col-12 col-md-8">
              <h2>Ready to Get Started?</h2>

              <p>
                Start your journey with us today and create something great.
              </p>
            </div>

            <div class="col-12 col-md-4 text-md-right">
              <q-btn
                color="white"
                text-color="primary"
                label="Start Now"
                size="lg"
                unelevated
              />
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
      <div class="container">
        <div class="row items-center justify-between">
          <div>
            <div class="text-h6 text-weight-bold">Quasar Fardaus</div>

            <div class="text-grey-6">
              © 2026 Quasar Fardaus. All Rights Reserved.
            </div>
          </div>

          <div class="q-gutter-sm">
            <q-btn flat round icon="facebook" />
            <q-btn flat round icon="language" />
            <q-btn flat round icon="email" />
          </div>
        </div>
      </div>
    </footer>
  </q-page>
</template>

<style scoped>
.home-page {
  background: #f8fafc;
}

/* Container */
.container {
  width: 90%;
  max-width: 1200px;
  margin: 0 auto;
}

/* Hero */
.hero-section {
  min-height: 650px;
  display: flex;
  align-items: center;
  background: white;
  padding: 80px 0;
}

.hero-title {
  font-size: 58px;
  line-height: 1.1;
  font-weight: 800;
  margin: 0 0 25px;
  color: #172033;
}

.hero-description {
  font-size: 18px;
  line-height: 1.7;
  color: #64748b;
  max-width: 550px;
  margin-bottom: 30px;
}

.btn-primary {
  padding: 0 28px;
}

.hero-image {
  display: flex;
  justify-content: center;
  align-items: center;
}

.image-box {
  width: 400px;
  height: 400px;
  border-radius: 30px;
  background: #eaf2ff;
  display: flex;
  justify-content: center;
  align-items: center;
}

/* Features */
.features-section {
  padding: 90px 0;
}

.section-heading {
  margin-bottom: 50px;
}

.section-title {
  font-size: 40px;
  font-weight: 800;
  color: #172033;
  margin: 10px 0;
}

.section-description {
  color: #64748b;
  font-size: 17px;
}

.feature-card {
  height: 100%;
  border-radius: 18px;
  padding: 20px;
  transition: 0.3s;
  border: 1px solid #e5e7eb;
}

.feature-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 15px 35px rgba(0, 0, 0, 0.08);
}

.feature-card h3 {
  font-size: 22px;
  margin: 20px 0 10px;
  color: #172033;
}

.feature-card p {
  color: #64748b;
  line-height: 1.6;
}

/* CTA */
.cta-section {
  padding: 30px 0 90px;
}

.cta-box {
  background: #1976d2;
  color: white;
  padding: 50px;
  border-radius: 25px;
}

.cta-box h2 {
  font-size: 36px;
  font-weight: 800;
  margin: 0 0 10px;
}

.cta-box p {
  font-size: 17px;
  margin: 0;
  opacity: 0.9;
}

/* Footer */
.footer {
  background: white;
  padding: 30px 0;
  border-top: 1px solid #e5e7eb;
}

/* Mobile */
@media (max-width: 768px) {
  .hero-section {
    padding: 60px 0;
  }

  .hero-title {
    font-size: 40px;
  }

  .hero-description {
    font-size: 16px;
  }

  .image-box {
    width: 280px;
    height: 280px;
  }

  .section-title {
    font-size: 32px;
  }

  .cta-box {
    padding: 35px 25px;
  }

  .cta-box h2 {
    font-size: 28px;
  }
}
</style>
