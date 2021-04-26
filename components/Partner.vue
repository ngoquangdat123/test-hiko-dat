<template>
    <div class="partner-wrapper">
      <div class="container ">
        <div class="col-12 ">
            <div class="row partner-content">
                <div class="col-md-6 partner-content__left">
                    <img src="~assets/images/img_partner.png" alt="" class="mr-2 w-100">
                </div>
                <div class="col-md-6 partner-content__right">
                    <div class="sub-title text-subtitle">BPLAY GAME</div>
                    <div class="title text-title mt-2">PARTNERS</div>
                    <p class="info-content text-description mt-4">
                    As a BPlay client you will benefit from content from more than 20 top tier providers. Based on your casino’s concept and targeted markets, we will tailor the perfect portfolio of games to offer to your players.
                    </p>
                    <img src="~assets/images/partner_logo.png" alt="" class="w-100">
                </div>
            </div>
        </div>
      </div>
    </div>
</template>
<script>
export default {
}
</script>
<style lang="scss" scoped>
.partner-wrapper {
    padding-top: 10rem;
    padding-bottom: 12rem;
    background: url('~assets/images/background_circle.png');
    background-repeat: no-repeat;
    background-size: 50% auto;
    .partner-content {
        &__left {

        }
        &__right {
            .sub-title {
                color: $red;
            }
            .title {
                color: $light-white;
            }
            .info-content {
                color: #E6E6E6;
            } 
        }
    }
}
@media screen and (max-width: 767px) {
    .partner-wrapper {
        padding-top: 5rem;
        padding-bottom: 5rem;
        background: url('~assets/images/background_circle.png');
        background-repeat: no-repeat;
        background-size: 100%;
        background-position: -1rem 100%;
        .partner-content {
            display: flex;
            flex-direction: column-reverse;
            justify-content: center;
            &__left {
                margin-top: 2rem;

            }
            &__right {
                .sub-title {
                    text-align: center;
                    color: $red;
                }
                .title {
                    text-align: center;
                    color: $light-white;
                }
                .info-content {
                    text-align: center;
                    color: #E6E6E6;
                } 
            }
        }
    }
}
</style>
