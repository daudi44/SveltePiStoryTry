<script>
    import { Router, Route, Link } from "svelte-routing";
    import AddImage from './AddImage.svelte';

    export const navItems = [
        {
            id: 0,
            label: "Add Image",
            href: "addimage",
            component: ""
        },
        {
            id: 1,
            label: "Login", 
            href: "login",
            component: '<Login/>'
        }
    ];
</script>

<Router>
    <div>
        <ul class="navegacio">
            <li>
                <a href="/">
                    <img src="./PiStory.png" alt="" class="logo" width="256" height="100">
                </a>
            </li>
            {#each navItems as item}
                <li class="links">
                    <Link to="{item.href}">{item.label}</Link>
                </li>     

                <div>
                    <Route path="{item.href}"><AddImage/></Route>
                </div>
            {/each}
        </ul>        
    </div>
</Router>

<style>
    .navegacio {
        background-color: black;
        list-style-type: none; 
        position: fixed;
        top: 0;
        left: 0;
        right: 0;
        display: flex;
        align-items: center;
        margin-block-start: 0;
        padding-top: 5px;
        padding-bottom: 5px;
    }
    
</style>