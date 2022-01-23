<script type="ts">
    import Illustration from "../assets/images/illustration-1.svg";
    let email = "";
    let valid = true;
    const ValidateEmail = (e) => {
        const {value} = e.target;
        valid = value.toLowerCase().replace(" ", "").match(
      /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/
    );
    }
    function handleClick():void {
       if(valid && email.length > 0) {
           alert("Thank you for subscribing!");
       } else {
            alert("Please enter a valid email address");
       }
    }

</script>
<main>
<div class="content">
    <h1>All your files in one secure location, accessible anywhere.</h1>
    <p>Fylo stores your most important files in one secure location. Access them wherever you need, share and collaborate with friends, family, and co-workers.</p>
    <div id="form" class={!valid ? "error": ""}>
        <div class="input">
            <input type="text" bind:value={email} on:input={ValidateEmail} placeholder="Enter your email" />
            {#if !valid}
        <p>Please check your email</p>
        {/if}
        </div>
        <button on:click={handleClick}>Get Started</button>
    </div>
</div>
    <div class="img-container">
        <img src={Illustration} alt="illustration">
    </div>
</main>

<style>
    :root {
        --light-gray: hsl(240, 93%, 89%);
        --light-blue: hsl(240, 75%, 98%);
        --desaturated-blue:  hsl(238, 22%, 44%);
        --bright-blue: hsl(224, 93%, 58%);
        --dark-blue: hsl(243, 87%, 12%);
        --light-red: hsl(0, 97%, 77%);
        --moderated-cyan: hsl(170, 45%, 43%);
    }
    main {
        display: flex;
        margin: 1.9rem 1.2rem 1.5rem 1.9rem;
        justify-content: space-evenly;
        align-items: center;
    }
    .content {
        flex-basis: 50%;
        font-family: "Raleway", sans-serif;
    }
    .img-container {
        display: flex;
        flex-basis: 50%;
        align-items: center;
        justify-content: center;
    }
    .content > p {
        font-family: "Open Sans", sans-serif;
        font-weight: 500;
        max-width: 44rem;
        font-size: 1em;
        color: var(--dark-blue);
    }
    .content > h1 {
        font-size: 1.9em;
        color: var(--dark-blue)
    }
    #form {
        display: flex;
        align-items: flex-start;
    }
    #form > .input >input {
        font-size: 1.2em;
        padding: 0.5rem;
        border-radius: 2px;
        border: solid 1px var(--dark-blue);
    }
    #form > .input >p {
        font-size: 1em;
        margin: 0.5rem 0;
        color: var(--light-red);
    }

    #form.error > .input > input {
        border: solid 1px var(--light-red);
    }
    #form > button {
        font-size: 0.8em;
        color: white;
        font-family: "Raleway";
        font-weight: 700;
        border-radius: 3px;
        border: none;
        margin-left: 0.7rem;
        background-color: var(--bright-blue);
        padding: 0.8rem 2.5rem 0.8rem 2.5rem;
        box-shadow: 2px 2px 5px var(--light-gray);
        transition: background-color 0.2s ease-in-out;
    }
    #form > button:active {
        background-color: hsl(224, 93%, 78%);
    }
    .img-container > img {
        width: 70%;
    }

    @media (max-width: 900px) {
        main {
            flex-direction: column-reverse;
            gap: 1rem;
        }
        .content {
            flex-basis: 100%;
            text-align: center;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .img-container {
            flex-basis: 100%;
        }
        .content > h1 {
            font-size: 1.8em;
            margin-bottom: 0.3rem;
        }
        #form {
            flex-direction: column;
            gap: 0.8rem;
           align-items: center;
            width: 80%;
        }
        #form >.input > p{
            text-align: center;
        }
        #form > .input {
            width: 100%;
        }
        #form > .input > input {
            width: 94%;
            margin-left: 0;
        }
        #form > button {
            margin-left: 0;
            width: 100%;
        }
    }
    
    
</style>