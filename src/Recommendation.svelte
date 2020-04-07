<script>
  import Photo from '../assets/photo.jpg';
  import BgImage from '../assets/bg1.jpg';
</script>
<style lang="scss">

  $image-width: 300px;
  .main {
    min-height: 777px;
    background-position: 68px;
    background-repeat: no-repeat;
    background-size: calc(100% - 50px);
  }
  h1 {
    margin-left: 68px;
    margin-top: 20px;
    font-size: 48px;
    color: var(--light-navy);
    margin-bottom: 0;
  }

  .content {
    display: flex;

    .image-wrapper {
      margin-top: 50px;
      margin-left: 68px;
      /*position: relative;*/
      width: $image-width;
      height: $image-width;

      img {
        border-radius: 100px;
        width: $image-width;
        height: $image-width;
      }
    }

    .image-frame {
      margin-top: 33px;
      margin-left: calc(17px - #{$image-width});
      border-radius: 100px;
      min-width: $image-width;
      width: $image-width;
      height: $image-width;
      border: solid 1px var(--light-navy);
    }
    .review {
      margin-top: 136px;
      margin-left: 56px;
      max-width: 530px;
      p {
        font-size: 18px;
        font-weight: 300;
        color: var(--black);
      }
      h5 {
        margin-top: 40px;
        margin-bottom: 14px;
        color: var(--dark-grey);
        font-size: 24px;
        font-weight: bold;
      }
    }
  }


</style>
<div class="main" style="background-image: url({BgImage})">
  <h1>Recommendations</h1>
  <div class="content">
    <div class="image-wrapper">
      <img src={Photo} alt="photo">
    </div>
    <div class="image-frame"></div>
    <div class="review">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla ut mattis eros, a sagittis risus. Nullam feugiat, risus eu vehicula dictum, enim arcu posuere sapien, in sodales enim neque eget elit. Nam fermentum eu metus id vehicula. Aliquam eleifend augue a semper lacinia. Maecenas eleifend lacus magna, a dignissim nisi laoreet sollicitudin. Quisque congue eu lectus tincidunt dignissim. Nunc at dolor eros. Pellentesque consequat mauris ac mi volutpat egestas. Nulla facilisi.</p>
      <h5>Some Author</h5>
      <p>DIRECTOR OF ENGINEERING AT DUNNHUMBY</p>
    </div>
  </div>
</div>