<template>
    <section class="hero">
        <div class="hero__container">
            <div class="hero__content">
                <h1 class="hero__title">Strong for life with us</h1>
                <div class="hero__divider"></div>
                <p class="hero__text">
                    The best Pre/postnatal fitness app! 100 exercises divided in before, during and after pregnancy. 
                    Stay strong and healthy through all stages of pregnancy.
                </p>
                <div class="hero__buttons">
                    <a href="#" class="hero__store-btn">
                        <img src="/src/assets/icons/Apple.png" alt="App Store">
                        <div class="hero__store-text">
                            <span class="hero__store-label">Download on the</span>
                            <span class="hero__store-name">App Store</span>
                        </div>
                    </a>

                    <a href="#" class="hero__store-btn">
                        <img src="/src/assets/icons/GooglePlay.png" alt="Google Play">
                        <div class="hero__store-text">
                            <span class="hero__store-label">GET IT ON</span>
                            <span class="hero__store-name">Google Play</span>
                        </div>
                    </a>
                </div>
            </div>

            <div class="hero__image">
                <img src="/src/assets/image/PhoneHero.png" alt="App screenshot">
            </div>
        </div>
    </section>
</template>

<style scoped>
.hero {
    padding: 40px 20px;
}

.hero__container {
    max-width: 950px;
    margin: 0 auto;
    padding: 16px 28px 56px 100px;
    background-image: url(/src/assets/image/bg.png);
    background-size: cover;
    background-position: center;
    border-radius: 30px;
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    gap: 32px;
}

.hero__content {
    flex: 1;
    max-width: 380px;
    margin-top: 36px;
}

.hero__title {
    font-size: 40px;
    font-weight: 700;
    color: var(--color-dark-text);
    margin-bottom: 24px;
    line-height: 1.1;
}

.hero__divider {
    width: 40px;
    height: 3px;
    background-color: var(--color-divider);
    margin-bottom: 24px;
    border-radius: 2px;
}

.hero__text {
    font-size: 18px;
    color: var(--color-light-text);
    line-height: 1.55;
    margin-bottom: 30px;
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
    justify-content: flex-end;
}

.hero__image img {
    max-width: 100%;
    max-height: 480px;
    object-fit: contain;
    transform: scale(1.2);
    transform-origin: top right;
}

</style>