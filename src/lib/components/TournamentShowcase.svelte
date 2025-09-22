<script lang="ts">
    import * as utils from "$lib/tournamentUtils.js";
    import { SvelteFlow, Controls, Panel, Background } from "@xyflow/svelte";
    import MatchNode from "./MatchNode.svelte";
    import "@xyflow/svelte/dist/style.css";
    import { Item } from "$lib/types/Item";
    import { players, matches, depth } from "$lib/global";

    $depth = 0;

    const nodeTypes = { matchNode: MatchNode };

    let nodes = $derived(utils.nodesGenerator($depth, $matches));

    let edges = $derived(utils.edgesGenerator($depth, $matches));

    import { onMount, tick } from "svelte";
    import { loadGame } from "$lib/global";

    let svelteflow: any;

    async function clickFitViewButton() {
        await tick();
        requestAnimationFrame(() => {
            // look for button inside the SvelteFlow element first, then globally
            const btn =
                svelteflow?.querySelector?.(".svelte-flow__controls-fitview") ??
                document.querySelector(".svelte-flow__controls-fitview");

            if (btn instanceof HTMLElement) {
                btn.click();
                return;
            }
        });
    }

    onMount(() => {
        (async () => {
            await loadGame();
            await clickFitViewButton();
        })();

        const load_interval = setInterval(async () => {
            await loadGame();
        }, 5000);
        const fitview_interval = setInterval(async () => {
            await clickFitViewButton();
        }, 2000);

        return () => {
            clearInterval(load_interval);
            clearInterval(fitview_interval);
        };
    });

    $inspect($matches);
</script>

<div>
    {svelteflow?.width?.()}
</div>

<div style="width: 100%; height: 40vh">
    <SvelteFlow
        bind:this={svelteflow}
        bind:nodes
        bind:edges
        {nodeTypes}
        proOptions={{ hideAttribution: true }}
        fitView
    >
        <Controls />
    </SvelteFlow>
</div>

<style>
    :global(.svelte-flow) {
        background: transparent !important;
    }
    :global(.svelte-flow__controls) {
    display: none !important;
  }
</style>
