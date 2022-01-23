<script type="ts">
  import avatar from "../assets/images/avatar-testimonial.jpg";
  import quotes from "../assets/images/icon-quotes.svg";
</script>

<div class="card">
  <img src={quotes} alt="quotes" />
  <p>
    Fylo has improved our team productivity by an order of magnitude. Since
    making the switch our team has become a well-oiled collaboration machine.
  </p>
  <div class="user">
    <img src={avatar} alt="avatar" />
    <div class="info">
      <p class="name">Kyle Burton</p>
      <p class="role">Founder & CEO, Huddie</p>
    </div>
  </div>
</div>

<style>
  .card {
    background: white;
    padding: 1.5rem;
    width: 70%;
    max-width: 24em;
    border-radius: 0.5rem;
    box-shadow: 0px 0px 7px 5px var(--light-gray);
    font-weight: 500;
    font-family: "Open Sans", monospace;
  }

  .card img {
    width: 10%;
    margin: 0;
  }
  .user {
    display: flex;
    align-items: center;
    margin: 0;
  }
  .user img {
    width: 15%;
    border-radius: 50%;
    margin: 0;
  }
  .user .info {
    display: flex;
    flex-direction: column;
    margin: 0 0 0 1rem;
  }
  .user .info * {
    margin: 0;
  }
  .user .info .name {
    font-size: 1.1rem;
    font-family: "Raleway", sans-serif;
    font-weight: 700;
    color: var(--dark-blue);
  }
  .user .info .role {
    font-size: 0.9em;
    font-family: "Open Sans", monospace;
    font-weight: 500;
    color: var(--dark-blue);
  }
</style>
