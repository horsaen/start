<script>
    // declare search engines
    const ddg = 'https://duckduckgo.com/'
    const google = 'https://www.google.com/search?q='
    const qwant = 'https://www.qwant.com/?q='
    const startpage = 'https://www.startpage.com/sp/search?query='
    let query = undefined
    const handleSubmit = (e) => {
        query = e.target.name.value
        window.location = google + query
    }
</script>

<div>
    <form class="searchbar" on:submit={handleSubmit}>
        <!-- since this is a startpage it's worth using the autofocus for ease-of-use :D -->
        <!-- svelte-ignore a11y-autofocus -->
        <input autofocus id="name" placeholder="hi" autocomplete="off" />
        <button type="submit">hi</button>
    </form>
</div>

<style>
    .searchbar {
        position: absolute;
        bottom: 10px;
        left: 10px;
    }
    .searchbar input {
        all: unset;
    }
</style>