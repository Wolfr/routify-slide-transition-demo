<script>
    export let borderPosition = null;
    export let background = null;
</script>

<nav
    class="c-navbar"
    class:c-navbar--bordered-top={ borderPosition == "top" }
    class:c-navbar--bordered-bottom={ borderPosition == "bottom" }
    class:c-navbar--white={ background == "white" }
    class:c-navbar--alt={ background == "alt" }
>
    <slot></slot>
</nav>
