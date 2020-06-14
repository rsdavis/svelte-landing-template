<script>
    import Section from '../components/Section.svelte'
</script>


<Section bgColor='#101D2D'>

    <div class='split'>

        <div class='cta'>

            <h1>
                Landing template for startups
            </h1>

            <p class='text-gray-light text-md font-sans font-normal leading-loose'>
                Our landing page template works on all devices,
                so you only have to set it up once, and get beautiful results forever.
            </p>

            <button class='btn bg-blue-light font-sans'>
                Pricing and plans
            </button>

            <button class='btn bg-gray-dark font-sans'>
                Learn more
            </button>

        </div>

        <img src='images/undraw_hero.png' alt='People chatting'/>

    </div>

</Section>


<style>

    h1 {
        color: white;
        font-size: 44px;
        font-weight: 600;
    }

    p {
        font-family: var(--font-sans);
    }

    .btn {
        outline: none;
        border: none;
        display: block;
        width: 100%;
        max-width: 280px;
        margin: 20px auto 0 auto;
        padding: 15px 0;
        border-radius: 3px;
        color: white;
    }

    .btn:hover {
        cursor: pointer;
        filter: brightness(120%);
    }

    img {
        width: 100%;
        margin-top: 40px;
    }

    .cta {
        text-align: center;
    }

    @media (min-width: 640px) {

        .split {
            display: grid;
            grid-template-columns: minmax(400px, 2fr) minmax(400px, 1fr);
            grid-gap: 5%;
            overflow: hidden;
        }

        .cta {
            margin: auto 0 auto 0;
            text-align: left;
        }

        img {
            display: block;
            margin: auto 0 auto auto;
            overflow: hidden;
            max-width: 400px;
            border-radius: 5px;
        }

        h1 {
            font-size: 52px;
        }

        p {
            margin-top: 20px;
        }

        .btn {
            display: inline-block;
            margin: 20px 10px 0 0;
            max-width: 200px;
        }

    }
</style>