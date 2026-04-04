<script setup>
import { ref } from 'vue'

const isLangOpen = ref(false)
const isDownloadOpen = ref(false)

const toggleLang = () => {
  isLangOpen.value = !isLangOpen.value
}

const toggleDownload = () => {
  isDownloadOpen.value = !isDownloadOpen.value
}
</script>

<template>
  <header class="header">
    <div class="header__container">
        <div class="header__logo">LOGO</div>

        <nav class="header__nav">
            <a href="#">Home</a>
            <a href="#">About</a>
            <a href="#">Pricing</a>
            <a href="#">Facts</a>
            <a href="#">Blog</a>
            <a href="#">Support</a>
        </nav>

        <div class="header__actions">
            <div class="header__download" @click="toggleDownload">
              <button class="header__btn">Download</button>
              <div v-if="isDownloadOpen" class="header__dropdown">
                <div class="header__dropdown-item header__dropdown-item--download">App Store</div>
                <div class="header__dropdown-item header__dropdown-item--download">Google Play</div>
              </div>
        </div>

            <div class="header__lang" @click="toggleLang">
              Eng {{ isLangOpen ? '▴' : '▾' }}
              <div v-if="isLangOpen" class="header__dropdown">
                <div class="header__dropdown-item">
                  <img src="/src/assets/icons/sverige.png" alt="Sverige"> Sverige
                </div>
                <div class="header__dropdown-item">
                  <img src="/src/assets/icons/english.png" alt="English"> English
                </div>
              </div>
            </div>
        </div>
    </div>
  </header>
</template>

<style>
  .header__container{
    max-width: 1200px;
    margin: 0 auto;
    padding: 16px 24px;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .header__logo{
    font-weight: bold;
    color: var( --color-primary);
    font-size: 40px;
  }

  .header__nav{
    display: flex;
    gap: 24px;
  }

  .header__nav a {
    text-decoration: none;
    color: var(--color-dark-text);
    font-weight: 400;
    font-size: 18px;
    line-height: 28px;
    transition: color 0.2s ease;
  }

  .header__nav a:hover {
    color: var(--color-primary);
  }

  .header__actions {
    display: flex;
    align-items: center;
    gap: 16px;
  }

  .header__btn {
    background: var(--color-primary);
    color: var(--color-white);
    border: none;
    border-radius: 100px;
    padding: 10px 24px;
    width: 174px;
    height: 44px;
    gap: 10px;
    font-weight: 500;
    font-size: 18px;
    line-height: 20px;
    letter-spacing: 0.1px;
    cursor: pointer;
    transition: opacity 0.2s ease;
  }

  .header__btn:hover {
    opacity: 0.9;
  }

  .header__download {
  position: relative;
  }

  .header__lang {
    position: relative;
    cursor: pointer;
    font-weight: 400;
    font-size: 18px;
    transition: color 0.2s ease;
  }

  .header__lang:hover {
    color: var(--color-primary);
  }

  .header__dropdown {
    position: absolute;
    top: 140%;
    left: 0;
    background: var(--color-white);
    border-radius: 4px;
    min-width: 145px;
    box-shadow: 0 6px 10px rgb(0, 0, 0, 0.1);
    overflow: hidden;
  }

  .header__dropdown-item {
    display: flex;
    align-items: center;
    padding: 4px 6px;
    cursor: pointer;
    font-size: 14px;
    transition: background-color 0.2s ease;
  }

  .header__dropdown-item:hover {
    background-color: #f5f5f5;
  }

  .header__dropdown-item--download {
    padding: 8px 16px;
  }
  </style>