<script>
  import illustration from "../../assets/images/illustration-2.svg";
  import curveDesktop from "../../assets/images/bg-curve-desktop.svg";
  import curveMobile from "../../assets/images/bg-curve-mobile.svg";
  import arrow from "../../assets/images/icon-arrow.svg";
  import avatar from "../../assets/images/avatar-testimonial.jpg";
  import quotes from "../../assets/images/icon-quotes.svg";

    let bgimage = window.screen.width <= 900 ? curveMobile : curveDesktop;
    window.addEventListener("resize", () => {
      if (window.screen.width <= 900) {
        bgimage = curveMobile;
      } else {
        bgimage = curveDesktop;
      }
    });
</script>

<img src={bgimage} class="arc" alt="arc" />
<article>
  <div class="article">
    <div class="content">
      <h2 class="article-title">Stay productive, wherever you are</h2>
      <p class="p p-1">
        Never let location be an issue when accessing your files. Fylo has you
        covered for all your file storage needs.
      </p>
      <p class="p p-2">
        Securely share files and folders with friends, family and colleagues for
        live collaboration. No email attachments required!
      </p>
      <!-- svelte-ignore a11y-invalid-attribute -->
      <a href="#"
        >See how Fylo works <span><img src={arrow} alt="arrow" /></span></a
      >
    </div>
    <div class="card">
        <img src={quotes} alt="quotes">
      <p>
        Fylo has improved our team productivity by an order of magnitude. Since
        making the switch our team has become a well-oiled collaboration
        machine.
      </p>
      <div class="user">
        <img src={avatar} alt="avatar">
        <div class="info">
            <p class="name">Kyle Burton</p>
            <p class="role">Founder & CEO, Huddie</p>
        </div>
      </div>
    </div>
  </div>
  <div class="illustration">
    <img src={illustration} alt="illustration" />
  </div>
</article>

<style>
    :root {
        scroll-behavior: smooth;
    }
  .arc {
    width: 100%;
    height: auto;
    margin: 12rem 0 0 0;
    display: flex;
  }
  article {
    background: var(--light-blue);
    padding: 3rem 0 5rem 0;
    display: flex;
    align-items: center;
  }
  .article {
    margin: 0 0 0 1.9rem;
    display: flex;
    flex-basis: 60%;
    flex-direction: column;
    align-items: flex-start;
    gap: 1.5rem;
  }
  .article .content h2 {
    font-size: 2rem;
    font-family: "Raleway", sans-serif;
    font-weight: 700;
    margin: 0;
    color: var(--dark-blue);
    margin-bottom: 1.5rem;
  }
  .article .content > p {
    font-size: 0.9rem;
    width: 70%;
    font-family: "Open Sans", monospace;
    font-weight: 500;
    color: var(--desaturated-blue);
  }
  .article .content > a {
    font-size: 1.2em;
    font-family: "Open Sans", monospace;
    text-decoration: none;
    color: var(--moderated-cyan);
  }
  .article .content a > span > img {
    display: flex;
    width: 80%;
    margin: 0 0 0 0.2rem;
  }
  .article .content > a {
    display: flex;
    width: max-content;
    border-bottom: 1px solid var(--moderated-cyan);
    align-items: center;
  }
  .illustration img {
    width: 90%;
    margin: 0;
  }
  .illustration {
    flex-basis: 40%;
    margin: 0;
    display: flex;
    align-items: center;
    justify-content: center;
  }
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

  .card img{
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
    .user .info *{
        margin: 0;
    }
    .user .info .name {
        font-size: 1.1rem;
        font-family: "Raleway", sans-serif;
        font-weight: 700;
        color: var(--dark-blue);
    }
    .user .info .role{
        font-size: 0.9em;
        font-family: "Open Sans", monospace;
        font-weight: 500;
        color: var(--dark-blue);
    }
    @media screen and (max-width: 900px) {
        .arc {
            margin-top: 5rem;
        }
        .article {
            align-items: center;
            flex-basis: auto;
            margin: 0 1.5rem 0 1.5rem;
        }
        .article .content {
            align-items: center;
            justify-content: center;
            margin-top: 3rem;
            text-align: center;
        }
        .article .content > p {
            text-align: start;
            width: 100%;
        }
        .article .content > h2 {
            text-align: center;
            font-size: 2em;
        }
        .article .content > a {
            margin: 1rem 0 2rem 0;
            display: inline-flex;
            font-size: 1em;
        }
        article {
            justify-content: center;
            align-items: center;
            flex-direction: column-reverse;
        }
    }




</style>
