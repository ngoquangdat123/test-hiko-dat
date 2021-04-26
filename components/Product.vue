<template>
    <div class="product-wrapper">
      <div class="container">
        <div class="product-wrapper__introduction col-12">
          <div class="row">
            <div class="col-md-4 ">
              <div class="sub-title text-subtitle">BPLAY GAME</div>
              <div class="mt-2 title text-title">OUR PRODUCTS</div>
            </div>
            <div class="col-md-8">
              <p class="info-content text-description">BPlay’s high quality iGaming Platform offers a complete solution for your casino. Get the full White Label turnkey solution or the Seamless API with our comprehensive selection of games. Through our global network of premium partners such as Vivo Gaming, SBTech and HoGaming you will have access to the best Live Casino, Sportsbook, Slots, Table Games, Number Games and Fishing Games on the market.</p>
            </div>
          </div>
        </div>
        <div class="product-wrapper__list col-12" v-if="$device.isDesktop">
          <div class="row">
            <div class="col-md-4 item"  v-for="(product, index) in products" :key="index">
              <product-item :product="product"/>
            </div>
          </div>
        </div>
        <div v-else class="product-wrapper__list">
            <client-only>
                <carousel :perPage="1.5" class="">
                    <slide :data-index="index" v-for="(product, index) in products" :key="index">
                        <product-item :product="product"/>
                    </slide>
                </carousel>
            </client-only>
        </div>
      </div>
    </div>
</template>
<script>
import ProductItem from '../components/ProductItem.vue'

export default {
    components: {
        ProductItem,
    },
    data() {
        return {
            products: [
                { logo: require('~/assets/images/product_1.png'),
                name: 'Live Casino',
                description: 'Vivo LiveCasino, HoGaming Live Casino, BPlay LiveCasino'
                },
                { logo: require('~/assets/images/product_2.png'),
                name: 'Fishing Game',
                description: 'BPlay Fishing 2D, BPlay Fishing 3D'
                },
                { logo: require('~/assets/images/product_3.png'),
                name: 'Sport Book',
                description: 'BTI Sportsbook, BPlay Sportsbook'
                },
                { logo: require('~/assets/images/product_4.png'),
                name: 'Quick Number',
                description: 'Keno, Number Games, Lottery'
                },
                { logo: require('~/assets/images/product_5.png'),
                name: 'White Label',
                description: 'Bplay White Label'
                },
                { logo: require('~/assets/images/product_6.png'),
                name: 'Slots',
                description: 'BPlay Slots, Jackpot Slots'
                },
                { logo: require('~/assets/images/product_7.png'),
                name: 'Seamless API',
                description: 'Seamless API'
                },
                { logo: require('~/assets/images/product_8.png'),
                name: 'Full Package',
                description: 'Full Package'
                },
                { logo: require('~/assets/images/product_9.png'),
                name: 'Table Game',
                description: 'Table Game'
                },
            ]
        }
    },
}
</script>
<style lang="scss" scoped>
.product-wrapper {
  padding-top: 10rem;
  background: url('~assets/images/background_product.png');
  margin-top: -25px;
  background-repeat: no-repeat;
  background-size: 100% 100%;
  padding-bottom: 10rem;
  &__introduction {
    .sub-title {
      color: $red;
    }
    .title {
      color: $light-white;
      font-size: 45px;
    }
    .info-content {
      color: #EAEAEA;
    }
  }
  &__list {
      margin-top: 3rem;
  }
}
@media screen and (max-width: 767px) {
    .container {
      margin: 0;
      padding: 0;
    }
    .product-wrapper {
      padding-top: 5rem;
      background: url('~assets/images/background_product_mobile.png');
      margin-top: 0;
      background-repeat: no-repeat;
      background-size: 100% 100%;
      padding-bottom: 5rem;
      &__introduction {
        display: flex;
        justify-self: center;
        .sub-title {
          color: $red;
          text-align: center;
        }
        .title {
          color: $light-white;
          text-align: center;
          font-size: 26px;
        }
        .info-content {
          margin-top: 1.5rem;
          color: #EAEAEA;
          text-align: center;
        }
      }
    }
}
/deep/ .VueCarousel-dot {
    border-radius: 0;
    transform: rotate(45deg);
    background-color: #505153 !important;
}
/deep/ .VueCarousel-dot--active {
    background-color: #F41616 !important;
}
/deep/ .VueCarousel-dot-container {
    margin: 0 !important;
}
</style>
