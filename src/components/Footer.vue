<template>
  <footer class="bg-dark">
    <div class="footer d-block flex-column">

      <div class="info">
        <h3>Our Team:</h3>
        <p>John-Bruce Noad: Ph - 063 681 3151, Email - johnnoad04@gmail.com</p>
        <p>Mishaine Isaacs: Ph -     , Email -     @gmail.com</p>
        <p>Brandon Swinton: Ph -     , Email -     @gmail.com</p>
        <p>Meezaan Davids: Ph -     , Email -     @gmail.com</p>
        <p>Camryn Herandien: Ph -     , Email -     @gmail.com</p>
        <p></p>
      </div>

      <div class="container-fluid d-flex justify-content-center align-items-center footer-items">
        <div class="github footer-item">
          <a href="https://github.com/Zile10" target="_blank">
            <img src="https://img.icons8.com/ios-glyphs/30/FFFFFF/github.png" loading="lazy" class="d-inline">
            <p class="d-inline">Github</p>
          </a>
        </div>
        <div class="gmail footer-item">
          <a href="mailto:johnnoad04@gmail.com" target="_blank">
            <img src="https://img.icons8.com/fluency/48/null/gmail.png" loading="lazy" class="d-inline">
            <p class="d-inline">Gmail</p>
          </a>
        </div>
        <div class="codepen footer-item">
          <a href="https://codepen.io/Zile10" target="_blank">
            <img src="https://img.icons8.com/ios/50/FFFFFF/codepen.png" loading="lazy" class="d-inline">
            <p class="d-inline">Codepen</p>
          </a>
        </div>
      </div>
      <div class="copyright">
        <p>Copyright &copy; 2022</p>
      </div>

    </div>
  </footer>
</template>

<script>
export default {
  
}
</script>

<style scoped>
  footer {
    box-shadow: 0 0 6px 4px black;
    z-index: 20;
    min-height: var(--navHeight);
    top: 0;
    padding: 15px;
    text-align: center;
    word-wrap: break-word;
    color: #fff;
  }

  footer .info p {
    margin: 2px auto;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
  }
  footer a {
    text-decoration: none;
    color: white;
  }
  footer .footer-item:hover {
    scale: 1.05;
  }
  .footer-item {
    margin: 5px 20px;
  }

  footer img {
    width: 25px;
  }
</style>