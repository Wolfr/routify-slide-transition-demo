<script>

    export let icon;

    import iconModule from './TabBarIcons/module.svg';

</script>

<div class="c-tab-bar__icon">
    {#if icon == 'module'}
        {@html iconModule}
    {/if}
</div>