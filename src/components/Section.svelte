
<script>
    export let bgColor = 'white'
    export let borderTop = false
</script>

<section style='background: {bgColor}'>
    <div class="{borderTop ? 'border-top' : ''}">
        <slot/>
    </div>
</section>


<style>

    section > div {
        padding-top: 80px;
        padding-bottom: 80px;
        max-width: 1280px;
        padding-left: 20px;
        padding-right: 20px;
        margin-left: auto;
        margin-right: auto;
    }

    .border-top {
        border-top: 1px solid rgb(220,220,220);
    }
</style>