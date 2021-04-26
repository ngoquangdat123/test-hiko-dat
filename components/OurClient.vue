<template>
    <div class="client-wrapper">
      <div class="container info">
        <div class="sub-title text-subtitle">BPLAY GAME</div>
        <div class="title mt-2 text-title">OUR CLIENTS</div>
        <div class="col-12 client-list">
            <div class="row d-flex justify-content-center">
                <div v-for="(partner, i) in partners" :key="i" :class="$device.isDesktop ? 'col-2dot4' : 'col-4'">
                    <img :src="partner" alt="" class="w-100 client-logo">
                </div>
            </div>
        </div>
      </div>
    </div>
</template>
<script>
export default {
    data(){
        return {
            partners: [require('~/assets/images/client1.png'),
                require('~/assets/images/client2.png'),
                require('~/assets/images/client3.png'),
                require('~/assets/images/client4.png'),
                require('~/assets/images/client5.png'),
                require('~/assets/images/client6.png'),
                require('~/assets/images/client7.png'),
                require('~/assets/images/client8.png'),
                require('~/assets/images/client9.png'),
                require('~/assets/images/client10.png'),
                require('~/assets/images/client11.png'),
                require('~/assets/images/client12.png')
            ]
        }
    }
}
</script>
<style lang="scss" scoped>
.client-wrapper {
    margin-top: 5rem;
    .info {
        text-align: center;
    }
    .sub-title {
        color: $red;
    }
    .title {
        color: $light-white;
    }
    .client-list {
        margin-top: 2rem;
        .client-logo {
            margin-top: 2rem;
        }
    }
    
}
@media screen and (max-width: 767px) {
    .client-wrapper {
        .client-list {
            .client-logo {
                margin-top: 1.25rem;
            }
        }
    }
}
</style>
