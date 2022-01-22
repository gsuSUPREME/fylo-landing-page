<script type="ts">
  let email = "";
  const handleSubmit = (e) => {
    e.preventDefault();
    if (valid && email.length > 0) {
      alert("Thank you for subscribing!");
    } else {
      alert("Please enter a valid email address");
    }
  };
  let valid = true;
  const ValidateEmail = (e) => {
    const { value } = e.target;
    valid = value
      .toLowerCase()
      .replace(" ", "")
      .match(
        /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/
      );
  };
</script>

<section>
  <article>
    <h2>Get early access today</h2>
    <p>
      It only takes a minute to sign up and our free starter tier is extremely
      generous. If you have any questions, our support team would be happy to
      help you
    </p>
  </article>
  <aside>
    <form on:submit={handleSubmit} action="post">
      <div class={"input " + (!valid && "error")}>
        <input
          on:input={ValidateEmail}
          bind:value={email}
          type="text"
          placeholder="email@example.com"
        />
        {#if !valid}
          <span>Please check your email</span>
        {/if}
      </div>
      <button>Get Started For Free</button>
    </form>
  </aside>
</section>

<style>
  section {
    display: flex;
    align-items: flex-start;
    padding: 8rem 2rem;
    background-color: var(--desaturated-blue);
    color: white;
  }
  article {
    flex-basis: 50%;
    display: inline-flex;
    flex-direction: column;
    align-items: flex-start;
  }
  article h2 {
    font-size: 2em;
    font-weight: 700;
    font-family: "Raleway", sans-serif;
    margin: 0;
    margin-bottom: 1rem;
  }
  article p {
    font-family: "Open Sans", monospace;
    font-weight: 500;
    font-size: 1em;
    width: 90%;
    max-width: 40rem;
  }
  aside {
    flex-basis: 50%;
    width: 100%;
  }
  aside form {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 1rem;
    width: 100%;
  }
  .input {
    display: inline-flex;
    width: 100%;
    flex-direction: column;
  }
  .input input {
    --desaturated-blue: hsl(238, 22%, 34%);
    box-sizing: border-box;
    width: 80%;
    font-size: 1.2em;
    padding: 0.5rem;
    border-radius: 3px;
    border: 1px solid var(--light-gray);
    box-shadow: 0px 3px 3px 1px var(--desaturated-blue);
  }
  .input.error span {
    margin-top: 0.5rem;
    font-family: "Raleway";
    font-weight: 500;
    font-size: 0.9em;
  }
  .input.error input {
    border: solid 1px var(--light-red);
  }
  form > button {
    --desaturated-blue: hsl(238, 22%, 34%);
    font-size: 0.8em;
    color: white;
    font-family: "Raleway";
    font-weight: 700;
    border-radius: 3px;
    border: none;
    background-color: var(--bright-blue);
    padding: 1rem 2.5rem;
    box-shadow: 0px 3px 3px 1px var(--desaturated-blue);
    transition: all 0.2s ease-in-out;
  }
  form > button:hover {
    cursor: pointer;
    transform: scale(1.05);
  }
  form > button:active {
    background-color: hsl(224, 93%, 78%);
  }

  @media (max-width: 900px) {
    section {
      flex-direction: column;
      align-items: center;
      padding-top: 4rem;
    }
    article {
      flex-basis: 100%;
      text-align: center;
      width: 100%;
      align-items: center;
    }
    article h2 {
      display: inline-block;
      margin-bottom: 2rem;
    }
    aside {
      flex-basis: 100%;
    }
    aside form {
        gap: 0.5rem;
      width: 100%;
    }
    .input input {
      width: 100%;
    }
    form button {
        width: 100%;
    }
    
    form button:hover {
        transform: scale(1);
    }
    
  }
</style>
