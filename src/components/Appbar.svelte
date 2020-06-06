<script>
    export let title;
    export let routes;
</script>

<div class="appbar">
    <h1>{title}</h1>
    <nav>
        {#each routes as route}
            <a href={route.link}>{route.label}</a>
        {/each}
    </nav>
</div>

<style>
    .appbar {
        border: 2px solid black;
        text-align: center;
        padding-bottom: 15px;
        font-size: 20px;
        margin: 10px;
    }

    a {
        text-decoration: none;
        color: black;
        padding: 10px;
        transition: font-size ease-in 300ms;
    }

    a:hover {
        border: 2px solid black;
        font-size: 25px;
    }

    a:active {
        font-size: 23px;
    }
</style>