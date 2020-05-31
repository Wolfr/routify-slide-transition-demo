<script>
    export let alt = null;
    export let spacing = null;
    export let flex = null;
</script>

<style>

    .flex {
        display: flex;
    }

    .alt {
        background: #EEE;
    }

    .spacing {
        padding: 1.6rem;
    }

    .c-content-area {
        height: 100%;
    }

</style>

<div class="c-content-area" class:alt={alt} class:spacing={spacing} class:flex={flex}>
    <slot></slot>
</div>