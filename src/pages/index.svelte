<script>

    let pageTitle = "List";

    let dataset = [
      {
          "image": "[]",
          "name":"a",
      },
      {
          "image": "[]",
          "name":"b",
      },
      {
          "image": "[]",
          "name":"c",
      },
      {
          "image": "[]",
          "name":"d",
      },
    ];


    import { url } from '@sveltech/routify';

    import NavBar from '../UI/NavBar.svelte';
    import ContentArea from '../UI/ContentArea.svelte';

    import Toolbar from '../UI/Toolbar.svelte';
    import ToolbarGroup from '../UI/ToolbarGroup.svelte';
    import ToolbarItem from '../UI/ToolbarItem.svelte';
    import ToolbarTitle from '../UI/ToolbarTitle.svelte';

</script>

<svelte:head>
    <title>{pageTitle} - Slide transition demo</title>
</svelte:head>

<NavBar borderPosition="bottom"  background="alt">
    <Toolbar>
        <ToolbarGroup align="center">
            <ToolbarItem>
                <ToolbarTitle>{pageTitle}</ToolbarTitle>
            </ToolbarItem>
        </ToolbarGroup>
    </Toolbar>
</NavBar>

<ContentArea>
    <ul class="c-item-grid">
        {#each dataset as item }
            {#if item.item == ""}
                <li class="c-item-grid__item">
                </li>
                {:else}
                <li class="c-item-grid__item">
                    <a href="/detail">
                        {item.image}
                        <br>
                        {item.name}
                    </a>
                </li>
            {/if}
        {/each}
    </ul>
</ContentArea>