<style>
  .contact-info-wrapper {
    margin: 10%;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .text {
    width: 50%;
    letter-spacing: 0.04em;
    font-size: 18px;
    margin-bottom: 18px;
  }
  .contact-title {
    font-weight: bold;
    font-size: 18px;
    letter-spacing: 0.1em;
    margin: 36px 0 18px 0;
    color: #ffffff;
  }
  .contact-text {
    font-size: 16px;
    line-height: 28px;
    color: #ffffff;
  }
  .input {
    width: 100%;
    height: 100%;
    font-size: 18px;
    background: #202020;
    color: #ffffff;
    border: none;
    padding: 0 12px;
  }
  .button {
    display: flex;
    align-items: center;
    justify-content: center;
    background: white;
    max-width: 80px;
    flex: 2;
  }
  .input-wrapper {
    background: red;
    flex: 8;
  }
  .form {
    width: 50%;
    height: 60px;
    background: aliceblue;
    display: flex;
  }
  .form-wrapper {
    background: #100f10;
    min-width: 360px;
    flex: 6;
    padding: 80px 0;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
  }
  .contact-info {
    background: var(--main-black);
    flex: 4;
  }
  .footer-wrap {
    display: flex;
    flex-wrap: wrap;
    min-height: 460px;
    color: #ffffff;
  }
  .btn-img {
    height: 25px;
    object-fit: cover;
  }
</style>

<div class="footer-wrap">
  <div class="form-wrapper">
    <div class="text">Regístrate en nuestro newsletter</div>
    <div class="form">
      <div class="input-wrapper">
        <input
          class="input"
          placeholder="Enter your email"
          type="email"
          name="email"
          id="email" />
      </div>
      <div class="button">
        <img class="btn-img" src="right-arrow.svg" alt="Registrar" />
      </div>
    </div>
  </div>
  <div class="contact-info-wrapper">
    <div class="contact-info">
      <p class="contact-title">GET IN TOUCH</p>
      <p class="contact-text">hola@hackademy.mx</p>
      <p class="contact-text">+52 6675738836</p>
      <p class="contact-title">FOLLOW US</p>
      <p class="contact-text">Facebook/Twitter/IG</p>
      <p class="contact-text">@hackademymx</p>
    </div>
  </div>
</div>
