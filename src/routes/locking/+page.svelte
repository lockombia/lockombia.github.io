<script lang="ts">
    import TournamentShowcase from "$lib/components/TournamentShowcase.svelte";
    import { players, matches, depth } from "$lib/global";

    // Firebase Functions
    import { loadGame, pushGame } from "$lib/global";

    import { onMount } from "svelte";
    onMount(async () => {
        await loadGame("locking");
    });
</script>

<div class="w-full h-full mt-12">
    <div
        class="flex w-[2000px] max-w-[30vw] h-20 mx-auto items-center justify-center mb-6 bg-black/50 shadow-md px-6 py-4 border-0 border-primary-200 rounded"
    >
        <h1>Locking Top 8</h1>
    </div>
</div>

<div
    class="absolute top-1/2 left-1/2 -translate-x-1/2
              w-full"
>
    <TournamentShowcase collectionId={"locking"} />
</div>
