<script>
    let users = fetchUsers();
    
    async function fetchUsers() {
        const res = await fetch(`https://jsonplaceholder.typicode.com/users`);
        const u = await res.json();

        if(u) {
            console.log(u);
            return u;
        } else {
            throw new Error();
        }
    }
</script>

{#await users}
<p>Loading...</p>
{:then usersList}
<ul>
    {#each usersList as user}
        <li>{user.name}</li>
    {/each}
</ul>
{:catch}
<p>An error occurred!</p>
{/await}