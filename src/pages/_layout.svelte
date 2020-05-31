<script>
  
  import NavBar from '../UI/NavBar.svelte';
  import TabBar from '../UI/TabBar.svelte';

  import { writable } from 'svelte/store';
  import Transition from "../components/Transition.svelte"
  const width = writable();

  const mainTabs = [
    ['/module1', 'Module 1', 'module'],
    ['/module2', 'Module 2', 'module'],
    ['/module3', 'Module 3', 'module']
    ];
  
</script>

<style>

  .flex-wrapper {
    height: 100%;
    display: flex;
    flex-direction: column;
  }
  
  .relative-wrapper {
    height: 100%;
    display: flex;
    flex-direction: column;
  }
  
</style>

<div class="flex-wrapper">
  <div bind:offsetWidth={$width} class="relative-wrapper">
    <slot decorator={Transition} scoped={{ width }} />
  </div>
  <NavBar borderPosition="top" background="alt">
      <TabBar data="{mainTabs}" />
  </NavBar>
</div>



