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
      @media (min-width: 992px) and (max-width: 1279px) {
        margin-right: 20px;
      }
      @media (min-width: 769px) and (max-width: 991px) {
        margin-right: 10px;
      }

      text-decoration: none;
    }

    .tt {
      font-size: 24px;
      padding-bottom: 2px;

      svg {
        margin-bottom: -3px;
        fill: currentColor;
        width: 20px;
      }
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
  <a href="https://www.toptal.com/resume/alex-dobrushskiy#unite-only-masterly-engineers" class="tt">
    <svg viewBox="0 0 21 30">
      <path
        d="M8.185 0l6.763 6.838.076.073.077.076L21 12.95l-9.595 9.65 4.396 4.445L12.859 30l-6.72-6.794-.117-.115-.123-.122L0 17.007 9.562 7.39 5.205 2.989 8.185 0zm4.034 10.715a.54.54 0 00-.246.152l-.07.069-5.462 5.498c-.159.154-.197.226-.225.314a.437.437 0 000 .265c.019.073.052.14.151.249l.068.07 1.733 1.754c.153.16.224.199.312.227a.427.427 0 00.262 0c.069-.019.133-.053.245-.153l.072-.068 5.462-5.498c.159-.155.197-.226.224-.315a.437.437 0 000-.264.547.547 0 00-.15-.249l-.068-.071-1.733-1.754c-.154-.16-.225-.198-.312-.226a.427.427 0 00-.263 0zM19.414.017c.383 0 .711.137.985.413.273.276.41.607.41.993 0 .391-.137.717-.41.987a1.331 1.331 0 01-.985.408 1.31 1.31 0 01-.978-.408 1.325 1.325 0 01-.405-.987c0-.386.131-.717.405-.993.273-.276.601-.413.978-.413zm.006.226c-.323 0-.596.115-.82.347a1.137 1.137 0 00-.34.833c0 .325.11.606.334.833.225.226.498.341.826.341.323 0 .596-.115.82-.341.224-.232.339-.508.339-.833 0-.326-.115-.607-.339-.833a1.098 1.098 0 00-.82-.347zm.093.413c.306 0 .486.182.486.436 0 .215-.158.375-.371.419l.377.678h-.257l-.372-.667h-.251v.667h-.23V.656h.618zm-.033.199l-.355.005v.464h.355c.197 0 .295-.078.295-.232 0-.16-.098-.237-.295-.237z"
        fill-rule="evenodd"></path>
    </svg>
  </a>
</div>
