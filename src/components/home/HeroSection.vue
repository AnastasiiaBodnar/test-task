<template>
  <section class="hero">

    <img src="@/assets/image/bg.png" alt="Background" class="hero-bg-img" />

    <div class="hero__container"> 
    
      <div class="hero__content">
        <h1 class="hero__title">
          Strong for life <br> 
          with us
        </h1>
        
        <div class="hero__divider"></div>
        
        <p class="hero__subtitle">
          The best Pre/postnatal fitness app! 100 <br>
          exercises divided in before, during and <br>
          after pregnancy. Stay strong and healthy <br>
          through all stages of pregnancy.
        </p>

        <div class="hero__buttons">

          <button class="hero__store-btn">
            <img src="@/assets/icons/Apple.png" alt="Apple" />
            <div class="hero__store-text">
              <span class="hero__store-label">Download on the</span>
              <span class="hero__store-name">App Store</span>
            </div>
          </button>
          
          <button class="hero__store-btn">
            <img src="@/assets/icons/GooglePlay.png" alt="Google Play" />
            <div class="hero__store-text">
              <span class="hero__store-label">GET IT ON</span>
              <span class="hero__store-name">Google Play</span>
            </div>
          </button>
        </div>
      </div>

      <div class="hero__image">
        <img src="@/assets/image/PhoneHero.png" alt="App Interface" class="phone-image" />
      </div>

    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
.hero {
  position: relative;
  max-width: 1200px;
  margin: 60px auto;
  height: 620px;
  overflow: visible;
}

.hero-bg-img {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: fill; 
  z-index: -1;
}

.hero__container {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  padding: 60px 60px 0 60px; 
}

.hero__content {
  flex: 1;
  margin-top: 0;
}

.hero__title {
  color: var(--color-dark-text, #23153E);
  font-size: 52px;
  font-weight: 800;
  line-height: 1.2;
  margin: 0;
}

.hero__divider {
  width: 45px;
  height: 3px;
  background-color: var(--color-divider, #FF2D55);
  margin: 20px 0 30px 0;
}

.hero__subtitle {
  color: var(--color-light-text, #443A5A);
  font-size: 18px;
  line-height: 1.5;
  margin-bottom: 35px;
  max-width: 420px;
}

.hero__buttons {
    display: flex;
    gap: 16px;
}

.hero__store-btn {
    display: flex;
    align-items: center;
    width: 170px;
    height: 40px;
    gap: 8px;
    background-color: var(--color-white);
    padding: 8px 14px;
    border-radius: 5px;
    text-decoration: none;
    color: var(--color-black);
    border: 1px solid #A6A6A6;
}

.hero__store-btn img {
    height: 30px;
    width: 25px;
}

.hero__store-text {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
}

.hero__store-label {
    font-size: 10px;
    line-height: 1;
    margin-bottom: 4px;
    color: var(--color-black);
}

.hero__store-name {
    font-size: 16px;
    font-weight: 600;
    line-height: 1;
}

.hero__image {
  flex: 1;
  display: flex;
  justify-content: center;
  margin-top: -80px;
}

.phone-image {
  max-width: 100%; 
  width: 540px;
  height: 700px;
}

</style>