<script>
    export let icon;

    // Possible icon types
    import IconChevronLeft from './Icons/chevron-left.svg';
    import IconChevronRight from './Icons/chevron-right.svg';
    import IconSoundOn from './Icons/sound-on.svg';
    import IconSoundOff from './Icons/sound-off.svg';

</script>

<style>
    .svg-icon :global(svg) {
        width: 1.6rem;
        height: 1.6rem;
    }
</style>

<div class="svg-icon">
    {#if icon == 'chevron-left'}
        {@html IconChevronLeft}
    {/if}
    {#if icon == 'chevron-right'}
        {@html IconChevronRight}
    {/if}
    {#if icon == 'sound-on'}
        {@html IconSoundOn}
    {/if}
    {#if icon == 'sound-off'}
        {@html IconSoundOff}
    {/if}
</div>