<template>
  <footer class=" container">
    <div class="footer">
      <div class="d-flex footer__logo">
        <img class="license" src="~assets/images/footer_logo1.png" alt="">
        <div class="d-flex partner">
          <img src="~assets/images/footer_logo2.png" alt="">
          <img src="~assets/images/footer_logo3.png" alt="">
          <img src="~assets/images/footer_logo4.png" alt="">
        </div>
      </div>
      <span class="footer__copyright">Copyright © 2020 bplay.com. All rights reserved.</span>
    </div>
  </footer>
</template>

<script>

export default {
  name: 'TheFooter',
  components: {
  }
}
</script>
<style scoped lang="scss">
@media screen and (min-width: 1500px){
    .container {
        max-width: 1344px !important;
    }
}
@media screen and (min-width: 1280px){
    .container {
      max-width: 1152px;
    }
}
.footer {
  margin-top: 3rem;
  background: transparent;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 2rem 0;
  border-top: 0.5px solid #424657;
  &__copyright {
    font-size: 14px;
    line-height: 28px;
    color: $white;
    opacity: 0.7;
  }
  &__logo{
    .license {

    } 
    .partner {
      img {
        margin-left: 2rem;
      }
    }
  }
}
@media screen and (max-width: 767px) {
  .footer {
    display: flex;
    flex-direction: column;
    padding: 2rem 0 0 0;
    &__copyright {
      font-size: 12px;
      line-height: 28px;
      color: $white;
      opacity: 0.7;
      border-top: 0.5px solid #424657;
      padding: 1rem 0;
      width: 100%;
      margin-top: 2rem;
      display: flex;
      justify-content: center;
    }
    &__logo {
      flex-direction: column-reverse;
      width: 80%;
      .license {
        margin-top: 2rem;
      }
      .partner {
        display: flex;
        justify-content: space-between;
        img {
          margin: 0;
        }
      }
    }
  }
}
</style>