<script>
    import IconMenu2 from '@tabler/icons-svelte/IconMenu2.svelte';
</script>

<header>    
    <IconMenu2 stroke={1.5}/>
    <span>goTask_</span>
    <h1>tablero 1</h1>
</header>

<style>
    header {
        width: 100dvw;
        height: 55px;

        background: #ebecee;  
        box-shadow: 0px 1px 5px 0px rgba(0,0,0,0.5);
        color: rgb(32, 31, 31); 

        display: grid;
        grid-template-columns: 50px 85px 1fr;
        place-items: center;
    }
</style>