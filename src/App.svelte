<script lang="ts">
  import { Router, Route, Link } from "svelte-navigator";
  import learnCurrentColor from "./pages/learnCurrentColor.svelte";
  import { MENUS } from "./router";
</script>

<div class="w-screen h-screen flex">
  <Router>
    <div
      class="flex flex-col absolute z-40 left-0 top-0 lg:static lg:left-auto lg:top-auto lg:translate-x-0 h-screen overflow-y-scroll lg:overflow-y-auto no-scrollbar w-64 lg:w-20 lg:sidebar-expanded:!w-64 2xl:!w-64 shrink-0 bg-slate-800 p-4 transition-all duration-200 ease-in-out "
    >
      <div class="">
        {#each MENUS as item}
          <div
            class="cursor-pointer text-white px-3 py-2 bg-gray-100/[0.3] rounded-lg shadow-md"
          >
            <Link class="cursor-pointer" to={item.path}>{item.name}</Link>
          </div>
        {/each}
      </div>
    </div>

    <main class="flex flex-1 bg-white p-1">
      {#each MENUS as item}
        <Route path={item.path}>
          <svelte:component this={item.items} />
        </Route>
      {/each}
    </main>
  </Router>
</div>

<style>
</style>
