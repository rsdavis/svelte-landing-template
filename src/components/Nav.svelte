
<header class='nav'>
    <div class='content'>
        <h1><a href='#'>Landing Template</a></h1>
        <a class='link secondary'>Secondary page</a>
        <a class='link btn'>Sign up</a>
    </div>
</header>

<style>
    .nav {
        background-color: var(--blue-dark);
        color: white;
    }

    .content {
        padding: 0 20px 0 20px;
        margin: 0 auto 0 auto;
        max-width: 1280px;
        display: flex;
        align-items: center;
        height: 80px;
    }

    h1 {
        font-size: 32px;
        flex-grow: 1;
    }

    h1 > a {
        color: white;
        text-decoration: none;
    }

    .link {
        margin-left: 50px;
        font-family: var(--font-sans);
        font-weight: 300;
    }

    .link:hover {
        cursor: pointer;
    }

    .secondary:hover {
        color: var(--blue-light);
    }

    .btn {
        background-color: var(--blue-light);
        border-radius: 3px;
        padding: 10px 30px;
    }

    .btn:hover {
        filter: brightness(120%);
    }
</style>