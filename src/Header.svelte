<script>
    import Logo from '../assets/logo.svg';
    import Menu from './Header/Menu.svelte';
    import Icon from 'fa-svelte';
    import { faGithub } from '@fortawesome/free-brands-svg-icons/faGithub';
    import { faLinkedin } from '@fortawesome/free-brands-svg-icons/faLinkedin';
</script>

<style lang="scss">
    .header {
        display: flex;
        flex-direction: row;
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
      .icon {
        font-size: 24px;
        color: var(--cool-grey);
        margin-right: 25px;
      }
    }
</style>

<div class="header">
    <div class="logo">
        <img src={Logo} alt=""/>
    </div>
    <Menu/>
    <div class="social-icons">
      <div class="icon">
        <Icon icon={faGithub} />
      </div>
      <div class="icon">
        <Icon icon={faLinkedin} />
      </div>
    </div>
</div>
