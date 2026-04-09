<script setup>
const steps = [
    {
        title: 'Browse exercises',
        text: 'Browse over 100 exercises with a video or picture and a description.',
        icon: '/src/assets/icons/exercises.png',
        alt: 'exercises'
    },
    {
        title: 'Create timeline',
        text: 'Take pictures along the way during and after the pregnancy to see the transformation.',
        icon: '/src/assets/icons/timeline.png',
        alt: 'timeline'
    }
];
</script>

<template>
    <section class="how">
        <div class="how__container">
           <h2 class="how__title">How does it work?</h2> 
           <p class="how__subtitle">Easy, fun & essential training for moms</p>
           <div class="how__divider"></div>

           <div class="how__items">
            <div v-for="(step, index) in steps" :key="index" class="how__item">
                <img :src="step.icon" :alt="step.alt">
                <div class="how__item-content">
                    <div class="how__item-title">{{ step.title }}</div>
                    <div class="how__item-text">{{ step.text }}</div>
                </div>
            </div>
           </div>
        </div>
    </section>
</template>


<style scoped>

.how__container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 70px 0;
    text-align: center;
}

.how__title {
    font-size: 48px;
    font-weight: 700;
    line-height: 100%;
    color: var(--color-dark-text);
}

.how__subtitle {
    font-size: 30px;
    font-weight: 500;
    line-height: 100%;
    color: var(--color-light-text);
}

.how__divider {
    width: 45px;
    height: 3px;
    background-color: var(--color-divider);
    margin: 20px auto 55px auto;
}

.how__items {
    display: flex;
    align-items: center;
    justify-content: space-around;
}

.how__item {
    display: flex;
    align-items: flex-start;
    gap: 20px;
    text-align: left;
}

.how__item img {
    display: flex;
    line-height: 1
}

.how__item-title {
    font-size: 30px;
    font-weight: 500;
    color: #23153E;
    line-height: 1.8;
}

.how__item-text {
    font-size: 16px;
    font-weight: 400;
    line-height: 28px;
    color: #443A5A;
    max-width: 480px;
}
</style>