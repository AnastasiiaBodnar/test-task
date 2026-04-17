<template>
  <section class="form">
    <div class="form__container">
      <div class="form__card">
        <h2 class="form__title">Send your data</h2>

        <div class="form__fields">
          <input class="form__input" type="text" placeholder="First Name">
          <input class="form__input" type="text" placeholder="Second Name">
          <input class="form__input" type="email" placeholder="Email">
          <input class="form__input" type="text" placeholder="Adress">
          <button class="form__btn">Submit</button>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>

.form {
  padding: 30px 0 60px 0;
}

.form__container {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  justify-content: center;
}

.form__card {
  align-items: center;
  background-image: url(/src/assets/image/bgForm.png);
  background-size: 100% 100%;
  background-repeat: no-repeat;
  border-radius: 20px;
  padding: 80px 60px 80px 60px;
  width: 1240px;
  display: flex;
  flex-direction: column;
  gap: 16px;
}

.form__title {
  margin: 0;
  font-weight: 700;
  font-size: 50px;
  line-height: 100%;
  text-align: center;
  color: var(--color-white);
}

.form__fields {
  display: flex;
  flex-direction: column;
  gap: 16px;
  width: 392px;
}

.form__input {
  width: 392px;
  height: 58px;
  padding: 14px 20px;
  border-radius: 100px;
  border: none;
  font-size: 18px;
  outline: none;
  background-color: var(--color-white);
  color: var(--color-dark-text);
}

.form__btn {
  background-color: var(--color-primary);
  border: none;
  text-align: center;
  border-radius: 100px;
  width: 392px;
  height: 58px; 
  color: var(--color-white);
  font-size: 18px;
  font-weight: 500;
  line-height: 28px;
  padding: 18px 30px;
}

@media (max-width: 1260px) {
  .form__container {
    padding: 0 60px;
  }
  .form__card {
    width: 100%;
  }
}

@media (max-width: 768px) {
  .form__container {
    padding: 0 24px;
  }
  .form__card {
    padding: 60px 30px;
    background-size: cover;
    background-position: center;
  }
  .form__title {
    font-size: 42px;
  }
  .form__fields {
    width: 100%;
    align-items: center;
  }
  .form__input, .form__btn {
    width: 100%;
    max-width: 392px;
  }
}

@media (max-width: 320px) {
  .form__container {
    padding: 0 16px;
  }
  .form__card {
    padding: 40px 20px;
  }
  .form__title {
    font-size: 34px;
  }
}
</style>