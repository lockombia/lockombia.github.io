<script lang="ts">
    let stream_link = "https://www.youtube.com/embed/czsot21OvxA add";
    let highligth_links = [
        "https://www.youtube.com/embed/djV11Xbc914",
        "https://www.youtube.com/embed/FTQbiNvZqaY",
        "https://www.youtube.com/embed/XfR9iY5y94s",
    ];
</script>

<div class="w-full mt-12">
    <div class="w-full h-full mt-12">
        <div
            class="flex w-[2000px] max-w-[30vw] h-20 mx-auto items-center justify-center mb-6 bg-black/50 shadow-md px-6 py-4 border-0 border-primary-200 rounded"
        >
            <h1>Transmisión en Vivo</h1>
        </div>
    </div>
    <div class="w-full flex justify-center">
        <iframe
            class="w-full max-w-[700px] aspect-video"
            src={stream_link}
            title="YouTube video player"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen
        ></iframe>
    </div>
</div>

<div class="w-full mt-12">
    <div
        class="flex w-[2000px] max-w-[30vw] h-20 mx-auto items-center justify-center mb-6 bg-black/50 shadow-md px-6 py-4 border-0 border-primary-200 rounded"
    >
        <h1>Highlights</h1>
    </div>
    <div class="grid grid-cols-1 sm:grid-cols-2 gap-6 w-full px-4">
        {#each highligth_links as link}
            <div class="w-full aspect-video">
                <iframe
                    class="w-full h-full"
                    src={link}
                    title="YouTube video player"
                    frameborder="0"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                    allowfullscreen
                ></iframe>
            </div>
        {/each}
    </div>
</div>
