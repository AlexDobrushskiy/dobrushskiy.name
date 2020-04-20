<script>
  import Photo from '../assets/photo.jpg';
  import BgImage from '../assets/bg1.jpg';
  import Icon from 'fa-svelte';
  import { faArrowLeft } from '@fortawesome/free-solid-svg-icons/faArrowLeft';
  import { faArrowRight } from '@fortawesome/free-solid-svg-icons/faArrowRight';
  import Carousel from '@beyonk/svelte-carousel';
  import Slide from './Recommendations/Slide.svelte';

  const reviewsData = [
    {
      photo: Photo,
      reviewContent: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla ut mattis eros, a sagittis risus. Nullam\n' +
        '      feugiat, risus eu vehicula dictum, enim arcu posuere sapien, in sodales enim neque eget elit. Nam fermentum eu\n' +
        '      metus id vehicula. Aliquam eleifend augue a semper lacinia. Maecenas eleifend lacus magna, a dignissim nisi\n' +
        '      laoreet sollicitudin. Quisque congue eu lectus tincidunt dignissim. Nunc at dolor eros. Pellentesque consequat\n' +
        '      mauris ac mi volutpat egestas. Nulla facilisi.',
      author: 'Some Author',
      authorPosition: 'DIRECTOR OF ENGINEERING AT DUNNHUMBY1'
    },
    {
      photo: Photo,
      reviewContent: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla ut mattis eros, a sagittis risus. Nullam\n' +
        '      feugiat, risus eu vehicula dictum, enim arcu posuere sapien, in sodales enim neque eget elit. Nam fermentum eu\n' +
        '      metus id vehicula. Aliquam eleifend augue a semper lacinia. Maecenas eleifend lacus magna, a dignissim nisi\n' +
        '      laoreet sollicitudin. Quisque congue eu lectus tincidunt dignissim. Nunc at dolor eros. Pellentesque consequat\n' +
        '      mauris ac mi volutpat egestas. Nulla facilisi.',
      author: 'Some Other Author',
      authorPosition: 'DIRECTOR OF ENGINEERING AT Some Other'
    }

  ];
</script>
<style lang="scss">

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


  /*.arrows {*/
  /*  display: flex;*/
  /*  margin-top: 20px;*/

  .circle-left, .circle-right {
    width: 49px;
    height: 49px;
    border-radius: 50%;
    cursor: pointer;
    color: rgba(255, 255, 255, 0.5);
    font-size: 25px;
    line-height: 55px;
    text-align: center;
  }

  .circle-left {
    background-color: var(--greyish);
    margin-right: 15px;
  }

  .circle-right {
    background-color: var(--light-navy);
  }

  /*}*/


</style>
<div class="main" style="background-image: url({BgImage})" id="id-recommendation">
  <h1>Recommendations</h1>
  <Carousel perPage={1} duration={1000}>
      {#each reviewsData as reviewData}
        <div class="slide-content">
          <Slide reviewData={reviewData}/>
        </div>
      {/each}
    <span slot="left-control">
      <div class="circle-left">
        <Icon icon={faArrowLeft}/>
      </div>
    </span>
    <span slot="right-control">
      <div class="circle-right">
        <Icon icon={faArrowRight}/>
      </div>
    </span>

  </Carousel>
</div>