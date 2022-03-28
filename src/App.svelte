<script>
	import { Router, Route, Link } from "svelte-routing";
	import AddImage from "./AddImage.svelte";
	import Login from "./Login.svelte";
</script>

<div class="tot">
	<Router>
		<header class="navegacio">
			<a href="/">
				<img src="./PiStory.png" width="256px" height="100px" alt="Logo" class="logo">
			</a>

			<nav>
				<Link to="addImage">Add Image</Link>
				<Link to="login">Login</Link>
			</nav>
		</header>
		<main class="nose">
			<Route path="addImage"><AddImage/></Route>
			<Route path="login"><Login/></Route>
		</main>
	</Router>
</div>

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
	.logo{
		padding-right: 1300px;
	}
	.nose{
		margin-block-start: 150px;
        left: 0;
		padding: 0px;
	}
</style>