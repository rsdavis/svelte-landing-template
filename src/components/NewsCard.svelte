
<script>
    export let title = 'Title'
    export let text = 'Text'
    export let imgSrc;
    export let className = 'hello'
</script>

<article class={className}>

    <img src={imgSrc} alt="Article cover">
    <h3 class="mx">{ title }</h3>
    <p class="mx">{ text }</p>
    <button class="mx">Read more</button>

</article>

<style>

    article {
        background: white;
        font-family: var(--font-sans);
        margin: 12px;
        --px: 20px;
        --py: 10px;
        display: flex;
        flex-direction: column;
        align-items: start;
        padding-bottom: 20px;
    }

    img {
        max-width: 100%;
        height: 200px;
        object-fit: contain;
        margin: 0 auto 0 auto;
    }

    h3 {
        margin-top: 20px;
        color: var(--blue-dark);
        font-size: 26px;
        font-weight: 600;
    }

    p {
        margin-top: 20px;
        flex-grow: 1;
        color: var(--gray-light);
        font-size: 18px;
        line-height: 1.5;
        font-weight: 300;
    }

    button {
        background: transparent;
        border: none;
        outline: none;
        padding: 0;
        display: block;
        margin-top: 20px;
    }

    button:hover {
        cursor: pointer;
        color: var(--blue-light);
    }

    .mx {
        margin-left: 20px;
        margin-right: 20px;
    }
</style>