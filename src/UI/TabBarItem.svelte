<script>
    import TabBarIcon from './TabBarIcon.svelte'

    export let href;
    export let icon;
    export let active;

</script>

<style>

    a {
        font-size: 1rem;
        display: block;
        text-align: center;
        height: 4.8rem;
        display: flex;
        align-items: center;
        flex-direction: column;
        justify-content: center;
        opacity: 0.5;
        text-decoration: none;
        color: #212121;
        font-weight: 500;
    }

    .active {
        opacity: 1;
    }

</style>

<li>
    <a {href} class:active={active}>
        <TabBarIcon {icon} />
        <slot></slot>
    </a>
</li>