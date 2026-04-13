<template>
  <section class="stages">
    <div class="stages__container">

      <div class="stages__header">
        <h2 class="stages__title">Before, during and after pregnancy</h2>
        <p class="stages__subtitle">
          The app is divided into three different stages to help you choose
          appropriate exercises. Each exercise is carefully selected to ensure safe and
          appropriate adjustments to follow the pregnancy's progress.
        </p>
        <div class="stages__divider"></div>
      </div>

      <div class="stages__row stages__row--right">
        <div class="stages__content">
          <h3 class="stages__stage-title">Before pregnancy</h3>
          <div class="stages__divider-stage"></div>
          <p class="stages__stage-text">
            Start preparing for pregnancy with safe exercises that build up a strong body.
          </p>
          <h4 class="stages__stage-subtitle">Trimesters</h4>
          <p class="stages__stage-text">
            The pregnancy is divided into first trimester, second trimester part 1 and 2,
            and third trimester part 1 and 2 to provide exercises that are safe for each
            stage of the pregnancy. Each exercise comes with a video and a description so
            you can safely perform each exercise. Simple put in your due date and you will
            be taken to the proper stage.
          </p>
        </div>
        <div class="stages__phone">
          <img src="@/assets/image/rightPhone.png" alt="Before pregnancy app" />
        </div>
      </div>

      <div class="stages__watermark-wrap">
        <div class="stages__watermark" aria-hidden="true">Healthy</div>
      </div>

      <div class="stages__row stages__row--left">
        <div class="stages__phone">
          <img src="@/assets/image/leftPhone.png" alt="During pregnancy app" />
        </div>
        <div class="stages__content">
          <h3 class="stages__stage-title">During pregnancy</h3>
          <div class="stages__divider-stage"></div>
          <p class="stages__stage-text">
            Working out during pregnancy has many benefits for both the mom and the baby.
            It can reduce back pain, help prevent gestational diabetes, promote good posture,
            strength and endurance, and also improve the ability to cope with labor.
          </p>
        </div>
      </div>

    </div>
  </section>
</template>


<style scoped>
.stages {
  padding: 60px 0;
}

.stages__container {
  max-width: 1200px;
  margin: 0 auto;
}

.stages__header {
  text-align: center;
  margin-bottom: 60px;
}

.stages__title {
  font-size: 50px;
  font-weight: 700;
  line-height: 100%;
  color: var(--color-dark-text);
  margin: 20px 0 20px 0;
}

.stages__subtitle {
  font-size: 32px;
  font-weight: 500;
  color: var(--color-light-text);
  margin: 0 auto;
  line-height: 100%;
}

.stages__divider {
  width: 45px;
  height: 3px;
  background-color: var(--color-divider);
  margin: 20px auto 30px auto;
}

.stages__row {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 60px;
  align-items: center;
  position: relative;
  z-index: 1;
}

.stages__row--right {
  margin-bottom: 40px;
}

.stages__row--left {
  margin-top: 40px;
}

.stages__row--left .stages__phone {
  grid-column: 1;
  grid-row: 1;
}

.stages__row--left .stages__content {
  grid-column: 2;
  grid-row: 1;
}

.stages__content {
  padding-top: 80px;
}

.stages__stage-title {
  font-size: 38px;
  font-weight: 700;
  color: var(--color-dark-text);
  margin: 0 0 16px 0;
}

.stages__divider-stage {
  width: 45px;
  height: 3px;
  background-color: var(--color-divider);
  margin: 16px auto 18px 0;
}

.stages__stage-subtitle {
  font-size: 26px;
  font-weight: 600;
  color: var(--color-light-text);
  margin: 20px 0 10px 0;
  line-height: 100%;
}

.stages__stage-text {
  font-size: 18px;
  font-weight: 400;
  color: var(--color-light-text);
  line-height: 28px;
  margin: 0 0 12px 0;
}

.stages__phone {
  display: flex;
  justify-content: center;
}

.stages__phone img {
  width: 550px;
  height: auto;
  object-fit: contain;
}

.stages__watermark-wrap {
  position: relative;
  height: 0;
  overflow: visible;
  z-index: 0;
}

.stages__watermark {
  position: absolute;
  left: 60%;
  transform: translateX(-50%);
  top: -90px;
  font-size: 220px;
  font-weight: bolder;
  color: #F8F7FC;
  line-height: 1;
  white-space: nowrap;
  user-select: none;
  pointer-events: none;
  letter-spacing: -6px;
}
</style>