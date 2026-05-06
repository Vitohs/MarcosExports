<template>
  <footer class="footer">
    <div class="parte-superior">
      <img class="logo" src="../assets/mNegativa.svg"  />
    </div>
    <div class="parte-inferior">
        <div class="footer-columns">
          <ul>
            <li class="footer-title">{{ $t('footer.about') }}</li>
            <li><a href="/sobre-nos">{{ $t('footer.company') }}</a></li>
          </ul>
          <ul>
            <li class="footer-title">{{ $t('footer.work') }}</li>
            <li><a href="/produtos">{{ $t('footer.ourProducts') }}</a></li>
          </ul>
          <ul>
            <li class="footer-title">{{ $t('footer.contact') }}</li>
            <li>{{ $t('footer.whatsapp') }}<p>{{ $t('footer.phone') }}</p></li>
          </ul>
        </div>
        <p class="direitos">{{ $t('footer.rights') }}</p>
    </div>
  </footer>
</template>

<script setup>

</script>

<style scoped>
  .footer {
    display: flex;
    flex-direction: column;
    align-items: center;
    background: #f8f9fa;
    color: black;
    min-height: 35vh;
  }
  .parte-superior {
    width: 100%;
    background: #e9ecef;
  }
  .parte-inferior{
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 100%;
    padding: 32px 0 16px 0;
  }
  .logo {
    height: 80px;
    width: auto;
    display: block;
    object-fit: contain;
  }
  .footer-columns {
    display: flex;
    justify-content: center;
    gap: 60px;
    padding: 40px 0;
  }
  @media (max-width: 768px) {
    .parte-superior {
      display: flex;
      justify-content: center;
      align-items: center;
      width: 100%;
      background: #e9ecef;
    }
    .logo {
      height: 50px;
      width: auto;
      display: block;
      object-fit: contain;
    }
    .footer-columns {
      flex-direction: column;
      align-items: center;
      gap: 24px;
      padding: 24px 0;
    }
    .footer ul {
      align-items: center;
      text-align: center;
      margin-bottom: 0;
    }
    .footer-title {
      font-size: 1.1em;
    }
    .parte-inferior {
      padding: 16px 0 8px 0;
    }
  }
  .footer-title {
    font-weight: bold;
    color: #444;
    margin-bottom: 10px;
    text-transform: uppercase;
  }
  .footer ul {
    list-style: none;
    padding: 0;
  }
  .footer li {
    margin-bottom: 8px;
    color: #888;
  }
  .footer a {
    color: #888;
    text-decoration: none;
  }
  .footer a:hover {
    text-decoration: underline;
  }
</style>
