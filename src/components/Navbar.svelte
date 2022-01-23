<script lang="ts">
    import logo from "../assets/images/logo.svg";
</script>


<nav class="navbar">
    <img src={logo} alt="logo" />
    <ul class="nav-items">
        <!-- svelte-ignore a11y-invalid-attribute -->
        <li class="nav-item"><a href="#">Features</a></li>
        <!-- svelte-ignore a11y-invalid-attribute -->
        <li class="nav-item"><a href="#">Team</a></li>
        <!-- svelte-ignore a11y-invalid-attribute -->
        <li class="nav-item"><a href="#">Sign in</a></li>
    </ul>
</nav>

<style>
    :root {
        --gray: hsl(0, 0%, 75%);
    }
    .navbar img {
        width: 14%;
        max-width: 8rem;
    }
    .navbar {
        padding: 1rem 1.9rem;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    .nav-items {
        display: flex;
        align-items: center;
        list-style-type: none;
        gap: 1.5rem;
    }

    .nav-item a{
        font-family: "Raleway", sans-serif;
        color: var(--gray);
        font-weight: 700;
        text-decoration: none;
        transition: all 0.3s ease-in-out;
    }

    .nav-item a:hover {
        color: hsl(0, 0%, 60%);
        text-decoration: underline;
    }
    @media (max-width: 900px) {
        .navbar {
            padding: 0.7rem;
        }
        
        .navbar img {
            width: 22%;
            max-width: 7em;
        }
    }
    @media (max-width: 450px) {
        .nav-item a {
            font-size: 0.8em;
        }
        .nav-items {
        padding: 0;
        }
        .navbar img {
            width: 19%;
        }
    }


</style>
