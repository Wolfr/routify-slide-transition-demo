<script>
    import TabBarItem from './TabBarItem.svelte';
    import { isActive, url } from '@sveltech/routify';
    export let data = {};
</script>

<nav class="c-tab-bar">
    <ul class="c-tab-bar__icons">
        {#each data as [path, name, icon]}
            <TabBarItem {icon} href={$url(path)} active={$isActive(path)}>{name}</TabBarItem>
        {/each}
    </ul>
</nav>

