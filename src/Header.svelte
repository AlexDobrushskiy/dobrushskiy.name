<script>
  import Logo from '../assets/logo.svg';
  import Menu from './Header/Menu.svelte';
  import Icon from 'fa-svelte';
  import { faGithub } from '@fortawesome/free-brands-svg-icons/faGithub';
  import { faLinkedin } from '@fortawesome/free-brands-svg-icons/faLinkedin';
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

  .social-icons {
    margin: 19px 0 0 50px;
    line-height: 116px;
    display: flex;

    a {
      font-size: 24px;
      color: var(--cool-grey);
      margin-right: 25px;
      text-decoration: none;
    }
  }
</style>

<div class="header">
  <div class="logo">
    <img src={Logo} alt=""/>
  </div>
  <Menu/>
  <div class="social-icons">
    <a href="https://github.com/AlexDobrushskiy">
      <Icon icon={faGithub}/>
    </a>
    <a href="https://www.linkedin.com/in/alex-dobrushskiy/">
      <Icon icon={faLinkedin}/>
    </a>
    <a href="https://www.toptal.com/resume/alex-dobrushskiy">Toptal</a>
  </div>
</div>
