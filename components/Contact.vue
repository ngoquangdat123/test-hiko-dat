<template>
    <div class="contact-wrapper">
      <div class="container">
        <div class="col-12 row">
          <div class="col-md-6">
            <img src="~/assets/images/Logo.svg" class="footer-logo"/>
          </div>
          <div class="col-md-6 info">
            <div class="title">CONTACT US</div>
            <div class="mt-3 d-flex align-items-center">
              <img src="~assets/icons/place.svg" alt="" class="icon">
              <span class="description ml-3">2901 Marmora Road, Glassgow, Seattle, WA 98122-1090</span>
            </div>
            <div class="mt-3 d-flex align-items-center">
              <img src="~assets/icons/mail.svg" alt="" class="icon">
              <span class="description ml-3">info@bplay.com</span>
            </div>
          </div>
        </div>
      </div>
     <the-footer />
    </div>
</template>
<script>
import TheFooter from '../components/TheFooter.vue'

export default {
    components: {
        TheFooter,
    },
}
</script>
<style lang="scss" scoped>
.contact-wrapper {
    padding-top: 15rem;
    background: url('~assets/images/background_footer.png');
    margin-top: -5rem;
    background-repeat: no-repeat;
    background-size: 100% 100%;
    .info {
        .title {
            font-weight: 800;
            font-size: 34px;
            line-height: 40px;
            color: $light-white;
        }
        .description {
            font-size: 18px;
            line-height: 40px;
            color: $white;
        }
        .icon {
            width: 24px;
            height: 24px;
        }
    }
    
}
@media screen and (max-width: 767px) {
    .contact-wrapper {
        padding-top: 7rem;
        background: url('~assets/images/background_footer_mobile.png');
        margin-top: 0;
        background-repeat: no-repeat;
        background-size: 100% 100%;
        .footer-logo {
            width: 120px
        }
        .info {
            margin-top: 2rem;
            .title {
                font-size: 18px;
                line-height: 21px;
            }
            .description {
                font-size: 16px;
                line-height: 23px;
                color: $white;
            }
            .icon {
                width: 18px;
                height: 18px;
            }
        }
    }
}
</style>
