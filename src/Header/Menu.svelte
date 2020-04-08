<script>
  let menuItems = ['Summary', 'Recommendations', 'Skills', 'Contacts'];
  let activeMenuItem = 0;
  const onClick = e => {
    console.log('Taksa');
  };
  import Circles from '../../assets/circles.png';
  import * as animateScroll from "svelte-scrollto";
  const verticalOffset = 145;

  const getYPosition = elId => {
    return document.getElementById(elId).getBoundingClientRect().y;
  };

  const onLinkClick = (idx) => {
    console.log('taksa');
    activeMenuItem = idx;
    switch (idx) {
      case 0:
        animateScroll.scrollToTop();
        break;
      case 1:
        animateScroll.scrollTo({element: '#id-recommendation', offset: -verticalOffset});
        break;
      case 2:
        animateScroll.scrollTo({element: '#id-skills', offset: -verticalOffset});
        break;
      default:
        break;
    }
  };

  const onScroll = (e) => {
    const position = window.scrollY;
    const recommendationPosition = getYPosition('id-recommendation');
    const skillsPosition = getYPosition('id-skills');
    if (position < recommendationPosition+600) {
      activeMenuItem = 0;
    } else if (position >= recommendationPosition && position < skillsPosition+600) {
      activeMenuItem = 1;
    } else if (position >= skillsPosition) {
      activeMenuItem = 2;
    }

  }
</script>

<style lang="scss">
  .header-menu {
    background-repeat: no-repeat;
    background-size: contain;
    background-position: 0 5px;
    ul {
      display: flex;
      margin-bottom: 0;
      flex-direction: row;
      list-style-type: none;

      li {
        cursor: pointer;
        padding: 0 25px;
        line-height: 116px;
        font-size: 24px;
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
