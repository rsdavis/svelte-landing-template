
<script>
    import Fa from 'svelte-fa'

    export let icon
    export let title
    export let text
</script>

<div class='card'>
    <div class='icon-circle'>
        <div class="icon">
            <Fa icon={icon} size='2x'/>
        </div>
    </div>
    <h4 class='title'>{ title }</h4>
    <p class='text'>{ text }</p>
</div>

<style>

    .card {
    }

    .icon-circle {
        background-color: var(--blue-light);
        width: 64px;
        height: 64px;
        border-radius: 64px;
        color: white;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .icon {
        width: 32px;
        height: 32px;
        text-align: center;
    }

    .title {
        margin-top: 15px;
        font-size: 26px;
        font-weight: 500;
        color: var(--blue-dark);
    }

    .text {
        margin-top: 15px;
        color: var(--gray-dark);
        font-size: 20px;
        line-height: 1.625;
        text-align: justify;
        font-family: var(--font-sans);
    }
</style>