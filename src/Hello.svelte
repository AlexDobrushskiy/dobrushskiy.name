<script>
  import Photo from '../assets/photo.jpg';
  import BgImage from '../assets/bg.jpg';
</script>
<style lang="scss">
  @mixin image($image-width) {
    .image-frame {
      margin-left: calc(27px - #{$image-width});
      position: relative;
      border-radius: 100px;
      min-width: $image-width;
      width: $image-width;
      height: $image-width;
      border: solid 1px var(--light-navy);
    }

    .image-wrapper {
      margin-left: 50px;
      position: relative;
      width: $image-width;
      height: $image-width;

      img {
        width: $image-width;
        height: $image-width;

      }

      top: 26px;
    }
  }

  @media (min-width: 1280px) {
    @include image($image-width: 462px);
  }

  @media (min-width: 992px) and (max-width: 1279px) {
    @include image($image-width: 358px);
  }

  @media (min-width: 769px) and (max-width: 991px) {
    @include image($image-width: 277px);
  }

  @media (max-width: 768px) {
    @include image($image-width: 358px);
  }

  .main {
    @media (min-width: 769px) {
      display: flex;
    }
  }

  .desktop {
    @media (max-width: 768px) {
      display: none;
    }
  }

  .mobile {
    @media (min-width: 769px) {
      display: none;
    }
    @media (max-width: 768px) {
      display: flex;
      margin-top: -200px;
    }

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
      @media (min-width: 1280px) {
        font-size: 24px;
      }

      @media (min-width: 992px) and (max-width: 1279px) {
        font-size: 20px;
      }

      @media (max-width: 991px) {
        font-size: 17px;
      }
      font-style: italic;
      /*margin-top: 58px;*/
    }

    h1 {
      @media (min-width: 1280px) {
        font-size: 62px;
      }

      @media (min-width: 992px) and (max-width: 1279px) {
        font-size: 46px;
      }

      @media (max-width: 991px) {
        font-size: 37px;
      }

    }

    p {
      color: var(--black);
      font-size: 18px;
      @media (max-width: 991px) {
        font-size: 15px;
      }

      font-weight: 300;
      margin-top: 20px;

      a {
        text-decoration: none;
        font-weight: 500;
        color: inherit;
      }

      b {
        font-weight: 500;
        font-style: italic;
      }
    }
  }
</style>
<div class="main" id="id-hello">
  <div class="image-wrapper desktop">
    <img src={Photo} alt="photo">
  </div>
  <div class="image-frame desktop"></div>
  <div class="content-block" style="background-image: url({BgImage})">
    <h1>Alex Dobrushskiy</h1>
    <h3>Software developer</h3>
    <p>Alex is experienced independent full stack software developer, who started his professional career in <b>2005</b>
      and has a great experience of working in small startups and big enterprises.<br/>
      Today his primary professional focus is full stack web development with Python and React.
      <br/>Alex is a member of <a href="https://www.toptal.com/resume/alex-dobrushskiy#unite-only-masterly-engineers">Toptal
        network</a>, containing top 3% of freelance talent.
  </div>
  <div class="mobile">
    <div class="image-wrapper">
      <img src={Photo} alt="photo">
    </div>
    <div class="image-frame"></div>
  </div>
</div>