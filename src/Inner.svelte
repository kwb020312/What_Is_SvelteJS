<script>
    import {createEventDispatcher} from 'svelte'

    const dispatch = createEventDispatcher();

    function Hello() {
        dispatch('msg',{
            text:'Hello There!!!'
        })
    }
</script>

<main>
    <button on:click={Hello}>Say Hello!!</button>
</main>