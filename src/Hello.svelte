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
      font-style: italic;
      /*margin-top: 58px;*/
    }
    h1 {
      font-size: 62px;
    }
    p {
      color: var(--black);
      font-size: 18px;
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
  <div class="image-wrapper">
    <img src={Photo} alt="photo">
  </div>
  <div class="image-frame"></div>
  <div class="content-block" style="background-image: url({BgImage})">
    <h1>Alex Dobrushskiy</h1>
    <h3>Software developer</h3>
    <p>Alex is expirienced independent full stack software developer, who started his professional career in <b>2005</b> and has a great experience of working in small startups and big enterprises.<br/>
      Today his primary professional focus is full stack web development with Python and React.
      <br/>Alex is a member of <a href="https://www.toptal.com/resume/alex-dobrushskiy#unite-only-masterly-engineers">Toptal network</a>, containing top 3% of freelance talent.
  </div>
</div>