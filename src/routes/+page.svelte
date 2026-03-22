<script lang="ts">
  import { goto } from '$app/navigation';
  import { base } from '$app/paths';
  import { buildRedirectUrl } from '$lib/util/redirect';
  import { onMount } from 'svelte';

  onMount(async () => {
    await goto(base + buildRedirectUrl(window.location), {
      replaceState: true
    });
  });
</script>
