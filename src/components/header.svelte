<script lang="ts">
	import * as config from '$lib/config';
</script>

<nav class="w-10/12 mx-auto flex items-center justify-between py-2">
	<a href="/">
		<b>{config.title}</b>
	</a>

	<ul class="flex items-center gap-4">
		<li>
			<a href="/posts">Posts</a>
		</li>
		<li>
			<a href="/contact">Contact</a>
		</li>
	</ul>
</nav>
