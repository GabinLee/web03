<template>
  <div class="about">
    <div class="main-img-box">
      <div class="bg-gray uppercase">about</div>
    </div>

    <div class="content-box padding-tb-50">
      <div class="j-top-head">Our story</div>
      <div class="group">
        <div class="box">
          <div class="img-box">
            <img src="../assets/about/about-content01.jpg" alt="">
          </div>
          <div class="mobile-img-box">
            <img src="../assets/about/mobile-about01.jpg" alt="">
          </div>
          <div class="text-box">
            <div class="j-text">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</div>
          </div>
        </div>

        <div class="box">
          <div class="img-box">
            <img src="../assets/about/about-content02.jpg" alt="">
          </div>
          <div class="mobile-img-box">
            <img src="../assets/about/mobile-about02.jpg" alt="">
          </div>
          <div class="text-box">
            <div class="j-text">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</div>
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
  .main-img-box{
    background-color: palegoldenrod;
    background-image: url(../assets/about/about-main-img.jpg);
    background-size: cover;
    background-position: center;
    height: 50vh;
    margin-bottom: 50px;
    .bg-gray{
      background-color: rgba(0, 0, 0, .6);
    }
  }

  .content-box{
    text-align: center;
    .j-top-head{ margin-bottom: 0; }
    .group{
      margin: 0 -40px;
      display: flex;
      flex-wrap: wrap;
    }
    .box{
      width: 50%;
      padding: 40px;
    }
    .mobile-img-box{
      display: none;
    }
  }



  @media (max-width: 900px) {
    .content-box{
      .group{ margin: 0 -30px; }
      .box{ padding: 30px; }
    }
  }

  @media (max-width: 768px) {
    .main-img-box{ height: 40vh; }

    .content-box{
      .group{ margin: 0 -20px; }
      .box{
        width: 100%;
        margin-bottom: 30px;
        padding: 20px;
      }
      .img-box{ display: none; }
      .mobile-img-box{ display: block; }
    }
  }

  @media (max-width: 600px) {
    .content-box{
      .box{ margin-bottom: 20px; }
    }
  }




</style>