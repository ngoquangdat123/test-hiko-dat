<template>
    <a @click="scrollTop" v-show="visible" class="bottom-right" >
      <img src="~assets/icons/icon_to_top.svg" alt="">
      <span>Top</span>
    </a>
</template>

<script >

export default {
    data () {
        return {
        visible: false
        }
    },
    methods: {
        scrollTop: function () {
        this.intervalId = setInterval(() => {
            if (window.pageYOffset === 0) {
            clearInterval(this.intervalId)
            }
            window.scroll(0, window.pageYOffset - 50)
        }, 10)
        },
        scrollListener: function (e) {
        this.visible = window.scrollY > 150
        }
    },
    mounted: function () {
        window.addEventListener('scroll', this.scrollListener)
    },
    beforeDestroy: function () {
        window.removeEventListener('scroll', this.scrollListener)
    }
  
}
</script>

<style scoped lang="scss">
.bottom-right {
  position: fixed;
  bottom: 35px;
  right: 60px;
  cursor: pointer;
  display: flex;
  flex-direction: column;
  align-items: center;
  font-size: 20px;
  font-weight: 300;
}
@media screen and (max-width: 767px) {
    .bottom-right {
        right: 20px;
        font-size: 14px;
        font-weight: 300;
        img {
            width: 30px;
        }
    }
    
}
</style>