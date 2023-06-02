<script>
    import "../app.css"
</script>
<header class="bg-whatsappGreen text-white p-4 text-lg flex items-center justify-between">
    WhatsApp
    <div class="flex items-center gap-6">
        <span class="material-symbols-outlined">
            photo_camera
        </span>
        <span class="material-symbols-outlined">
            search
        </span>
        <span class="material-symbols-outlined font-bold">
            more_vert
        </span>
    </div>
</header>
<svelte:head>
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@48,400,0,0" />
</svelte:head>
<main>
    <slot></slot>
</main>