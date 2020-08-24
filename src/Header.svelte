<script>

  import Menu from './Header/Menu.svelte';
  import Social from './Header/Social.svelte';

  let Logo = 'images/logo.svg';
</script>

<style lang="scss">
  .header {
    position: fixed;
    top: 0;
    width: 100vw;
    display: flex;
    flex-direction: row;
    background: var(--white);
    z-index: 3;
  }

  .logo {
    margin: 19px 0 0 46px;
    @media (max-width: 991px) {
      margin-left: 0;
    }
    @media (min-width: 992px) and (max-width: 1279px) {
      margin-left: 20px;
    }

    img {
      height: 116px;
      @media (min-width: 769px) and (max-width: 991px) {
        width: 250px;
      }
      @media  (max-width: 768px) {
        width: 60vw;
      }
    }
  }
  .social {
    margin-top: 40px;
    @media (min-width: 992px) and (max-width: 1279px) {
      margin-left: 25px;
    }
    @media (max-width: 991px) {
      margin-left: 10px;
    }
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
