<template>
    <div class="about">
        <div class="about__banner">
            <div class="title">
                <div>CASINO</div>
                <div>PLAYGAME</div>
            </div>
            <div class="btn-scroll">
                <div class="text">Scroll</div>
                <img class="icon-scroll" src="~assets/icons/scroll.svg" alt="">
            </div>
            <img src="~assets/images/img_banner.png" class="img-fluid background-banner" alt="">
        </div>
        <div class="about__introduction container">
            <div class="content">
                <div class="sub-title text-subtitle">BPLAY GAME</div>
                <div class="title mt-2 text-title">WHO WE ARE</div>
                <p class="mt-4 info-content text-description">BPlay was founded in 2015 by a group of highly skilled professionals with over 15 years of experience in the iGaming industry. Today we are an international company with more than 100 employees and have operations in Malta, Ukraine, Romania, Norway, India, Myanmar and Taiwan...</p>
            </div>
            <img src="~assets/images/maps.png" class="img-fluid" alt="">
        </div>
        <div class="about__experience">
            <div class="container info-wrapper">
                <div class="info">
                    <span class="number">15</span>
                    <span class="year">YEARS</span>
                    <div class="line-red"></div>
                    <span class="description">of experience</span>
                    <span class="description">in the <span style="color:$red">iGaming</span></span>
                </div>
            </div>
            <img :src="$device.isDesktop ? require('~/assets/images/banner.png') : require('~/assets/images/banner_mobile.png')" alt="" class="w-100">
        </div>
    </div>
</template>
<script>
export default {
}
</script>
<style lang="scss" scoped>
.about {
    background: url('~assets/images/icon_1.png');
    background-repeat: no-repeat;
    background-position: 10% 38%;
    &__banner{
        position: relative;
        .title {
            position: absolute;
            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
            font-weight: 800;
            font-size: 96px;
            line-height: 113px;
            text-align: center;
            letter-spacing: 10px;
            mix-blend-mode: normal;
            text-shadow: 0px 0px 50px rgba(0, 0, 0, 0.4);
            background: linear-gradient(180deg, $white 0%, #FFECBC 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        .btn-scroll {
            position: absolute;
            left: 50%;
            top: 80%;
            transform: translate(-50%, -50%);
            display: flex;
            flex-direction: column;
            align-items: center;
            .text {
                font-size: 25px;
                line-height: 35px;
                letter-spacing: 1px;  
                font-weight: 300;
            }
            .icon-scroll {
                width: 50px;
            }
        }
    }
    &__introduction {
        margin-top: 5rem;
        .content{
            text-align: center;
            .sub-title {
                color: $red;
            }
            .title {
                color: $light-white;
            }
            .info-content {
                color: #E6E6E6;
                max-width: 70%;
                display: inline-flex;
            }
        }
        img {
            margin-top: -40px;
            margin-bottom: -70px;
        }
    }
    &__experience {
        position: relative;
        .info-wrapper {
            .info{
                display: flex;
                flex-direction: column;
                background: rgba(21, 22, 30, 0.9);
                border-radius: 0px 0px 20px 20px;
                position: absolute;
                align-items: center;
                justify-content: center;
                padding: 1rem 2rem;
                .number {
                    font-weight: bold;
                    font-size: 135px;
                    color: #F41616;
                    line-height: 140px;
                }
                .year {
                    font-weight: 600;
                    font-size: 50px;
                    color: $white;
                }
                .description {
                    font-size: 20px;
                    color: $white;
                }
                .line-red {
                    width: 50%;
                    height: 1px;
                    background: #F41616;
                    margin: .5rem 0;
                }
            }
        }
    }
}
@media screen and (max-width: 767px) {
    .about {
        background-position: -17% 27%;
        background-size: 41%;
        &__banner {
            background-size: 30%;
            background-position: -50px 100%;
            .background-banner{
                width: 100%;
                height: 50vh;
                object-fit: cover;
            }
            .title {
                font-weight: 800;
                font-size: 36px;
                line-height: 42px;
                letter-spacing: 5px;
            }
            .btn-scroll {
                .text {
                    font-size: 12px;
                    line-height: 14px;
                    letter-spacing: 1px;
                }
                .icon-scroll {
                    width: 21px;
                }
            }
        }
        &__introduction {
            .content{
                .info-content {
                    max-width: 100%;
                }
            }
            img {
                margin-top: 0;
                margin-bottom: 0;
                // transform: scale(1.2);
            }
        }
        &__experience {
            .info-wrapper {
                display: flex;
                justify-content: center;
                .info{
                    padding: 3rem;
                    width: 65%;
                    .number {
                        font-size: 80px;
                        line-height: 90px;
                    }
                    .year {
                        font-weight: 600;
                        font-size: 30px;
                    }
                    .description {
                        font-size: 17px;
                    }
                }
            }
        }
    } 
}
</style>
