<script>
  import Header from './Header.svelte';
  import Hello from './Hello.svelte';
  import Recommendation from './Recommendation.svelte';
  import Skills from './Skills.svelte';
  import Contacts from './Contacts.svelte';
</script>


<style>
  .content {
    padding-top: 140px;
    scroll-behavior: smooth;
  }
</style>

<Header/>
<div class="content">
  <Hello/>
  <Recommendation/>
  <Skills/>
  <Contacts/>
</div>