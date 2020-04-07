<script>
  export let name;
  export let percent
</script>
<style lang="scss">
  .skill {
    margin-bottom: 20px;

    .name {
      display: flex;
      width: 100%;
      justify-content: space-between;

      .percent {
        font-size: 24px;
        color: var(--text-color-2);
        font-weight: bold;
        line-height: 28px;
      }

      .skillname {
        font-size: 20px;
        color: var(--dark-grey);
        font-weight: bold;
        line-height: 28px;
      }
    }
    .greyline {
      width: 100%;
      height: 12px;
      background-color: var(--line-grey);
      border-radius: 20px;
    }
    .line {
      margin-top: -12px;
      height: 12px;
      background-color: var(--line-blue);
      border-radius: 20px;
    }
  }


</style>

<div class="skill">
  <div class="name">
    <div class="skillname">{name}</div>
    <div class="percent">{percent}%</div>
  </div>
  <div class="greyline"/>
  <div class="line" style="width: {percent}%"/>
</div>