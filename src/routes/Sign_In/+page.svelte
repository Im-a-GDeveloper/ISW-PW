<script>
    import Input from '../Components/Input.svelte'
    import Input_Submit from '../Components/Input_Submit.svelte'

    /**@type {string}*/
    let userEmail = "";
    let userPassword = "";
    let userCheckPassword = "";   


    //Errors
    /**@type {number}*/
    let shortPassword = 0;
    let emailError = 0;

    function validate()
    {
        
        if(userPassword != userCheckPassword)
            shortPassword = 1;
        else
            shortPassword = 0;


        if(!userEmail.includes("@"))
            emailError = 1;
        else 
            emailError
    }
</script>


<section>

    
    <form on:submit|preventDefault={validate}>
        <h2>Create Your Account</h2>


        <input type="email" name="User_email" id="UserEmail" placeholder="Email"  
        bind:value={userEmail}>
        


        <input type="password" name="User_password" id="UserPassword" placeholder="Password" required minlength="6" 
        bind:value={userPassword}>
        {#if shortPassword == 1}
            <p>Both passwords most be the same</p>
        {/if}

        <input type="password" name="User_check_password" id="UserCheckPassword" placeholder="Password" required minlength="6" 
        bind:value={userCheckPassword}>

        {#if shortPassword == 1}
            <p>Both passwords most be the same</p>
        {/if}
        <input class="Submit_input" type="submit" on:submit={() => validate}>

        <p>Already have an account? Log in</p>

        
    </form>
</section>



<style>
    form{
        width: 80%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        color: white;
    }

    form > * {
        margin-bottom: 26px;
    }

    section{
        height: 100vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    input{
        width: 100%;
        height: 56px;
        border-style: none;
        border-radius: 10px;
        background-color: #1E212A;
        color: white;
    }

    .Submit_input{
        background-color: #00B865;
        border-radius: 50px;
        font-size: 20px;
    }
</style>


