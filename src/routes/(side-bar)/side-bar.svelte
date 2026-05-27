<script lang="ts">
	import Button from '$lib/components/ui/button/button.svelte';
	import Menu from '@lucide/svelte/icons/menu';
	import X from '@lucide/svelte/icons/x';

	let open = $state(false);
</script>

<section>
	<Button
		variant="outline"
		onclick={() => {
			open = !open;
		}}
		>{#if open === false}
			<Menu />
		{:else}
			<X />
		{/if}</Button
	>
</section>
