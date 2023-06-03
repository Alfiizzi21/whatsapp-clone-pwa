<div>
    {#each [1,1,1,1,1,1,1,1,1,1] as i}
    <div class="hover:bg-gray-100 flex gap-4 justify-between items-center p-4">
        <img class="rounded-full w-14 " src="./Alhusniyah.png" alt="">
        <article class="w-4/6">
            <h1 class="text-lg truncate">Alfi izzi jalal</h1>
            <p class="text-sm text-gray-500 truncate">Lorem ipsum dolor sit amet consectetur adip...</p>
        </article >
        <div class="flex flex-col items-center gap-1">
            <div  class="text-green-500 text-sm">
                07.26
            </div>
            <div class="text-white bg-green-500 w-5 h-5 rounded-full flex justify-center items-center text-sm">
                2
            </div>
        </div>
    </div>        
    {/each}

</div>
