<script>
  import Photo from '../assets/photo.jpg';
</script>
<style lang="scss">
  @mixin image($image-width) {
    .image-frame {
      margin-left: calc(27px - #{$image-width});
      position: relative;
      border-radius: 100px;
      @media (max-width: 768px) {
        border-radius: 15vw;
        margin-left: calc(10px - #{$image-width});
      }

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
      top: 26px;
      @media (max-width: 768px) {
        margin-left: 20px;
        top: 10px;
      }

      img {
        width: $image-width;
        height: $image-width;

      }


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
    @include image($image-width: 40vw);
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
      width: 100vw;
      margin-left: -40px;
    }

  }

  img {
    border-radius: 100px;
    @media (max-width: 768px) {
      border-radius: 15vw;
    }
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
    background-image: url("/images/bg.jpg");
    @media (max-width: 768px) {
      padding: 20px;
      margin-left: 0;

      height: inherit;
      background-repeat: repeat;
    }

    h1, h3 {
      margin: 0 20px 0 0;
      font-weight: bold;
      display: flex;
      justify-content: flex-end;
    }

    h3 {
      font-size: 1.87vw;
      @media (max-width: 768px) {
        font-size: 14px;
      }

      font-style: italic;
    }

    h1 {
      font-size: 4.85vw;
      @media (max-width: 768px) {
        font-size: 22px;
      }

    }

    p {
      color: var(--black);
      font-size: 1.24vw;
      @media (max-width: 768px) {
        font-size: 12px;
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

    .content-container {
      @media (max-width: 786px) {
        display: flex;
      }
    }
  }
</style>
<div class="main" id="id-hello">
  <div class="image-wrapper desktop">
    <img src={Photo} alt="photo">
  </div>
  <div class="image-frame desktop"></div>

  <div class="content-block">
    <div class="content-container">
      <div class="mobile">
        <div class="image-wrapper">
          <img src={Photo} alt="photo">
        </div>
        <div class="image-frame"></div>
      </div>
      <div>
        <h1>Alex Dobrushskiy</h1>
        <h3>Software developer</h3>
      </div>
    </div>
    <p>Alex is experienced independent full stack software developer, who started his professional career in <b>2005</b>
      and has a great experience of working in small startups and big enterprises.<br/>
      Today his primary professional focus is full stack web development with Python and React.
      <br/>Alex is a member of <a href="https://www.toptal.com/resume/alex-dobrushskiy#unite-only-masterly-engineers">Toptal
        network</a>, containing top 3% of freelance talent.
  </div>
</div>