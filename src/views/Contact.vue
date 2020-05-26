<template>
  <div class="contact">
    <div class="main-img-box">
      <div class="bg-gray uppercase">contact</div>
    </div>

    <div class="content-box padding-tb-50">
      <div class="group">
        <div class="img-box padding-lr-50">
          <img src="../assets/contact-map.jpg" alt="">
        </div>
        <div class="text-box padding-lr-50 fs16">
          <input type="text" name="first-name" value="" placeholder="Name" />
          <input type="text" name="first-name" value="" placeholder="Email" />
          <textarea name="your-message" aria-required="true" placeholder="Message" rows="10"></textarea>
          <button class="green-btn uppercase">submit</button>
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
  .contact{
    text-align: center;
    .main-img-box{
      background-color: palegoldenrod;
      background-image: url(../assets/contact-main-img.jpg);
      background-size: cover;
      background-position: center;
      height: 50vh;
      margin-bottom: 60px;
      .bg-gray{ background-color: rgba(0, 0, 0, .7); }
    }

    .content-box{
      margin-bottom: 50px;
      .group{ display: flex; justify-content: center }
      .img-box{ width: 40%; overflow: hidden; }
      .text-box{
        text-align: center;
        width: 50%;
        input, textarea{
          background-color: #dedede;
          width: 100%;
          margin-bottom: 20px;
          padding: 14px 10px;
        }
        textarea{ margin-bottom: 40px; }
        input:focus, textarea:focus{ outline: none; }
        button{
          border: 1px solid #1bb850;
          border-radius: 5px;
          padding: 14px 50px;
          transition: .2s;
        }
        button:hover{
          background-color: #1bb850;
          color: #fff;
        }
      }
    }
  }



  @media (max-width: 1080px) {
    .contact{
      .content-box{
        .img-box{
          width: 50%;
          padding: 0 30px;
        }
        .text-box{ padding: 0 30px; }
      }
    }
  }

  @media (max-width: 900px) {
    .contact{
      .content-box{
        .group{ flex-direction: column; }
        .img-box{ margin: 0 auto 10px; padding: 0 20px; }
        .text-box{
          width: 80%;
          margin: 0 auto;
        }
      }
    }
  }
  
  @media (max-width: 768px) {
    .contact{
      .main-img-box{ height: 40vh; }
      .content-box{
        .img-box{ width: 60%; }
        .text-box{ width: 90%; padding: 0 20px; }
      }
    }
  }

  @media (max-width: 600px) {
    .contact{
      .content-box{
        .img-box{ width: 70%; margin-bottom: 20px; padding: 0; }
        .text-box{ width: 100%; padding: 0; }
      }
    }
  }
</style>