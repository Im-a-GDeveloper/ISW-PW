<script>
    /**@type {String}*/
    let userEmail;
    /**@type {String}*/
    let userPassword;
    /**@type {String}*/
    let checkPassword;


    //Errors
    /**@type {Boolean}*/
    let errorMessage;
    /**@type {String}*/
    let emailError = "";
    function validate()
    {
        if(!userEmail.includes("@"))
        {
            errorMessage = true;
            emailError = "Please enter a valid email";
        } 
        else if(userEmail.length == 0) {
            errorMessage = true;
            emailError = "This field can't be empty";
        }
        else
        {
            errorMessage = false
            emailError = ""
        } 


    }
</script>


<div class="main">

    <form on:submit|preventDefault={validate} method="POST">
        <h2>Sign In</h2>

        <input type="text" placeholder="Email" bind:value={userEmail} >
            <!-- {#if errorMessage == true}
                <p class="error">{emailError}</p>
            {/if} -->
        <p class="error">{emailError}</p>

        <input id="pass" type="password" placeholder="Password" bind:value={userPassword} >
        <input type="password" placeholder="Repeat Your Password" bind:value={checkPassword} />
        
        
        

        <input class="submit" type="submit" value="Sign In">
        <p class="Link">Already have an account? <a href="/Pages/Login/">Log In</a></p>
    </form>
</div>


<style>

    .main{
        height: 100vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    .main form{
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 30px;
    }

    input{
        width: 90%;
        height: 60px;
        border-radius: 10px;
        border-style: none;
        background-color: #F3F3F3;

        &::placeholder{
            font-size: 16px;
        }
    }

    .submit{
        background-color: #00B865;
        border-radius: 50px;
        font-size: 20px;
        color: white;
    }

    a{
        color: #00B865;
    }

    .Link{
        font-size: 18px;
    }

    .error{
        
        color: red;
        padding: 0;
    }
</style>


