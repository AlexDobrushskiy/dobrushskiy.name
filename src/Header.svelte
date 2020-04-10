<script>
  import Logo from '../assets/logo.svg';
  import Menu from './Header/Menu.svelte';
  import Social from './Header/Social.svelte';
</script>

<style lang="scss">
  .header {
    position: fixed;
    top: 0;
    width: 100%;
    display: flex;
    flex-direction: row;
    background: var(--white);
    z-index: 3;
  }

  .logo {
    margin: 19px 0 0 46px;

    img {
      height: 116px;
    }
  }
  .social {
    margin-top: 40px;
    margin-left: 50px;
  }
</style>

<div class="header">
  <div class="logo">
    <img src={Logo} alt=""/>
  </div>
  <Menu/>
  <div class="social">
      <Social/>
  </div>
</div>
