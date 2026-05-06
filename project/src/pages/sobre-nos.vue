<template>
    <div class="page-wrapper">
        <div class="banner">
            <img class="image" src="../assets/fundo.svg">
            <h1 class="banner-title">{{ $t('aboutus.banner.title') }}</h1>
            <p class="banner-subtitle">{{ $t('aboutus.banner.subtitle') }}</p>
        </div>

        <section class="about-section">
            <div class="container">
                <div class="company-intro">
                    <h2 class="section-title">{{ $t('aboutus.whoWe.title') }}</h2>
                    <p class="intro-text">
                        {{ $t('aboutus.whoWe.description') }}
                    </p>
                </div>

                <div class="services-grid">
                    <div class="service-card">
                        <h3>{{ $t('aboutus.services.eucalipto.title') }}</h3>
                        <p>{{ $t('aboutus.services.eucalipto.description') }}</p>
                    </div>

                    <div class="service-card">
                        <h3>{{ $t('aboutus.services.pinus.title') }}</h3>
                        <p>{{ $t('aboutus.services.pinus.description') }}</p>
                    </div>

                    <div class="service-card">
                        <h3>{{ $t('aboutus.services.cavaco.title') }}</h3>
                        <p>{{ $t('aboutus.services.cavaco.description') }}</p>
                    </div>

                    <div class="service-card">
                        <h3>{{ $t('aboutus.services.acucar.title') }}</h3>
                        <p>{{ $t('aboutus.services.acucar.description') }}</p>
                    </div>
                </div>

                <div class="market-reach">
                    <h2 class="section-title">{{ $t('aboutus.market.title') }}</h2>
                    <div class="market-grid">
                        <div class="market-card">
                            <h4>{{ $t('aboutus.market.national.title') }}</h4>
                            <p>{{ $t('aboutus.market.national.description') }}</p>
                        </div>
                        <div class="market-card">
                            <h4>{{ $t('aboutus.market.export.title') }}</h4>
                            <p>{{ $t('aboutus.market.export.description') }}</p>
                        </div>
                    </div>
                </div>

                <div class="values-section">
                    <h2 class="section-title">{{ $t('aboutus.values.title') }}</h2>
                    <div class="values-grid">
                        <div class="value-item">
                            <h4>{{ $t('aboutus.values.quality.title') }}</h4>
                            <p>{{ $t('aboutus.values.quality.description') }}</p>
                        </div>
                        <div class="value-item">
                            <h4>{{ $t('aboutus.values.sustainability.title') }}</h4>
                            <p>{{ $t('aboutus.values.sustainability.description') }}</p>
                        </div>
                        <div class="value-item">
                            <h4>{{ $t('aboutus.values.reliability.title') }}</h4>
                            <p>{{ $t('aboutus.values.reliability.description') }}</p>
                        </div>
                        <div class="value-item">
                            <h4>{{ $t('aboutus.values.innovation.title') }}</h4>
                            <p>{{ $t('aboutus.values.innovation.description') }}</p>
                        </div>
                    </div>
                </div>

                <div class="commitment-section">
                    <h2 class="section-title">{{ $t('aboutus.commitment.title') }}</h2>
                    <div class="commitment-content">
                        <p>
                            {{ $t('aboutus.commitment.text1') }}
                        </p>
                        <p>
                            {{ $t('aboutus.commitment.text2') }}
                        </p>
                    </div>
                </div>
            </div>
        </section>
    </div>
</template>

<script setup>

</script>

<style scoped>
    .page-wrapper {
        width: 100%;
    }
    .container {
        max-width: 1200px;
        margin: 0 auto;
        padding: 40px 20px;
        text-align: center;
    }
    .banner {
        width: 100vw;
        height: 90vh;
        position: relative;
        background-color: black;
        display: flex;
        align-items: center;
        justify-content: center;
        overflow: hidden;
    }
    .image {
        object-fit: cover;
        width: 100%;
        height: 100%;
        filter: brightness(0.6);
    }
    .banner-title {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        color: #fff;
        font-size: 3rem;
        font-weight: bold;
        text-align: center;
        width: 90%;
        pointer-events: none;
        text-shadow: 0 4px 16px rgba(0,0,0,0.8);
        line-height: 1.2;
    }
    .banner-subtitle {
        position: absolute;
        top: 62%;
        left: 50%;
        transform: translate(-50%, -50%);
        color: #fff;
        font-size: 1.5rem;
        text-shadow: 0 2px 8px rgba(0,0,0,0.7);
        margin: 0;
        z-index: 2;
        text-align: center;
        width: 90%;
        pointer-events: none;
        line-height: 1.4;
    }
    .about-section {
        background-color: #f8f9fa;
        padding: 80px 0;
    }
    .section-title {
        font-size: 2.8rem;
        color: #2c3e50;
        margin-bottom: 40px;
        font-weight: 700;
        text-align: center;
    }
    .company-intro {
        margin-bottom: 80px;
    }

    .intro-text {
        font-size: 1.3rem;
        color: #5a6c7d;
        line-height: 1.8;
        max-width: 800px;
        margin: 0 auto;
        text-align: center;
    }
    .services-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
        gap: 40px;
        margin-bottom: 80px;
    }
    .service-card {
        background: linear-gradient(135deg, #1a472a 0%, #2d5016 100%);
        padding: 40px 30px;
        border-radius: 16px;
        box-shadow: 0 8px 32px rgba(26, 71, 42, 0.3);
        transition: transform 0.3s ease, box-shadow 0.3s ease;
    }

    .service-card:hover {
        transform: translateY(-8px);
        box-shadow: 0 16px 48px rgba(26, 71, 42, 0.4);
    }
    .icon {
        font-size: 3rem;
        margin-bottom: 20px;
    }
    .service-card h3 {
        font-size: 1.8rem;
        color: #ffffff;
        margin-bottom: 15px;
        font-weight: 600;
    }
    .service-card p {
        color: rgba(255, 255, 255, 0.9);
        line-height: 1.6;
        font-size: 1.1rem;
    }
    .market-reach {
        margin-bottom: 80px;
    }
    .market-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 30px;
        margin-top: 40px;
    }
    .market-card {
        background: #003566;
        color: white;
        padding: 30px;
        border-radius: 12px;
        box-shadow: 0 8px 24px rgba(0,0,0,0.15);
    }
    .market-card h4 {
        font-size: 1.5rem;
        margin-bottom: 15px;
        font-weight: 600;
    }
    .market-card p {
        line-height: 1.6;
        opacity: 0.95;
    }
    .values-section {
        margin-bottom: 80px;
    }
    .values-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 30px;
        margin-top: 40px;
    }
    .value-item {
        background: white;
        padding: 30px 25px;
        border-radius: 12px;
        box-shadow: 0 4px 20px rgba(45, 80, 22, 0.12);
        transition: all 0.3s ease;
    }
    .value-item:hover {
        transform: translateY(-4px);
        background: #e8f5e9;
        box-shadow: 0 8px 28px rgba(45, 80, 22, 0.2);
    }
    .value-icon {
        font-size: 2.5rem;
        margin-bottom: 15px;
    }
    .value-item h4 {
        font-size: 1.4rem;
        color: #2c3e50;
        margin-bottom: 10px;
        font-weight: 600;
    }
    .value-item p {
        color: #5a6c7d;
        line-height: 1.5;
        font-size: 0.95rem;
    }
    .commitment-section {
        background: linear-gradient(135deg, #ffffff 0%, #e8f5e9 50%, #f0f7f4 100%);
        padding: 60px 40px;
        border-radius: 16px;
        box-shadow: 0 8px 32px rgba(26, 71, 42, 0.15);
        border: none;
        position: relative;
        overflow: hidden;
    }
    .commitment-section::before {
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        height: 4px;
    }
    .commitment-content p {
        font-size: 1.2rem;
        color: #5a6c7d;
        line-height: 1.8;
        margin-bottom: 25px;
        text-align: left;
        max-width: 900px;
        margin-left: auto;
        margin-right: auto;
    }
    .commitment-content p:last-child {
        margin-bottom: 0;
    }
    @media (max-width: 1024px) {
        .banner-title {
            font-size: 2.5rem;
        }
        .banner-subtitle {
            font-size: 1.3rem;
        }
        .section-title {
            font-size: 2.4rem;
        }
        .services-grid {
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }
    }
    @media (max-width: 768px) {
        .banner {
            height: 70vh;
        }
        .banner-title {
            font-size: 2rem;
            width: 95%;
            padding: 0 10px;
        }
        .banner-subtitle {
            font-size: 1.1rem;
            width: 95%;
            padding: 0 10px;
            top: 65%;
        }
        .about-section {
            padding: 60px 0;
        }
        .container {
            padding: 30px 15px;
        }
        .section-title {
            font-size: 2rem;
            margin-bottom: 30px;
        }
        .intro-text {
            font-size: 1.1rem;
        }
        .services-grid {
            grid-template-columns: 1fr;
            gap: 25px;
            margin-bottom: 60px;
        }
        .service-card {
            padding: 30px 25px;
        }
        .market-grid, .values-grid {
            grid-template-columns: 1fr;
            gap: 20px;
        }
        .commitment-section {
            padding: 40px 25px;
        }
        .commitment-content p {
            font-size: 1.1rem;
            text-align: center;
        }
    }
    @media (max-width: 480px) {
        .banner {
            height: 60vh;
        }
        .banner-title {
            font-size: 1.6rem;
        }
        .banner-subtitle {
            font-size: 0.95rem;
        }
        .about-section {
            padding: 40px 0;
        }
        .container {
            padding: 20px 10px;
        }
        .section-title {
            font-size: 1.7rem;
        }
        .intro-text {
            font-size: 1rem;
        }
        .service-card {
            padding: 25px 20px;
        }
        .service-card h3 {
            font-size: 1.5rem;
        }
        .commitment-section {
            padding: 30px 20px;
        }
        .market-card, .value-item {
            padding: 25px 20px;
        }
    }
</style>
