<script>
  import photoMike from '../assets/review_photos/mike.jpeg';
  import photoAlex from '../assets/review_photos/alex_b.jpeg';
  import photoThomas from '../assets/review_photos/thomas.jpeg';
  import BgImage from '../assets/bg1.jpg';
  import Icon from 'fa-svelte';
  import { faArrowLeft } from '@fortawesome/free-solid-svg-icons/faArrowLeft';
  import { faArrowRight } from '@fortawesome/free-solid-svg-icons/faArrowRight';
  import Carousel from '@beyonk/svelte-carousel';
  import Slide from './Recommendations/Slide.svelte';

  const reviewsData = [
    {
      photo: photoMike,
      reviewContent: 'I enjoyed working with Alex in IntelligiChain Inc. He shown his exceptional skills in creating backend part of complex client-server system. Alex not only can implement a server-side components, he gives estimates and advices on the architecture in early stage, he directs and helps in selecting most effective solution both cost and performance wise. Having Alex in the team is a great advantage for your company.',
      author: 'Michael Shishlyaev',
      authorPosition: 'Founder and CEO at IntelligiChain',
      authorLinkedin: 'https://www.linkedin.com/in/michael-shishlyaev-a9b3462/'
    },
    {
      photo: photoAlex,
      reviewContent: 'Anything is possible when it comes to architecting and building complex software solutions with Alexey on your team. I met Alexey @ Revel Systems, when he joined our rapidly growing engineering team as a software engineer. He took on a complex task of expanding our product into a new vertical, building a fuel retail POS. He proved himself as result-oriented professional with can do attitude. He is extremely smart, was able to learn a new domain quickly and implement key components of our product very efficiently. He also has great personality and was a pleasure to work with - I sincerely hope our professional paths will cross again in the future. In the meantime, I strongly recommend Alexey for any challenging software development project as I am confident he is capable to deliver great results as he did for Revel.',
      author: 'Alex Bogachek',
      authorPosition: 'CEO at MERA',
      authorLinkedin: 'https://www.linkedin.com/in/abogachek/'
    },
    {
      photo: photoThomas,
      reviewContent: 'Alex was fantastic to work with, understood a complex product at https://oscer.ai adding features, ideas and clean code from front end to back. Competent in full stack development across react.js, python, Django and more.... would highly recommend for any projects, learns quickly and is easy to communicate with in English and across Slack, Jira etc.',
      author: 'Thomas Kelly',
      authorPosition: 'Surgery Resident at Alfred Health',
      authorLinkedin: 'https://www.linkedin.com/in/thomas-kelly-58b301106/'
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