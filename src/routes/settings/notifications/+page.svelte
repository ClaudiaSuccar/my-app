<script lang="ts">
	import type { PageProps } from './$types';
    import { Sample } from '$lib';
	let { data }: PageProps = $props();
</script>

<h1>Settings/{data.sections[1].title}</h1>
<Sample/>