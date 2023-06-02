<script>
	import { onMount } from 'svelte';
    import { page } from '$app/stores';
        
	let path = "";
	let host = '';

    $: {
        path = $page.url.href.split('/')[3];
    }  


	onMount(() => {
		host = window.location.protocol + '//' + window.location.host;
	});
</script>

<nav class="bg-whatsappGreen">
	<ul class="flex">
		<li>
			<a href="{host}/groups">
				<button
					class:active={path == 'groups'}
					class="hover:bg-opacity-10 hover:bg-white hover:text-white ho p-2 py-2 text-gray-300"
				>
					<span class="material-symbols-outlined"> groups </span>
				</button>
			</a>
		</li>
		<li class="flex-grow">
			<a href="{host}">
				<button
					class:active={path == "" || path == 'chats'}
					class="text-sm h-full w-full hover:bg-opacity-10 hover:bg-white hover:text-white p-2 py-2 text-gray-300"
				>
					Chats
				</button>
			</a>
		</li>
		<li class="flex-grow">
			<a href="{host}/status">
				<button
					class:active={path == 'status'}
					class="text-sm h-full w-full hover:bg-opacity-10 hover:bg-white hover:text-white p-2 py-2 text-gray-300"
				>
					Status
				</button>
			</a>
		</li>

		<li class="flex-grow">
			<a href="{host}/calls">
				<button
					class:active={path == 'calls'}
					class="text-sm h-full w-full hover:bg-opacity-10 hover:bg-white hover:text-white p-2 py-2 text-gray-300"
				>
					Calls
				</button>
			</a>
		</li>
	</ul>
</nav>
{host}

<style>
	.material-symbols-outlined {
		font-variation-settings: 'FILL' 1, 'wght' 400, 'GRAD' 0, 'opsz' 48;
	}
	.active {
		border-bottom: 3px white solid;
	}
</style>
