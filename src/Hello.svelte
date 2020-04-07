<script>
  import Photo from '../assets/photo.jpg';
  import BgImage from '../assets/bg.jpg';
</script>
<style lang="scss">
  $image-width: 462px;

  .main {
    display: flex;
    /*width: calc(100% - 77px);*/
    /*padding-left: 77px;*/
    /*position: relative;*/
  }

  .image-frame {
    margin-left: calc(27px - #{$image-width});
    position: relative;
    border-radius: 100px;
    min-width: 462px;
    width: $image-width;
    height: $image-width;
    border: solid 1px var(--light-navy);
    /*z-index: 2;*/
  }

  .image-wrapper {
    margin-left: 50px;
    position: relative;
    width: $image-width;
    height: $image-width;
    top: 26px;
  }

  img {
    border-radius: 100px;
  }

  .content-block {
    color: var(--light-navy);
    margin-left: -50px;
    padding-left: 148px;
    padding-right: 132px;
    padding-top: 58px;
    height: 685px;
    background-size: 100%;
    background-repeat: no-repeat;
    h1, h3 {
      margin: 0 20px 0 0;
      font-weight: bold;
      display: flex;
      justify-content: flex-end;
    }
    h3 {
      font-size: 24px;
      /*margin-top: 58px;*/
    }
    h1 {
      font-size: 62px;
    }
    p {
      color: var(--black);
      font-size: 18px;
      font-weight: 300;
    }
  }
</style>
<div class="main">
  <div class="image-wrapper">
    <img src={Photo} alt="photo">
  </div>
  <div class="image-frame"></div>
  <div class="content-block" style="background-image: url({BgImage})">
    <h3>Hello! My name is</h3>
    <h1>Alex Dobrushskiy</h1>
    <p>I am expirienced independent software developer, who can help you and your business to be more efficient using
      software.
      My primary professional focus is full stack web development.
      Please feel free to refer to my professional experience for more details.
      I am always happy to discuss new opportunities and help you with your project, feel free to contact me.</p>
  </div>
</div>