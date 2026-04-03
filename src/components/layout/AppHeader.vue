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
            <button class="header__btn">Download</button>
            <div class="header__lang">Eng ▾</div>
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
  }

  .header__lang {
    font-weight: 400;
    font-size: 18px;
    line-height: 28px;
  }
  </style>