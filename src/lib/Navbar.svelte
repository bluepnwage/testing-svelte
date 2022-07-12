<script>
  import { onMount } from "svelte";
  onMount(() => {
    const interval = setInterval(() => {
      time = new Date().toLocaleTimeString();
    }, 1000);
    return () => clearInterval(interval);
  });
  let time = new Date().toLocaleTimeString();
  const navItems = ["Home", "About", "Contact"];
  let loggedIn = false;
  const userName = "bluepnwage";

  const toggleAuth = () => {
    loggedIn = loggedIn ? false : true;
  };
  $: message = loggedIn ? "Sign out" : "Log in";
</script>

<header class="flex justify-center h-16 border-bottom border sticky top-0 left-0 bg-white items-center">
  <nav class="w-3/5 flex justify-between items-center">
    <div class="flex gap-10">
      {#each navItems as link}
        <a href="!#" class="cursor-pointer text-gray-900 font-semibold hover:text-gray-600">{link}</a>
      {/each}
      <span class="text-gray-900 font-semibold">{time}</span>
    </div>
    <div class="flex gap-5 items-center">
      {#if loggedIn}
        <p>Welcome {userName}</p>
      {:else}
        <p>You are not signed in</p>
      {/if}
      <button on:click={toggleAuth} class="bg-gray-900 font-bold text-gray-100 px-4 py-2 rounded-lg">{message}</button>
    </div>
  </nav>
</header>
