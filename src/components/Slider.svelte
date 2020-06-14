

<script>

    import Fa from 'svelte-fa'
    import { faNewspaper, faCopyright, faBook, faBookmark } from '@fortawesome/free-solid-svg-icons'

    let slides = [
        {
            icon: faCopyright,
            label: 'Branding',
            src: 'images/undraw_3.png'
        },
        {
            icon: faNewspaper,
            label: 'Print',
            src: 'images/undraw_2.png'
        },
                {
            icon: faBook,
            label: 'Illustration',
            src: 'images/undraw_1.png'
        },
                        {
            icon: faBookmark,
            label: 'Digital',
            src: 'images/undraw_4.png'
        }
    ]

    let selected = 0;

    const handleClick = (ndx) => {
        selected = ndx
    }

    let fw;
    let fh;

</script>


<div class='slider'>

    <ul class='buttons font-sans'>
        { #each slides as slide, ndx }
            <li>
                <button
                    on:click={handleClick.bind(null, ndx)}
                    class:active={ndx === selected}
                >
                    <div
                        class='circle'
                    >
                        <Fa icon={slide.icon} size='2x'></Fa>
                    </div>

                    <div class='label'>{slide.label}</div>
                </button>

            </li>
        { /each }
    </ul>

    <img src={slides[selected].src} alt='Built exclusively for you'>
</div>

<style>

    .slider {
        margin-top: 40px;
    }

    button {
        background: transparent;
        outline: none;
        border: none;
        opacity: 60%;
    }

    button:hover {
        cursor: pointer;
        opacity: 100%;
    }

    .active {
        opacity: 100%;
    }

    .active.circle {
        border: 1px solid var(--gray-dark);
    }

    .buttons {
        display: grid;
        grid-template-columns: 1fr 1fr;
        justify-content: space-around;
        justify-items: center;
    }

    .circle {
        width: 64px;
        height: 64px;
        border: 1px solid var(--gray-light);
        border-radius: 64px;
        background: transparent;
        color: var(--blue-light);
        display: flex;
        justify-content: center;
        align-items: center;
        margin: 0 auto;
    }

    .label {
        text-align: center;
        font-size: 22px;
        color: var(--gray-dark);
    }

    li {
        text-align: center;
    }

    img {
        height: 300px;
        margin: 30px auto 0 auto;
    }

    @media (min-width: 640px) {
        .buttons {
            grid-template-columns: repeat(auto-fit, 150px);
            justify-content: center;
        }

        img {
            height: 400px;
            display: block;
            margin: 40px auto 0 auto;
        }
    }
</style>