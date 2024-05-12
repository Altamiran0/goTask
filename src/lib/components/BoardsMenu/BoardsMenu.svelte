<script>
	import NewBoard from './NewBoard.svelte';    
	import BoardLink from './BoardLink.svelte';
    import Overlay from './Overlay.svelte';
    import ToggleMenuButton from './ToggleMenuButton.svelte';
    import { slide } from 'svelte/transition';
    import { quintOut } from 'svelte/easing';

    let statusMenu = false;
</script>

<ToggleMenuButton bind:statusMenu/>

{#if statusMenu}
<Overlay />
<nav transition:slide={{ delay: 0, duration: 350, easing: quintOut, axis: 'x' }}>
    <span>
        Tableros
        <div>
            <NewBoard />
            <ToggleMenuButton bind:statusMenu/>
        </div>
    </span>    
    <ul>
        <BoardLink boardName={ 'Tablero 1' } />
        <BoardLink boardName={ 'Tablero 2' } />
        <BoardLink boardName={ 'Tablero 3' } />
        <BoardLink boardName={ 'Tablero 4' } />
        <BoardLink boardName={ 'Tablero 5' } />
    </ul>
</nav>
{/if}

<style>
    nav {
        background: var(--White_1);
        box-shadow: 1px 0 5px 0px var(--ShadowColor);
        width: 100dvw;
        max-width: 350px;
        height: 100dvh;
        position: fixed;
        top: 0; left: 0;
        display: grid;
        row-gap: 5px;
        grid-template-rows: 70px minmax(250px, 1fr);
    }

    span {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 10px;
        font-size: 18px;
        font-weight: 700;
        box-shadow: 0 1px 4px 0 rgba(0,0,0,0.5);
    }

    span div {
        display: grid;
        grid-template-columns: 50px 50px;
    }

    ul {
        padding: 15px 20px;
        overflow: auto;
        display: grid;
        grid-template-rows: repeat(auto-fit, 50px);
        align-items: center;
        gap: 5px;
    }
</style>