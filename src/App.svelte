<script>
    import PageContent from './lib/pageContent.svelte'

    let pageNumber = 0
</script>

{#if !pageNumber}
    <main id="page-0">
    <PageContent bind:pageNumber/>
    </main>
{:else}
    <main id="page-1">
        <PageContent bind:pageNumber/>
    </main>
{/if}
