<script>
    import Icon from './Icon.svelte';

    // layouts: icon-only, label-icon, icon-label, icon-label-icon, icon-label-narrow-icon
    export let layout = "label";

    export let icon = null;
    export let icon2 = null;

</script>

{#if layout == "icon-only"}
    <span class="c-button__icon-only-wrap"><Icon {icon} /></span>
    <span class="u-d-sr-only"><slot></slot></span>
{:else if layout == "icon-label-icon"}
    <Icon {icon} />
    <span class="c-button__label"><slot></slot></span>
    <Icon icon={icon2} />
{:else if icon}
    <Icon {icon} />
    <span class="c-button__label"><slot></slot></span>
{:else}
    <span class="c-button__label"><slot></slot></span>
{/if}
