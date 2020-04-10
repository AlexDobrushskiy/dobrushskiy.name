<script>
  import Icon from 'fa-svelte';
  import { faGithub } from '@fortawesome/free-brands-svg-icons/faGithub';
  import { faLinkedin } from '@fortawesome/free-brands-svg-icons/faLinkedin';
</script>

<style lang="scss">
  .social-icons {
    display: flex;
    align-items: flex-end;
    a {
      font-size: 24px;
      color: var(--cool-grey);
      margin-right: 25px;
      text-decoration: none;
    }
    .tt {
      font-size: 28px;
      padding-bottom: 2px;
    }
  }

</style>

<div class="social-icons">
  <a href="https://github.com/AlexDobrushskiy">
    <Icon icon={faGithub}/>
  </a>
  <a href="https://www.linkedin.com/in/alex-dobrushskiy/">
    <Icon icon={faLinkedin}/>
  </a>
  <a href="https://www.toptal.com/resume/alex-dobrushskiy" class="tt">TT</a>
</div>
