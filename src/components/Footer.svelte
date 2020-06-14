
<script>
    import Fa from 'svelte-fa'
    import { faFacebook, faTwitter, faInstagram } from '@fortawesome/free-brands-svg-icons'
</script>

<footer>
    <div class='content'>
        <div class='media'>

            <a><Fa icon={faFacebook} size='2x'></Fa></a>
            <a><Fa icon={faTwitter} size='2x'></Fa></a>
            <a><Fa icon={faInstagram} size='2x'></Fa></a>

        </div>

        <div class='links'>
            <a>Contact</a>
            <a>About us</a>
            <a>FAQ's</a>
            <a>Support</a>
        </div>
    </div>
</footer>


<style>
    footer {
        height: 200px;
        background-color: var(--blue-dark);
    }

    .content {
        margin: 0 auto;
        max-width: 1280px;
        display: flex;
        flex-flow: column nowrap;
        justify-content: center;
        height: 100%;
        padding: 0 20px;
    }

    .media {
        display: flex;
        color: white;
        justify-content: flex-end;
        padding: 10px 0 10px 0;
    }

    .media > a {
        margin-left: 20px;
        margin-bottom: 10px;
    }

    a:hover {
        cursor: pointer;
        color: var(--blue-light);
    }

    .links {
        color: white;
        font-family: var(--font-sans);
        font-size: 16px;
        font-weight: 200;
        display: flex;
        justify-content: flex-end;
    }

    .links > a {
        margin-left: 30px;
    }

</style>