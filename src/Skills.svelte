<script>
  import Skill from './Skill.svelte';

  let skills = [
    {
      name: 'Python',
      percent: 95,
    },
    {
      name: 'Javascript',
      percent: 85,
    },
    {
      name: 'Django',
      percent: 95,
    },
    {
      name: 'React.js',
      percent: 90,
    },
    {
      name: 'Redux',
      percent: 90,
    },
    {
      name: 'Svelte',
      percent: 75,
    },
    {
      name: 'AWS',
      percent: 75,
    },
    {
      name: 'Docker',
      percent: 79,
    },
    {
      name: 'REST API',
      percent: 96,
    },
    {
      name: 'Blockchain',
      percent: 75,
    },
  ];
</script>
<style lang="scss">
  $left-shift: 68px;
  $image-width: 300px;
  .main {
    min-height: 777px;
    background-image: url("/images/bg1.jpg");
    background-position: $left-shift;
    background-repeat: no-repeat;
    background-size: calc(100% - 50px);
  }

  h1 {
    margin-left: $left-shift;
    margin-top: 20px;
    font-size: 48px;
    @media (max-width: 768px) {
      margin-left: 20px;
      font-size: 9vw;
    }
    color: var(--light-navy);
    margin-bottom: 0;
  }

  h3 {
    margin-left: $left-shift;
    margin-top: 20px;
    font-size: 30px;
    font-style: italic;
    color: var(--light-navy);
    margin-bottom: 0;
  }

  .skillbox {
    margin-left: $left-shift;
    margin-top: 50px;
    display: flex;
    width: 60%;
    min-width: 600px;
    @media (max-width: 768px) {
      min-width: 0;
      width: 100%;
      margin-left: 20px;
      margin-top: 20px;
    }

    justify-content: space-between;

    .col {
      width: 45%;
    }
  }
  .desktop {
    @media (max-width: 768px) {
      display: none;
    }

  }
  .mobile {
    @media (min-width: 769px) {
      display: none;
    }
    .col {
      width: 85%;
    }

  }
</style>
<div class="main" id="id-skills">
  <h1>Skills</h1>
  <div class="skillbox desktop">
      <div class="col">
          {#each skills.slice(0, 5) as skill}
            <Skill name={skill.name} percent={skill.percent}/>
          {/each}

      </div>
      <div class="col">
          {#each skills.slice(5, 10) as skill}
            <Skill name={skill.name} percent={skill.percent}/>
          {/each}


    </div>

  </div>
  <div class="skillbox mobile">
      <div class="col">
          {#each skills as skill}
            <Skill name={skill.name} percent={skill.percent}/>
          {/each}

      </div>

  </div>
  <h3>...And much more depending on the task</h3>
</div>