<script lang="ts">
	import { AppBar } from "@skeletonlabs/skeleton";
  import menuItems from "../../config/menuItems";
</script>

<!-- App Bar -->
<AppBar>
  <svelte:fragment slot="lead">
    <a href="/">
      <strong class="text-xl uppercase">RSD</strong>
    </a>
  </svelte:fragment>
  <svelte:fragment slot="trail">
    {#each menuItems as item}
      <a
        class="btn btn-sm variant-ghost-surface"
        href={item.path}
        rel="noreferrer"
      >
        {item.title}
      </a>
    {/each}
  </svelte:fragment>
</AppBar>