<script>
  export let reviewData;
  import Icon from 'fa-svelte';
  import { faLinkedin } from '@fortawesome/free-brands-svg-icons/faLinkedin';
</script>
<style lang="scss">

  @mixin image($image-width) {
    .image-wrapper {
      margin-top: 50px;
      margin-left: 68px;
      /*position: relative;*/
      width: $image-width;
      height: $image-width;

      img {
        border-radius: calc(#{$image-width}/4);
        width: $image-width;
        height: $image-width;
      }

    }

    .image-frame {
      margin-top: 33px;
      margin-left: calc(17px - #{$image-width});
      border-radius: calc(#{$image-width}/4);
      min-width: $image-width;
      width: $image-width;
      height: $image-width;
      border: solid 1px var(--light-navy);
    }
  }

  @media (min-width: 1280px) {
    @include image($image-width: 300px);
  }

  @media (min-width: 992px) and (max-width: 1279px) {
    @include image($image-width: 225px);
  }

  @media (max-width: 991px) {
    @include image($image-width: 180px);
  }

  .content {
    display: flex;


    .review {
      margin-top: 136px;
      margin-left: 56px;
      max-width: 530px;

      p {
        font-size: 18px;
        font-weight: 300;
        color: var(--black);
        font-style: italic;
      }

      h5 {
        margin-top: 40px;
        margin-bottom: 14px;
        color: var(--dark-grey);
        font-size: 24px;
        font-weight: bold;

        a {
          text-decoration: none;
          color: inherit;

          span {
            margin-left: 15px;
            color: var(--line-blue)
          }
        }
      }

    }
  }

</style>
<div class="content">

  <div class="image-wrapper">
    <img src={reviewData.photo} alt="photo">
  </div>
  <div class="image-frame"></div>
  <div class="review">

    <p>"{reviewData.reviewContent}"</p>

    <h5>
      <a href={reviewData.authorLinkedin}> {reviewData.author} <span><Icon icon={faLinkedin}/></span></a>
    </h5>
    <p>{reviewData.authorPosition}</p>

  </div>
</div>
