<template>
    <div class="page-wrapper">
        <div class="banner">
            <img class="image" src="../assets/eucalipto.svg">
            <h1 class="banner-title">QUALIDADE EM PRIMEIRO LUGAR</h1>
            <p class="banner-subtitle">Qualidade e sustentabilidade em cada produto. Conheça nossa linha completa!</p>
        </div>

        <section class="services-section">
            <div class="container">
              <div class="cavaco">
                    <h2 class="cavaco-title">Produção de Cavaco Premium</h2>
                    <p class="cavaco-subtitle">
                        Cavacos de eucalipto de alta qualidade para geração de energia e biomassa. Produto versátil com granulometria controlada, ideal para fornos industriais, caldeiras e produção de energia térmica sustentável.
                    </p>
                    <img class="imgCavaco" src="../assets/cavaco.svg">
                </div>
            </div>
             <div class="container">
              <div class="cavaco-celulose">
                    <h2 class="cavaco-celulose-title">Produção de Cavaco Premium para celulose</h2>
                    <p class="cavaco-celulose-subtitle">
                        Cavacos de eucalipto com especificações técnicas rigorosas para a indústria de celulose e papel. Granulometria uniforme (15-30mm), baixo teor de casca, umidade controlada e ausência de impurezas, atendendo aos mais altos padrões de qualidade do setor.
                    </p>
                    <img class="imgCavaco" src="../assets/cavaco-celulose.webp">
                </div>
            </div>
            <div class="container">
                <div class="toras">
                 <h2 class="toras-title">Comércio de toras de Eucalipto</h2>
                 <p class="toras-subtitle">
                    Toras de eucalipto selecionadas com diâmetros variados e certificação de origem. Produto versátil para construção civil, móveis, energia renovável e indústria madeireira em geral.
                 </p>
                <img class="imgToras" src="../assets/toras.svg">
              </div>
            </div>
            <div class="container">
                <div class="pinus">
                 <h2 class="pinus-title">Comércio de toras de Pinus</h2>
                 <p class="pinus-subtitle">
                    Toras de pinus de reflorestamento com crescimento controlado e manejo sustentável. Excelente para estruturas, laminação, compensados e projetos que exigem madeira de fibra longa.
                 </p>
                <img class="imgPinus" src="../assets/pinus.svg">
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
    .cavaco, .cavaco-celulose, .toras, .pinus {
        background: white;
        border-radius: 16px;
        padding: 40px;
        margin-bottom: 40px;
        box-shadow: 0 8px 32px rgba(0,0,0,0.1);
        transition: all 0.3s ease;
        position: relative;
        overflow: hidden;
    }
    
    .cavaco {
        border: 3px solid rgba(249, 115, 22, 0.3);
    }
    
    .cavaco-celulose {
        border: 3px solid rgba(20, 184, 166, 0.3);
    }
    
    .toras {
        border: 3px solid rgba(22, 163, 74, 0.3);
    }
    
    .pinus {
        border: 3px solid rgba(146, 64, 14, 0.3);
    }
    
    .cavaco:hover {
        transform: translateY(-8px);
        box-shadow: 0 16px 48px rgba(249, 115, 22, 0.2);
        border-left-color: rgba(249, 115, 22, 0.8);
    }
    
    .cavaco-celulose:hover {
        transform: translateY(-8px);
        box-shadow: 0 16px 48px rgba(20, 184, 166, 0.2);
        border-left-color: rgba(20, 184, 166, 0.8);
    }
    
    .toras:hover {
        transform: translateY(-8px);
        box-shadow: 0 16px 48px rgba(22, 163, 74, 0.2);
        border-left-color: rgba(22, 163, 74, 0.8);
    }
    
    .pinus:hover {
        transform: translateY(-8px);
        box-shadow: 0 16px 48px rgba(146, 64, 14, 0.2);
        border-left-color: rgba(146, 64, 14, 0.8);
    }
    .cavaco-title, .cavaco-celulose-title, .toras-title, .pinus-title {
        font-size: 2.5rem;
        margin-bottom: 20px;
        color: #003566;
        font-weight: 700;
        line-height: 1.2;
    }
    .cavaco-subtitle, .cavaco-celulose-subtitle, .toras-subtitle, .pinus-subtitle {
        font-size: 1.2rem;
        color: #5a6c7d;
        margin-bottom: 30px;
        line-height: 1.6;
        max-width: 600px;
        margin-left: auto;
        margin-right: auto;
    }
    .imgCavaco, .imgToras, .imgPinus {
        max-width: 600px;
        height: auto;
        margin-top: 20px;
        border-radius: 12px;
        transition: transform 0.3s ease;
    }
    .imgCavaco:hover, .imgToras:hover, .imgPinus:hover {
        transform: scale(1.05);
    }
    @media (max-width: 1024px) {
        .banner-title {
            font-size: 2.5rem;
        }

        .banner-subtitle {
            font-size: 1.3rem;
        }

        .cavaco-title, .cavaco-celulose-title, .toras-title, .pinus-title {
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
        .cavaco, .cavaco-celulose, .toras, .pinus {
            padding: 30px 20px;
            margin-bottom: 30px;
            border-radius: 12px;
        }
        .cavaco-title, .cavaco-celulose-title, .toras-title, .pinus-title {
            font-size: 1.8rem;
            margin-bottom: 15px;
        }
        .cavaco-subtitle, .cavaco-celulose-subtitle, .toras-subtitle, .pinus-subtitle {
            font-size: 1rem;
            margin-bottom: 20px;
            line-height: 1.5;
        }
        .imgCavaco, .imgToras, .imgPinus {
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

        .cavaco, .cavaco-celulose, .toras, .pinus {
            padding: 25px 15px;
        }

        .cavaco-title, .cavaco-celulose-title, .toras-title, .pinus-title {
            font-size: 1.5rem;
        }

        .cavaco-subtitle, .cavaco-celulose-subtitle, .toras-subtitle, .pinus-subtitle {
            font-size: 0.9rem;
        }

        .imgCavaco, .imgToras, .imgPinus {
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