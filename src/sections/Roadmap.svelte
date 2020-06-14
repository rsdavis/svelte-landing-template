
<script>
    import Section from '../components/Section.svelte'
    import SectionHeader from '../components/SectionHeader.svelte'
</script>

<Section bgColor='white'>

    <SectionHeader>
        <h2 class='title' slot='title'>Product roadmap</h2>
        <p class='text' slot='text'>Vitae aliquet nec ullamcorper sit amet risus nullam eget felis semper quis lectus nulla at volutpat diam ut venenatis tellus in ornare.</p>
    </SectionHeader>


    <div class='roadmap'>

        <div class='border'></div>

        <div class='box item1'>
            <p class='date'>November 2019</p>
            <p class='text'>Deployed a high-quality first release and conducted a market validation test</p>
        </div>

        <div class='box item2 flip'>
            <p class='date'>December 2019</p>
            <p class='text'>Deployed a high-quality first release and conducted a market validation test</p>
        </div>

        <div class='border'></div>
        <div class='border'></div>

        <div class='box item3'>
            <p class='date'>January 2020</p>
            <p class='text'>Deployed a high-quality first release and conducted a market validation test</p>
        </div>

        <div class='box item4 flip'>
            <p class='date'>February 2020</p>
            <p class='text'>Deployed a high-quality first release and conducted a market validation test</p>
        </div>

        <div class='border'></div>
        <div class='border'></div>

        <div class='box item5'>
            <p class='date'>March 2020</p>
            <p class='text'>Deployed a high-quality first release and conducted a market validation test</p>
        </div>


    </div>

</Section>

<style>

    .title {
        color: var(--gray-dark);
    }

    .text {
        color: var(--gray-light);
    }

    .roadmap {
        margin-top: 50px;
    }

    .box {
        font-family: var(--font-sans);
        padding: 10px 20px;
        border-left: 2px solid rgb(220,220,220);
    }

    .date {
        font-size: 18px;
        color: var(--gray-light);
        font-weight: 300;
    }

    .box > .text {
        font-weight: 600;
        color: var(--blue-dark);
        font-size: 22px;
    }

    @media (min-width: 640px) {

        .border {
            height: 100%;
        }

        .roadmap {
            display: grid;
            grid-template-columns: 1fr 1fr;
        }


        .roadmap > div:nth-child(even) {
            border-left: 2px solid rgb(210,210,210);
            border-right: 0;
        }

        .roadmap > div:nth-child(odd) {
            border-left: 0;
            text-align: right;
        }

    }
</style>