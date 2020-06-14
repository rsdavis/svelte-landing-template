
<div class='section-header'>
    <slot name='title'></slot>
    <slot name='text'></slot>
</div>

<style>
    .section-header {
        width: 100%;
        text-align: center;
    }

    .section-header :global(h2) {
        font-size: 44px;
        line-height: 54px;
        font-weight: 900;
    }

    .section-header :global(p) {
        font-size: 20px;
        font-weight: 300;
        line-height: 1.625;
        font-family: var(--font-sans);
    }

    @media (min-width: 640px) {
        .section-header {
            width: 60%;
            margin: 0 auto;
        }
    }

</style>