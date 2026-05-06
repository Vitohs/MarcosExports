<template>
  <div class="page-content">
    <section class="video-banner">
      <video
        src="../assets/presents.mp4"
        autoplay
        loop
        muted
        playsinline
        class="video-bg"
      ></video>
    </section>

    <section class="hero-section">
      <div class="container">
        <h1>{{ $t('page.title') }}</h1>
        <p class="hero-subtitle">{{ $t('page.subtitle') }}</p>
        <p class="hero-description">
          {{ $t('page.description') }}
        </p>
      </div>
    </section>

    <section class="services-section">
      <div class="container">
          <h2>{{ $t('services.title') }}</h2>
          <p class="services-description">
            {{ $t('services.description') }}
          </p>
          <div class="services-buttons">
            <a href="/produtos">
              <button class="cta-button">{{ $t('buttons.products') }}</button>
            </a>
          </div>
      </div>
    </section>

    <section class="market-section">
      <div class="container">
        <h2>{{ $t('market.title') }}</h2>
        <p>{{ $t('market.description') }}</p>
        <a href="sobre-nos">
          <button class="cta-button">{{ $t('market.button') }}</button>
        </a>
      </div>
    </section>

  </div>
</template>

<style scoped>
.page-content {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

.video-banner {
  width: 100%;
  height: 80vh;
  overflow: hidden;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
}

.video-bg {
  width: 100%;
  height: 100%;
  object-fit: cover;
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
  text-align: center;
}

.hero-section {
  padding: 80px 0;
  background-color: #f8f9fa;
  color: #333;
  min-height: 70vh;
  display: flex;
  align-items: center;
}

.hero-section h1 {
  font-size: 3rem;
  margin-bottom: 20px;
  color: #003566;
}

.hero-subtitle {
  font-size: 1.5rem;
  margin-bottom: 30px;
  color: #003566;
  font-weight: 600;
}

.hero-description {
  font-size: 1.1rem;
  line-height: 1.6;
  color: #666;
  max-width: 800px;
  margin: 0 auto;
}

.services-section {
  padding: 80px 0;
  background-color: #003566;
  color: white;
}

.services-section h2 {
  font-size: 2.5rem;
  margin-bottom: 50px;
  color: white;
}

.services-description {
  font-size: 1.2rem;
  color: #e0e0e0;
  margin-bottom: 40px;
  max-width: 700px;
  margin-left: auto;
  margin-right: auto;
}

.services-buttons {
  display: flex;
  justify-content: center;
  gap: 20px;
}

.market-section {
  padding: 80px 0;
  background-color: #f8f9fa;
  color: #333;
  text-align: center;
}

.market-section h2 {
  font-size: 2.5rem;
  margin-bottom: 30px;
  color: #003566;
}

.market-section p {
  font-size: 1.2rem;
  color: #666;
  margin-bottom: 40px;
  max-width: 600px;
  margin-left: auto;
  margin-right: auto;
}

.cta-button {
  background-color: #003566;
  color: white;
  padding: 15px 30px;
  border: 2px solid white;
  border-radius: 200px;
  font-size: 1.1rem;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.cta-button:hover {
  background-color: #002445;
}


@media (max-width: 768px) {
  .video-banner {
    height: 40vh;
  }

  .hero-section {
    padding: 50px 0;
    min-height: auto;
  }

  .hero-section h1 {
    font-size: 2.2rem;
  }

  .hero-subtitle {
    font-size: 1.2rem;
  }

  .hero-description {
    font-size: 1rem;
  }

  .services-section {
    padding: 50px 0;
  }

  .services-section h2 {
    font-size: 2rem;
  }

  .products-grid {
    grid-template-columns: 1fr;
    gap: 20px;
  }

  .product-card {
    padding: 25px;
  }

  .market-section {
    padding: 50px 0;
  }

  .market-section h2 {
    font-size: 2rem;
  }

  .market-section p {
    font-size: 1.1rem;
  }

  .container {
    padding: 0 15px;
  }
}
</style>
