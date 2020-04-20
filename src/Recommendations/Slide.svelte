<script>
  export let reviewData;

</script>
<style lang="scss">
  $image-width: 300px;
  
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
<div class="content">

  <div class="image-wrapper">
    <img src={reviewData.photo} alt="photo">
  </div>
  <div class="image-frame"></div>
  <div class="review">

    <p>{reviewData.reviewContent}</p>

    <h5>{reviewData.author}</h5>
    <p>{reviewData.authorPosition}</p>

  </div>
</div>
