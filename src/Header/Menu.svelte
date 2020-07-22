<script>
  let menuItems = ['Summary', 'Skills', 'Recommendations', 'Contacts'];
  let activeMenuItem = 0;
  let scrollInProgress = false;
  import Circles from '../../assets/circles.png';
  import * as animateScroll from 'svelte-scrollto';

  const verticalOffset = 145;

  const getYPosition = elId => {
    return document.getElementById(elId).getBoundingClientRect().y;
  };

  const onLinkClick = (idx) => {
    activeMenuItem = idx;
    let options = {
      offset: -verticalOffset + 1,
      onStart: () => scrollInProgress = true,
      onDone: () => scrollInProgress = false,
    };
    switch (idx) {
      case 0:
        animateScroll.scrollToTop(options);
        break;
      case 1:
        animateScroll.scrollTo({ ...options, element: '#id-skills' });
        break;
      case 2:
        animateScroll.scrollTo({ ...options, element: '#id-recommendation' });
        break;
      case 3:
        animateScroll.scrollTo({ ...options, element: '#id-contacts' });
        break;
      default:
        break;
    }
  };

  const onScroll = (e) => {
    if (scrollInProgress) {
      return;
    }
    const helloPosition = getYPosition('id-hello');
    const recommendationPosition = getYPosition('id-recommendation');
    const skillsPosition = getYPosition('id-skills');
    const contactsPosition = getYPosition('id-contacts');

    if (contactsPosition < verticalOffset) {
      activeMenuItem = 3;
    } else if (recommendationPosition < verticalOffset) {
      activeMenuItem = 2;
    } else if (skillsPosition < verticalOffset) {
      activeMenuItem = 1;
    } else if (helloPosition < verticalOffset) {
      activeMenuItem = 0;
    }
  };
</script>

<style lang="scss">
  .header-menu {
    @media (max-width: 767px) {
      display: none;
    }

    background-repeat: no-repeat;
    background-size: contain;
    background-position: 0 5px;

    @media (min-width: 768px) and (max-width: 991px) {
      font-size: 18px;
    }
    @media (min-width: 992px) and (max-width: 1279px) {
      font-size: 20px;
    }
    @media (min-width: 1280px) {
      font-size: 24px;
    }


    ul {
      display: flex;
      margin-bottom: 0;
      flex-direction: row;
      list-style-type: none;
      padding: 0;

      li {
        cursor: pointer;
        @media (min-width: 768px) and (max-width: 991px) {
          padding: 0 5px;
        }
        @media (min-width: 992px) and (max-width: 1279px) {
          padding: 0 10px;
        }
        @media (min-width: 1280px) {
          padding: 0 25px;
        }

        line-height: 116px;
        color: var(--dark-grey);
        font-weight: bold;

        &::before {
          content: "";
          left: 0;
          display: block;
          position: absolute;
          width: 0;
          height: 0;
          transition: width 1s;
        }

        &.active {
          color: var(--light-navy);
          position: relative;

          &::before {
            content: "";
            left: 0;
            display: block;
            position: absolute;
            width: 100%;
            height: 5px;
            background-color: var(--light-navy);
            transition: width 0.3s;
          }
        }
      }
    }
  }
</style>

<svelte:window on:scroll={onScroll}/>

<div class="header-menu" style="background-image: url({Circles})">
  <ul>
      {#each menuItems as item, idx}
        <li
          class={idx === activeMenuItem ? 'active' : ''}
          on:click={() => onLinkClick(idx)}>
            {item}
        </li>
      {/each}
  </ul>
</div>
