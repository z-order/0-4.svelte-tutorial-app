<script>
	import Info from './12.Info.svelte';

	const pkg = {
		name: 'svelte',
		version: 3,
		speed: 'blazing',
		website: 'https://svelte.dev'
	};
</script>

<!-- Use this -->
<Info {...pkg}/>

<!-- Instead of using below
<Info name={pkg.name} version={pkg.version} speed={pkg.speed} website={pkg.website}/>
-->