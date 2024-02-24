<script>

    /** @type {string}*/
    export let type;
    /** @type {string}*/
    export let placeholder;
</script>


<input type={type} placeholder={placeholder}>



<style>
    input{
        width: 100%;
        height: 50px;
        border-style: none;
        border-radius: 10px;
        background-color: #1E212A;
        color: white;
        margin-bottom: 20px;
    }

    input::placeholder{
        margin-left: 10px;
    }
</style>