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
        <a href="#"><img src="@/assets/icons/Facebook.png" alt="Facebook"></a>
        <a href="#"><img src="@/assets/icons/Instagram.png" alt="Instagram"></a>
        <a href="#"><img src="@/assets/icons/YouTube.png" alt="YouTube"></a>
        <a href="#"><img src="@/assets/icons/Pinterest.png" alt="Pinterest"></a>
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
  padding: 50px 0;
  display: flex;
  align-items: flex-start;
  justify-content: flex-start;
  gap: 80px;
}

.footer__logo {
  font-weight: bold;
  font-size: 35px;
  color: var(--color-white);
  line-height: 1;
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
  font-size: 20px;
  line-height: 1.2;
  margin-bottom: 20px;
  transition: opacity 0.2s ease;
}

.footer__nav-col a:hover {
  opacity: 0.7;
}

.footer__social {
  display: flex;
  gap: 16px;
}

.footer__social a {
  display: inline-block;
  transition: transform 0.2s ease;
}

.footer__social a:hover {
  transform: scale(1.1);
}

.footer__social img {
  width: 28px;
  height: 28px;
}

@media (max-width: 1260px) {
  .footer__container {
    padding: 50px 60px;
    gap: 40px;
  }
  .footer__nav {
    gap: 80px;
  }
}

@media (max-width: 768px) {
  .footer__container {
    flex-direction: column;
    align-items: center;
    text-align: center;
    padding: 50px 60px;
    gap: 40px;
  }
  .footer__nav {
    gap: 60px;
  }
  .footer__nav-col {
    align-items: center;
  }
}

@media (max-width: 480px) {
  .footer__container {
    padding: 40px 16px;
    gap: 30px;
  }
  .footer__logo {
    font-size: 28px;
  }
  .footer__nav {
    flex-direction: column;
    gap: 20px;
  }
  .footer__nav-col a {
    font-size: 16px;
    margin-bottom: 12px;
  }
}
</style>