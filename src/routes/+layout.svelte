<script>
    import "../app.css"
    import { fly } from 'svelte/transition';
    let isMoreMenuVisible = false
</script>
<header class="bg-whatsappGreen p-4 text-lg flex items-center justify-between">
    <div id="title" class="text-white">
        WhatsApp
    </div>
    <div class="flex items-center gap-6 text-white">
        <button class="material-symbols-outlined">
            photo_camera
        </button>
        <button class="material-symbols-outlined">
            search
        </button>
        <button on:click={()=> isMoreMenuVisible = true} class="material-symbols-outlined">
            more_vert
        </button>
    </div>
    {#if isMoreMenuVisible}
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <div on:click={()=> isMoreMenuVisible = false} class="bg-black bg-opacity-20 fixed top-0 bottom-0 left-0 right-0">
        <div transition:fly={{ y: -100, x: 100 }} on:click={event => event.stopPropagation()} class="bg-white shadow-lg right-1 text-base top-1 rounded-sm w-1/2 absolute">
            <ul>
                <li>
                    <button class="p-3 hover:bg-gray-100 w-full text-start">
                    New group 
                    </button>
                </li>
                <li>
                    <button class="p-3 hover:bg-gray-100 w-full text-start">
                    New broadcast 
                    </button>
                </li>
                <li>
                    <button class="p-3 hover:bg-gray-100 w-full text-start">
                    Linked devices
                    </button>
                </li>
                <li>
                    <button class="p-3 hover:bg-gray-100 w-full text-start">
                    Starred messages 
                    </button>
                </li>
                <li>
                    <button class="p-3 hover:bg-gray-100 w-full text-start">
                    Settings
                    </button>
                </li>
            </ul>
        </div>        
    </div>
    {/if}

</header>
<svelte:head>
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@48,400,0,0" />
</svelte:head>
<main>
    <slot></slot>
</main>