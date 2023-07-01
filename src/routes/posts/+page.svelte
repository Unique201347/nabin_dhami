<script lang="ts">
	import { formatDate } from '$lib/utils';
	import * as config from '$lib/config';
	import type { Post } from '$lib/types';

	export let data: { posts: Post[] };
</script>

<svelte:head>
	<title>{config.title}</title>
</svelte:head>

<!-- Posts -->
<section>
	<div class="grid grid-cols-4 gap-10 w-10/12 mx-auto">
		{#each data.posts as post}
			<article class="bg-gray-400">
				<a href={`posts/${post.slug}`} class="title">{post.title}</a>
				<p class="date">{formatDate(post.date)}</p>
				<p class="description">{post.description}</p>
			</article>
		{/each}
	</div>
</section>
