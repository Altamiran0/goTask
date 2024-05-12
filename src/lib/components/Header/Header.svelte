<script>
    import BoardsMenu from './../BoardsMenu/BoardsMenu.svelte';
</script>


<header>    
    <BoardsMenu />
    <span style="font-weight: 700; font-size: 18px;">goTask_</span>
    <h1 style="font-weight: 500; font-size: 28px;">tablero 1</h1>
</header>

<style>
    header {
        width: 100dvw;
        height: 55px;

        background: var(--White_1);  
        box-shadow: 0 1px 5px 0 var(--ShadowColor);

        display: grid;
        grid-template-columns: 50px 85px 1fr;
        place-items: center;
    }
</style>