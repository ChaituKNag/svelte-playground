<script>
	import UsersList from './components/UsersList.svelte';
	export let name;
	let imgSrc = `https://picsum.photos/id/1041/536/354`;
</script>

<style>
	h1 {
		color: purple;
	}
</style>

<!-- <h1>Hello {name}!</h1> -->
<!-- <img src={imgSrc} alt="My Image"> -->
<UsersList />
