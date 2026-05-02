<template>
    <div class="page-wrapper">
        <div class="banner">
            <img class="image" src="../assets/eucalipto.svg">
            <h1 class="banner-title">QUALIDADE EM PRIMEIRO LUGAR</h1>
            <p class="banner-subtitle">Qualidade e sustentabilidade em cada produto. Conheça nossa linha completa!</p>
        </div>

        <section class="services-section">
            <div class="container">
              <div class="product-card card-orange">
                    <h2 class="product-title">Produção de Cavaco Premium</h2>
                    <p class="product-subtitle">
                        Cavacos de eucalipto de alta qualidade para geração de energia e biomassa. Produto versátil com granulometria controlada, ideal para fornos industriais, caldeiras e produção de energia térmica sustentável.
                    </p>
                    <img class="product-image" src="../assets/cavaco.svg">
                </div>
            </div>
             <div class="container">
              <div class="product-card card-teal">
                    <h2 class="product-title">Produção de Cavaco Premium para celulose</h2>
                    <p class="product-subtitle">
                        Cavacos de eucalipto com especificações técnicas rigorosas para a indústria de celulose e papel. Granulometria uniforme (15-30mm), baixo teor de casca, umidade controlada e ausência de impurezas, atendendo aos mais altos padrões de qualidade do setor.
                    </p>
                    <img class="product-image" src="../assets/cavaco-celulose.webp">
                </div>
            </div>
            <div class="container">
                <div class="product-card card-green">
                 <h2 class="product-title">Comércio de toras de Eucalipto</h2>
                 <p class="product-subtitle">
                    Toras de eucalipto selecionadas com diâmetros variados e certificação de origem. Produto versátil para construção civil, móveis, energia renovável e indústria madeireira em geral.
                 </p>
                <img class="product-image" src="../assets/toras.svg">
              </div>
            </div>
            <div class="container">
                <div class="product-card card-brown">
                 <h2 class="product-title">Comércio de toras de Pinus</h2>
                 <p class="product-subtitle">
                    Toras de pinus de reflorestamento com crescimento controlado e manejo sustentável. Excelente para estruturas, laminação, compensados e projetos que exigem madeira de fibra longa.
                 </p>
                <img class="product-image" src="../assets/pinus.svg">
              </div>
            </div>
            <div class="container">
                <div class="product-card card-gray">
                 <h2 class="product-title">Exportação de Açúcar</h2>
                 <p class="product-subtitle">
                    Fornecimento de açúcar de alta pureza voltado para o mercado internacional; Garantimos processos rigorosos de controle de qualidade, armazenamento seguro e logística eficiente, atendendo às exigências globais da indústria com máxima excelência.
                 </p>
                <img class="product-image" src="../assets/acucar.svg">
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
    .services-section {
        background-color: #f8f9fa;
        padding: 80px 0;
        min-height: auto;
    }

    .product-card {
        background: white;
        border-radius: 16px;
        padding: 40px;
        margin-bottom: 40px;
        box-shadow: 0 8px 32px rgba(0,0,0,0.1);
        transition: all 0.3s ease;
        position: relative;
        overflow: hidden;
        border: 3px solid transparent;
    }
    .product-card:hover {
        transform: translateY(-8px);
    }
    
    .card-orange { border-color: rgba(249, 115, 22, 0.3); }
    .card-orange:hover {
        border-left-color: rgba(249, 115, 22, 0.8);
    }
    
    .card-teal { border-color: rgba(20, 184, 166, 0.3); }
    .card-teal:hover {
        border-left-color: rgba(20, 184, 166, 0.8);
    }
    
    .card-green { border-color: rgba(22, 163, 74, 0.3); }
    .card-green:hover {
        border-left-color: rgba(22, 163, 74, 0.8);
    }
    
    .card-brown { border-color: rgba(146, 64, 14, 0.3); }
    .card-brown:hover {
        border-left-color: rgba(146, 64, 14, 0.8);
    }

    .card-gray { border-color: rgba(100, 116, 139, 0.3); }
    .card-gray:hover {
        border-left-color: rgba(100, 116, 139, 0.8);
    }

    .product-title {
        font-size: 2.5rem;
        margin-bottom: 20px;
        color: #003566;
        font-weight: 700;
        line-height: 1.2;
    }
    .product-subtitle {
        font-size: 1.2rem;
        color: #5a6c7d;
        margin-bottom: 30px;
        line-height: 1.6;
        max-width: 600px;
        margin-left: auto;
        margin-right: auto;
    }
    .product-image {
        max-width: 600px;
        width: 100%;
        height: auto;
        margin-top: 20px;
        border-radius: 12px;
        transition: transform 0.3s ease;
    }
    .product-image:hover {
        transform: scale(1.05);
    }

    @media (max-width: 1024px) {
        .banner-title {
            font-size: 2.5rem;
        }

        .banner-subtitle {
            font-size: 1.3rem;
        }

        .product-title {
            font-size: 2.2rem;
        }

        .container {
            padding: 30px 15px;
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
        .services-section {
            padding: 60px 0;
        }
        .container {
            padding: 20px 10px;
        }
        .product-card {
            padding: 30px 20px;
            margin-bottom: 30px;
            border-radius: 12px;
        }
        .product-title {
            font-size: 1.8rem;
            margin-bottom: 15px;
        }
        .product-subtitle {
            font-size: 1rem;
            margin-bottom: 20px;
            line-height: 1.5;
        }
        .product-image {
            max-width: 350px;
            margin-top: 15px;
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

        .product-card {
            padding: 25px 15px;
        }

        .product-title {
            font-size: 1.5rem;
        }

        .product-subtitle {
            font-size: 0.9rem;
        }

        .product-image {
            max-width: 200px;
        }

        .container {
            padding: 15px 8px;
        }

        .services-section {
            padding: 40px 0;
        }
    }
</style>