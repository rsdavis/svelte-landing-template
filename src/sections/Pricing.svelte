
<script>
    import Section from '../components/Section.svelte'
    import SectionHeader from '../components/SectionHeader.svelte'

    let tiers = [
        {
            price: 25,
            nfeatures: 3
        },
        {
            price: 99,
            nfeatures: 4
        },
        {
            price: 499,
            nfeatures: 5
        }
    ]
</script>

<Section bgColor='#101D2D'>

    <SectionHeader>
        <h2 class='title' slot='title'>Simple, transparent pricing</h2>
        <p class='text' slot='text'>Vitae aliquet nec ullamcorper sit amet risus nullam eget felis semper quis lectus nulla at volutpat diam ut venenatis tellus in ornare.</p>
    </SectionHeader>

    <div class='cards'>
        { #each tiers as tier }
            <div class='card'>
                <div class='price'>
                    <span>${tier.price}</span>
                    <span style='font-size: 18px'>/m</span>
                </div>
                <p class='tier'>Premium, perfect for you</p>
                <p style='font-weight: bold; font-size: 18px; margin-top: 20px;'>Whats included ...</p>

                <ul>
                    <li class='feature'>
                        <span class='check'></span>
                        <span class='feature-text'>Excepteur sint occaecat velit</span>
                    </li>
                    <li class='feature'>
                        <span class='check'></span>
                        <span class='feature-text'>Excepteur sint occaecat velit</span>
                    </li>
                    <li class='feature'>
                        <span class='check'></span>
                        <span class='feature-text'>Excepteur sint occaecat velit</span>
                    </li>
                    <li class='feature'>
                        <span class="{tier.nfeatures > 3 ? 'check' : 'nocheck'}"></span>
                        <span class='feature-text'>Excepteur sint occaecat velit</span>
                    </li>
                    <li class='feature'>
                        <span class="{tier.nfeatures > 4 ? 'check' : 'nocheck'}"></span>
                        <span class='feature-text'>Excepteur sint occaecat velit</span>
                    </li>
                </ul>

                <button>Start free trial</button>

            </div>
        { /each }
    </div>

</Section>

<style>

    .title {
        color: white;
    }

    .text {
        color: var(--gray-light);
    }

    .cards {
        margin-top: 40px;
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
    }

    .card {
        background: white;
        flex-basis: 100%;
        padding: 25px;
        font-family: var(--font-sans);
        margin: 20px;
    }

    .price {
        font-size: 36px;
        color: var(--blue-dark);
        font-weight: 600;
    }

    .tier {
        color: var(--gray-light);
        font-size: 22px;
        font-family: var(--font-sans);
        font-weight: 300;
        margin-top: 20px;
    }

    ul {
        margin-top: 20px;
    }

    .feature {
        border-bottom: 1px solid rgb(220,220,220);
        line-height: 52px;
        color: var(--gray-light);
        font-size: 18px;
        font-weight: 300;
    }

    .feature:first-child {
        border-top: 1px solid rgb(220,220,220);
    }

    .check {
        display: inline-block;
        vertical-align: middle;
        width: 24px;
        height: 24px;
        background-image: url("data:image/svg+xml;charset=US-ASCII,%3Csvg%20width%3D%2224%22%20height%3D%2224%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%3E%3Cg%20fill-rule%3D%22nonzero%22%20fill%3D%22none%22%3E%3Ccircle%20fill%3D%22%232BBF96%22%20cx%3D%2212%22%20cy%3D%2212%22%20r%3D%2212%22%2F%3E%3Cpath%20fill%3D%22%23fff%22%20d%3D%22M10.5%2012.267l-2.5-1.6-1%201.066L10.5%2016%2017%209.067%2016%208z%22%2F%3E%3C%2Fg%3E%3C%2Fsvg%3E")
    }

    .nocheck {
        display: inline-block;
        width: 24px;
        height: 24px;
    }

    .feature-text {
        padding-left: 10px;
        font-size: 14px;
    }

    button {
        background: var(--blue-light);
        color: white;
        border: none;
        outline: none;
        border-radius: 3px;
        padding: 10px 20px;
        width: 100%;
        margin-top: 20px;
    }

    button:hover {
        cursor: pointer;
        filter: brightness(120%);
    }

    @media (min-width: 640px) {
        .card {
            min-width: 370px;
            flex-basis: 370px;
        }

        .feature-text {
            font-size: 18px;
        }
    }

    @media (min-width: 1280px) {
        .cards {
            justify-content: space-between;
            margin: 40px 0 0 0;
        }

        .card {
            margin: 0;
        }
    }
</style>