<template>
  <nav class="header navbar navbar-expand-lg navbar-light ">
    <div class="container">
      <img src="~/assets/images/Logo.svg" class="logo"/>
      <div class="collapse navbar-collapse" id="navbarToggler">
        <ul class="navbar-nav mr-auto mt-lg-0 w-100 justify-content-center">
          <li class="nav-item mr-3 active">
            <a class="nav-link" href="#">ABOUT US <span class="sr-only">(current)</span></a>
          </li>
          <li class="nav-item mr-3">
            <a class="nav-link" href="#">PRODUCTS</a>
          </li>
          <li class="nav-item mr-3">
            <a class="nav-link " href="#">PARTNERS</a>
          </li>
          <li class="nav-item mr-3">
            <a class="nav-link" href="#">OUR CLIENTS</a>
          </li>
          <li class="nav-item mr-3">
            <a class="nav-link " href="#">CONTACT US</a>
          </li>
        </ul>
      </div>
      <div class="d-flex justify-content-center">
        <div class="dropdown">
          <button class="dropbtn"><img src="~assets/icons/eng_flag.svg" alt=""><span class="ml-2">ENG</span></button>
          <div class="dropdown-content">
            <a href="#"><img src="~assets/icons/eng_flag.svg" alt=""><span class="ml-2">English</span></a>
            <a href="#"><img src="~assets/icons/eng_flag.svg" alt=""><span class="ml-2">Vietnamese</span></a>
            <a href="#"><img src="~assets/icons/eng_flag.svg" alt=""><span class="ml-2">Japanese</span></a>
          </div>
        </div>
        <button class="navbar-toggler ml-4" type="button" data-toggle="collapse" data-target="#navbarToggler" aria-controls="navbarToggler" aria-expanded="false" aria-label="Toggle navigation">
          <img src="~/assets/images/custom_toggle.svg" alt="">
        </button>
      </div>
    </div>
  </nav>
</template>

<script>

export default {
  name: 'TheHeader',
  components: {
  },
  data() {
    return {
    }
  },
}
</script>
<style scoped lang="scss">
  .nav-link {
    color: $white !important;
    font-weight: bold;
  }
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
.header {
  z-index: 1000;
  height: 100px;
  background: transparent;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  .dropbtn {
    background: transparent;
    color: white;
    padding: 10px 16px;
    font-size: 16px;
    align-items: center;
    cursor: pointer;
    border-radius: 30px;
    border: 1px solid $white;
    font-weight: 600;
    display: flex;
    justify-content: center;
    &::after {
      content: url("~assets/icons/icon_polygon.svg");
      margin-left: 25px;
    }
  }

  .dropdown {
    position: relative;
    display: inline-block;
  }
  .navbar-toggler {
    padding: 0;
  }
  .dropdown-content {
    display: none;
    position: absolute;
    background-color: #f9f9f9;
    min-width: 160px;
    box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
    z-index: 1;
  }

  .dropdown-content a {
    color: black;
    padding: 12px 16px;
    text-decoration: none;
    display: block;
  }

  .dropdown-content a:hover {background-color: #f1f1f1}

  .dropdown:hover .dropdown-content {
    display: block;
  }
}
@media screen and (max-width: 767px) {
  .header {
    height: 70px;
    .logo {
      width: 100px;
    }
    .dropbtn {
      padding: 5px 8px;
      &::after {
        content: url("~assets/icons/icon_polygon.svg");
        margin-left: 10px;
      }
    }
  } 
}

</style>