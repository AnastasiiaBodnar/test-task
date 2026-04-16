<script setup>
import { ref } from 'vue'

const isLangOpen = ref(false)
const isDownloadOpen = ref(false)
const isMobileMenuOpen = ref(false)

const toggleLang = () => {
  isLangOpen.value = !isLangOpen.value
  isDownloadOpen.value = false
}

const toggleDownload = () => {
  isDownloadOpen.value = !isDownloadOpen.value
  isLangOpen.value = false
}

const toggleMobileMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value
}
</script>

<template>
  <header class="header">
    <div class="header__container">

      <div class="header__logo">LOGO</div>

      <button class="header__burger" @click="toggleMobileMenu">
        <span></span>
        <span></span>
        <span></span>
      </button>

      <div v-if="isMobileMenuOpen" class="header__mobile-menu">
        <a href="#">Home</a>
        <a href="#">About</a>
        <a href="#">Pricing</a>
        <a href="#">Facts</a>
        <a href="#">Blog</a>
        <a href="#">Support</a>

        <div class="header__download" @click="toggleDownload">
          <button class="header__btn">Download</button>
          <div v-if="isDownloadOpen" class="header__dropdown">
            <div class="header__dropdown-item">App Store</div>
            <div class="header__dropdown-item">Google Play</div>
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
          <div v-if="isLangOpen" class="header__dropdown header__dropdown--right">
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
.header__container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px 0;
  display: flex;
  align-items: center;
  justify-content: space-between;
  position: relative;
}

.header__logo {
  font-weight: bold;
  color: var(--color-primary);
  font-size: 40px;
}

.header__nav {
  display: flex;
  gap: 24px;
  margin-left: auto;
  margin-right: 40px;
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
  font-weight: 500;
  font-size: 18px;
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
  top: 120%;
  left: 0;
  background: var(--color-white);
  border-radius: 4px;
  min-width: 145px;
  box-shadow: 0 6px 10px rgba(0, 0, 0, 0.1);
  overflow: hidden;
  z-index: 101;
}

.header__dropdown--right {
  left: auto;
  right: 0;
}

.header__dropdown-item {
  display: flex;
  align-items: center;
  padding: 8px 16px;
  cursor: pointer;
  font-size: 14px;
  transition: background-color 0.2s ease;
}

.header__dropdown-item:hover {
  background-color: #f5f5f5;
}

.header__burger {
  display: none;
  flex-direction: column;
  justify-content: space-between;
  width: 30px;
  height: 20px;
  background: transparent;
  border: none;
  cursor: pointer;
  padding: 0;
  z-index: 100;
}

.header__burger span {
  display: block;
  width: 100%;
  height: 3px;
  background-color: var(--color-dark-text);
  border-radius: 2px;
}

.header__mobile-menu {
  display: none;
}


@media (max-width: 1024px) {
  .header__container {
    padding: 20px 60px;
  }
  .header__logo {
    font-size: 32px;
  }
  .header__nav {
    gap: 16px;
    margin-right: 20px;
  }
  .header__nav a {
    font-size: 16px;
  }
  .header__btn {
    width: auto;
    padding: 10px 16px;
    font-size: 16px;
  }
}

@media (max-width: 768px) {

  .header__nav,
  .header__actions {
    display: none;
  }

  .header__burger {
    display: flex;
  }


  .header__mobile-menu {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 20px;
    position: absolute;
    top: 80px;
    left: 0;
    width: 100%;
    background: var(--color-white);
    padding: 30px 0 40px 0;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    z-index: 99;
  }

  .header__mobile-menu a {
    text-decoration: none;
    color: var(--color-dark-text);
    font-size: 18px;
    font-weight: 400;
    transition: color 0.2s ease;
  }

  .header__mobile-menu a:hover {
    color: var(--color-primary);
  }

  .header__mobile-menu .header__download,
  .header__mobile-menu .header__lang {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .header__mobile-menu .header__dropdown {
    position: relative;
    top: 10px;
    left: auto;
    right: auto;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    min-width: 180px;
    text-align: center;
  }
}

@media (max-width: 480px) {
  .header__container {
    padding: 20px 16px;
  }
  .header__logo {
    font-size: 28px;
  }
  .header__mobile-menu {
    top: 75px;
  }
}
</style>