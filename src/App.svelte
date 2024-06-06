<script>
    import { Router, Link, Route } from "svelte-routing"

        
    import Home     from "./routes/Home.svelte"
    import Docs     from "./routes/Docs.svelte"
    import About    from "./routes/About.svelte"
    import License  from "./routes/License.svelte"
    import Releases from "./routes/Releases.svelte"
    import NotFound from "./routes/NotFound.svelte"


    export let url = ""
</script>



<Router {url}>
    <nav>
        <Link to="/">
            <img src="/svg/logo-text.svg" alt="Logo" class="logo-text" />
        </Link>

        <Link to="/docs"    >Docs</Link>
        <Link to="/releases">Releases</Link>
        <Link to="/about"   >About</Link>
    </nav>


    <main>
        <Route path="/"         component={Home}     />
        <Route path="/docs"     component={Docs}     />
        <Route path="/about"    component={About}    />
        <Route path="/license"  component={License}  />
        <Route path="/releases" component={Releases} />
        <Route path="*"         component={NotFound} />
    </main>



    <footer>
        <a>Support</a>
        <a>Privacy</a>
        <a>Terms of Use</a>
        <a>License</a>

    </footer>
</Router>



<style>
    nav {
        padding: 10px;
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 20px;
        background: linear-gradient(55deg, #050130 0%, #0c0561 100%);
    }

    :global(nav > a) {
        color: white;
        font-weight: 600;
        transition: 0.2s;
    }

    :global(nav > a:hover) {
        color: gray;
        transition: 0.2s;
    }


    main {
        padding: 10px;
    }


    .logo-text {
        width: 150px;
    }

</style>