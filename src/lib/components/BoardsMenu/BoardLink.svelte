<script lang="ts">
    export let boardName: String;
    let boardName_url = boardName.replaceAll(' ', '_');
</script>

<li><a href="/boards/{ boardName_url }">{ boardName }</a></li>

<style>
    li {
        width: 100%;
        height: 50px;
        border-radius: 5px;
        font-size: 14px;

        display: flex;
        align-items: center;
        justify-self: center;
        padding: 0 10px;
        font-weight: 500;
        text-overflow: ellipsis;
    }

    li:hover {
        background: rgba(0, 0, 0, 0.02);
    }

    a {
        width: 100%;
        height: 100%;
        display: flex;
        align-items: center;
        color: var(--Black_1);
    }
</style>