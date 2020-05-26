<template>
  <div class="product">
    <div class="main-img-box">
      <div class="bg-gray uppercase">product</div>
    </div>

    <div class="product-card padding-tb-50">
      <div class="group">
        <div class="card-box">
          <div class="img-box">
            <img src="../assets/square/cherry-mint.jpg" alt="">
          </div>
          <div class="text-box">
            <div class="j-title">Cherry</div>
            <div class="j-text">10,000</div>
          </div>
        </div>
        <div class="card-box">
          <div class="img-box">
            <img src="../assets/square/lemon.jpg" alt="">
          </div>
          <div class="text-box">
            <div class="j-title">Lemon</div>
            <div class="j-text">10,000</div>
          </div>
        </div>
        <div class="card-box">
          <div class="img-box">
            <img src="../assets/square/strawberry.jpg" alt="">
          </div>
          <div class="text-box">
            <div class="j-title">Strawberry</div>
            <div class="j-text">10,000</div>
          </div>
        </div>
        <div class="card-box">
          <div class="img-box">
            <img src="../assets/square/kiwi.jpg" alt="">
          </div>
          <div class="text-box">
            <div class="j-title">Kiwi</div>
            <div class="j-text">10,000</div>
          </div>
        </div>
        <div class="card-box">
          <div class="img-box">
            <img src="../assets/square/pomegranate.jpg" alt="">
          </div>
          <div class="text-box">
            <div class="j-title">Pomegranate</div>
            <div class="j-text">10,000</div>
          </div>
        </div>
        <div class="card-box">
          <div class="img-box">
            <img src="../assets/square/avocado.jpg" alt="">
          </div>
          <div class="text-box">
            <div class="j-title">Avocado</div>
            <div class="j-text">10,000</div>
          </div>
        </div>
        <div class="card-box">
          <div class="img-box">
            <img src="../assets/square/grapefruit.jpg" alt="">
          </div>
          <div class="text-box">
            <div class="j-title">Grapefruit</div>
            <div class="j-text">10,000</div>
          </div>
        </div>
        <div class="card-box">
          <div class="img-box">
            <img src="../assets/square/orange-slice.jpg" alt="">
          </div>
          <div class="text-box">
            <div class="j-title">Orange</div>
            <div class="j-text">10,000</div>
          </div>
        </div>
        <div class="card-box">
          <div class="img-box">
            <img src="../assets/square/apple.jpg" alt="">
          </div>
          <div class="text-box">
            <div class="j-title">Apple</div>
            <div class="j-text">10,000</div>
          </div>
        </div>
        <div class="card-box">
          <div class="img-box">
            <img src="../assets/square/lime.jpg" alt="">
          </div>
          <div class="text-box">
            <div class="j-title">Lime</div>
            <div class="j-text">10,000</div>
          </div>
        </div>
        <div class="card-box">
          <div class="img-box">
            <img src="../assets/square/watermelon.jpg" alt="">
          </div>
          <div class="text-box">
            <div class="j-title">Watermelon</div>
            <div class="j-text">10,000</div>
          </div>
        </div>      
        <div class="card-box">
          <div class="img-box">
            <img src="../assets/square/banana.jpg" alt="">
          </div>
          <div class="text-box">
            <div class="j-title">Banana</div>
            <div class="j-text">10,000</div>
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
  .product{
    text-align: center;
    .main-img-box{
      background-color: palegoldenrod;
      background-image: url(../assets/product-main-img.jpg);
      background-size: cover;
      background-position: center;
      height: 50vh;
      margin-bottom: 60px;
      .bg-gray{
        background-color: rgba(0, 0, 0, .7);
      }
    }
  }
  .product-card{
    .group{
      margin: 0 -20px;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
    }
    .card-box{
      width: 25%;
      margin-bottom: 30px;
      padding: 20px;
    }
    .img-box{ width: 100%; }
  }


  @media (max-width: 768px) {
    .product{
      .main-img-box{
        height: 40vh;
        margin-bottom: 0;
      }
    }
    .product-card{
      .group{
        margin: 0 -10px;
      }
      .card-box{
        width: 33.33333%;
        padding: 10px;
      }
    }
  }



  
  
</style>