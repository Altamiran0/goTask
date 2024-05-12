<script lang="ts">
    import IconMenu2 from '@tabler/icons-svelte/IconMenu2.svelte';
    import IconX from '@tabler/icons-svelte/IconX.svelte';

    export let statusMenu: boolean;
    const ChangeState = () => statusMenu = !statusMenu;
</script>

{#if statusMenu}
<button style="display: flex" on:click={ ChangeState }> 
    <IconX stroke={1.5} size={32}/>
</button>
{:else}
<button style="display: flex" on:click={ ChangeState }>
    <IconMenu2 stroke={1.5}/>
</button>
{/if}
