<template>
    <div class="product">
        <img :src="product.logo" alt="" class="w-100">
        <div class="product__info mt-4 px-4 w-100">
            <img src="~assets/images/frame_product.png" alt="" class="w-100">
            <span class="name">{{product.name}}</span>
        </div>
        <div class=" mt-3 product__description">{{product.description}}</div>
    </div>
</template>
<script>
export default {
    props: ['product']
}
</script>
<style lang="scss" scoped>
.product {
    margin-bottom: 4rem;
    &__info {
         position: relative;
        text-align: center;
        color: white;
        .name {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-weight: bold;
            font-size: 25px;
            line-height: 30px;
            letter-spacing: 1px;
            color: #FFFDF1;
            width: 100%;
        }
    }
    &__description {
        text-align: center;
        font-size: 16px;
        line-height: 28px;
        letter-spacing: 1px;
        color: $white;
        padding: 0 .5rem;
    }
}
@media screen and (max-width: 767px) {
    .product {
        padding: .75rem;
        margin-bottom: 0;
        &__info {
            position: relative;
            text-align: center;
            color: white;
            .name {
                position: absolute;
                top: 50%;
                left: 50%;
                transform: translate(-50%, -50%);
                font-weight: bold;
                font-size: 16px;
                line-height: 19px;
                letter-spacing: 1px;
                color: #FFFDF1;
                width: 100%;
            }
        }
        &__description {
            text-align: center;
            font-size: 14px;
            line-height: 26px;
            letter-spacing: 1px;
            color: $white;
        }
    }
}
</style>
