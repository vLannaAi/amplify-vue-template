<script setup lang="ts">
import { ref, watch, onMounted } from 'vue';
import { Authenticator } from "@aws-amplify/ui-vue";
import Todos from "./components/Todos.vue";
import { I18n } from "aws-amplify/utils";
import { translations } from '@aws-amplify/ui-vue';
import "@aws-amplify/ui-vue/styles.css";

const selectedLanguage = ref('th');

I18n.setLanguage(selectedLanguage.value);
I18n.putVocabularies(translations);


const changeLanguage = () => {
  // Save the selected language in localStorage
  localStorage.setItem('language', selectedLanguage.value);

  // Refresh the page
  window.location.reload();
};

// Retrieve the saved language on page load
onMounted(() => {
  const savedLanguage = localStorage.getItem('language');
  if (savedLanguage) {
    selectedLanguage.value = savedLanguage;
    I18n.setLanguage(selectedLanguage.value);
    I18n.putVocabularies(translations);

  }
});


</script>

<template>
  <main>
    <Authenticator>
      <!-- customize with your logo -->
      <template v-slot:header>
        <div style="padding: var(--amplify-space-large); text-align: center">
          <img
            class="amplify-image"
            alt="Amplify logo"
            src="https://docs.amplify.aws/assets/logo-dark.svg"
          />
        </div>
      </template>

      <template v-slot:footer>
        <div style="padding: var(--amplify-space-large); text-align: center">
          <p
            class="amplify-text"
            style="color: var(--amplify-colors-neutral-80)"
          >
            <select v-model="selectedLanguage" @change="changeLanguage"  style="padding:4px;">
              <option value="th">🇹🇭 ไทย ⭐️</option>
              <option value="en">🇬🇧 English</option>
              <option value="it">🇮🇹 Italiano</option>
              <option value="zh">🇨🇳 中文 </option>
              <option value="ja">🇯🇵 日本語</option>
              <option value="ko">🇰🇷 한국어</option>

            </select>
          </p>
        </div>
      </template>

      <template v-slot="{ user, signOut }">
        <h1>Hello {{ user?.signInDetails?.loginId }}'s todos</h1>
        <Todos />
        <button @click="signOut">Sign Out</button>
      </template>
    </Authenticator>
  </main>
</template>
