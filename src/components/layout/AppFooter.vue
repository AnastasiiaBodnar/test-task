<template>
  <footer class="footer">
    <div class="footer__container"> 
      <div class="footer__logo">
      LOGO
      </div>

      <nav class="footer__nav">
        <div class="footer__nav-col">
          <a href="#">About us</a>
          <a href="#">Blog</a>
          <a href="#">Support</a>
        </div>

        <div class="footer__nav-col">
          <a href="#">Terms & Conditions</a>
          <a href="#">Privacy Policy</a>
          <a href="#">Cookies</a>
        </div>
      </nav>

      <div class="footer__social">
        <a href="#"><img src="/src/assets/icons/Facebook.png" alt="Facebook"></a>
        <a href="#"><img src="/src/assets/icons/Instagram.png" alt="Instagram"></a>
        <a href="#"><img src="/src/assets/icons/YouTube.png" alt="YouTube"></a>
        <a href="#"><img src="/src/assets/icons/Pinterest.png" alt="Pinterest"></a>
      </div>
    </div>
  </footer>
</template>

<style scoped>

.footer {
  background: #423C4E;
}

.footer__container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 60px 24px;
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
}

.footer__logo {
  font-weight: 700;
  font-size: 40px;
  line-height: 100%;
  color: var(--color-white);
}

.footer__nav {
  display: flex;
  gap: 180px;
}

.footer__nav-col {
  display: flex;
  flex-direction: column;
}

.footer__nav-col a {
  text-decoration: none;
  color: var(--color-white);
  font-weight: 400;
  font-size: 24px;
  line-height: 50px;
}

.footer__social {
  display: flex;
  gap: 16px;
}

.footer__social img {
  width: 32px;
  height: 32px;
}
</style>