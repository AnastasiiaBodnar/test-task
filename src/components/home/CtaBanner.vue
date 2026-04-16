<template>
    <section class="cta">
        <div class="cta__container"> 
            <div class="cta__banner">
                <h2 class="cta__title">Send your data</h2>
                <router-link to="/form" class="cta__btn">Go to form</router-link>
            </div>
        </div>
    </section>
</template>


<style scoped>
.cta {
    padding: 60px 0 140px 0;
}
 
.cta__container {
    max-width: 1200px;
    margin: 0 auto;
}
 
.cta__banner {
    background-image: url('@/assets/image/bagroundCta.png');
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    border-radius: 20px;
    padding: 60px 100px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}
 
.cta__title {
    font-size: 50px;
    font-weight: 700;
    color: var(--color-white);
    line-height: 100%;
}
 
.cta__btn {
    background-color: var(--color-primary);
    color: var(--color-white);
    text-decoration: none;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 100px;
    padding: 10px 24px;
    font-size: 18px;
    font-weight: 500;
    cursor: pointer;
    height: 58px;
    width: 392px;
}

@media (max-width: 1260px) {
  .cta__container {
    padding: 0 60px;
  }
  .cta__banner {
    padding: 40px 60px;
  }
}

@media (max-width: 768px) {
  .cta__banner {
    flex-direction: column;
    text-align: center;
    gap: 30px;
    padding: 40px 20px;
  }
  .cta__btn {
    width: 100%;
    max-width: 300px;
  }
}

@media (max-width: 320px) {

.cta__title { font-size: 36px; }
  
}
</style>