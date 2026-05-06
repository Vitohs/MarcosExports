<template>
  <div class="language-switcher">
    <button 
      @click="setLanguage('pt')"
      :class="['lang-btn', { active: locale === 'pt' }]"
    >
      PT
    </button>
    <span class="separator">|</span>
    <button 
      @click="setLanguage('en')"
      :class="['lang-btn', { active: locale === 'en' }]"
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
.language-switcher {
  display: flex;
  align-items: center;
  gap: 4px;
  white-space: nowrap;
}

.lang-btn {
  background: none;
  border: none;
  cursor: pointer;
  padding: 4px 8px;
  font-size: 0.9rem;
  font-weight: 600;
  color: inherit;
  transition: all 0.3s ease;
  border-bottom: 2px solid transparent;
  min-width: auto;
}

.lang-btn:hover {
  opacity: 0.8;
}

.lang-btn.active {
  border-bottom-color: currentColor;
  opacity: 1;
}

.separator {
  opacity: 0.5;
  font-size: 0.9rem;
}

@media (max-width: 768px) {
  .language-switcher {
    gap: 2px;
  }

  .lang-btn {
    padding: 3px 6px;
    font-size: 0.8rem;
  }

  .separator {
    font-size: 0.8rem;
  }
}
</style>
