<script>
  import Logo from "../assets/logo.svg";
  import Menu from "./Header/Menu.svelte";
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
</style>

<div class="header">
  <div class="logo">
    <img src={Logo} alt="" />
  </div>
  <Menu/>
</div>
