<script>
  let menuItems = ['Summary', 'Skills', 'Recommendations', 'Contacts'];
  let activeMenuItem = 0;
  const onClick = e => {
    console.log('Taksa');
  };
  import Circles from '../../assets/circles.png';
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

<div class="header-menu" style="background-image: url({Circles})">
  <ul>
      {#each menuItems as item, idx}
        <li
          class={idx === activeMenuItem ? 'active' : ''}
          on:click={() => (activeMenuItem = idx)}>
            {item}
        </li>
      {/each}
  </ul>
</div>
