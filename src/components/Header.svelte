<script lang="ts">
  import logo from '../assets/images/logo.svg'
</script>
<header>
    <img src={logo} alt='Logo'>
    <div id='nav'>
        <nav>
            <select title="product" id='product'>
                <option selected hidden>Product</option>
                <option>Overview</option>
                <option>Pricing</option>
                <option>Marketplace</option>
                <option>Features</option>
                <option>Integrations</option>
            </select>
            <select title="company" id='company'>
                <option selected hidden>Company</option>
                <option>About</option>
                <option>Team</option>
                <option>Blog</option>
                <option>Careers</option>
            </select>
            <select title="connect" id='connect'>
                <option selected hidden>Connect</option>
                <option>Contact</option>
                <option>Newsletter</option>
                <option>LinkedIn</option>
            </select>
        </nav>
        <div>
            <button type='button'>Login</button>
            <button type='button'>Sign Up</button>
        </div>
    </div>
  
</header>
<style scoped>
  header {
    display: flex;
    width: calc(100% - 8rem);
    padding: 3rem 4rem;
    position: absolute;
    top: 0;
    z-index: 1;
  }
    #nav {
        margin-left: 1rem;
        width: 100%;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    #nav select {
        background-color: transparent;
        border-width: 0;
    }
    #nav select:hover {
        cursor: pointer;
    }
    #nav select:focus-visible {
        outline: none;
    }

</style>