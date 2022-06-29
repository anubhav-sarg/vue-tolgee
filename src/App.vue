<script lang="ts">
/* eslint-disable @typescript-eslint/no-var-requires */
import { defineComponent } from 'vue';
import { TolgeeProvider } from '@tolgee/vue';
import { useLanguage } from '@tolgee/vue';

import MainPage from './views/mainPage.vue';

export default defineComponent({
  name: 'App',
  components: { TolgeeProvider, MainPage },
  data() {
    return {
      config: {
        defaultLanguage: 'en',
        staticData: {
          en: () => import('./i18n/en.json'),
          es: () => import('./i18n/es-ES.json'),
          fr: () => import('./i18n/fr-FR.json'),
        },
        // remove this to enable language auto detection
        enableLanguageDetection: false,
        apiUrl: "https://app.tolgee.io",
        apiKey: "8374m29dp4b9eqh25pmeafvvgb",
      },
      setup() {
        const language = useLanguage();
        return { language };
      },
      currentRoute: window.location.pathname,
    };
  },
});
</script>


<template>
  <TolgeeProvider :config="config">
    <MainPage/>
    <template v-slot:fallback>
      <div>Loading...</div>
    </template>
  </TolgeeProvider>
</template>
