<template>
  <div class="language-switcher-fixed">
    <button 
      @click="setLanguage('pt')"
      :class="['lang-btn', { active: locale === 'pt' }]"
      title="Português"
    >
      PT
    </button>
    <span class="separator">|</span>
    <button 
      @click="setLanguage('en')"
      :class="['lang-btn', { active: locale === 'en' }]"
      title="English"
    >
      EN
    </button>
  </div>
</template>

<script setup>
import { useI18n } from 'vue-i18n'
import { ref, watch } from 'vue'

const i18n = useI18n()
const locale = ref(i18n.locale)

const setLanguage = (newLocale) => {
  locale.value = newLocale
  i18n.locale = newLocale
  localStorage.setItem('locale', newLocale)
}

watch(() => i18n.locale, (newLocale) => {
  locale.value = newLocale
})
</script>

<style scoped>
.language-switcher-fixed {
  position: fixed;
  bottom: 20px;
  right: 20px;
  display: flex;
  align-items: center;
  gap: 6px;
  background: #003566;
  padding: 8px 12px;
  border-radius: 50px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
  z-index: 999;
}

.lang-btn {
  background: none;
  border: none;
  cursor: pointer;
  padding: 4px 10px;
  font-size: 0.9rem;
  font-weight: 600;
  color: white;
  transition: all 0.3s ease;
  border-radius: 4px;
}

.lang-btn:hover {
  background: rgba(255, 255, 255, 0.1);
}

.lang-btn.active {
  background: rgba(255, 255, 255, 0.2);
}

.separator {
  opacity: 0.5;
  color: white;
}

@media (min-width: 769px) {
  .language-switcher-fixed {
    display: none;
  }
}
</style>
