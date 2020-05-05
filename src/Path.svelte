<script>
    import DropCard from './cards/DropCard.svelte';
    import ActionCard from './cards/ActionCard.svelte';
    let path = [];
    export let setup = true;
</script>

<div class="flex">
    {#if setup}
    <DropCard />
    {/if}

    <ActionCard/>
    <!-- {#each path as actionCard}
        <ActionCard data={actionCard}/>
    {/each} -->
    {#if setup}
    <DropCard />
    {/if}
</div>
