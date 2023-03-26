<script lang="ts">
  
  import logo from '../assets/images/logo.svg'
  import arrowLight from '../assets/images/icon-arrow-light.svg'

  const handleClickNav = (e: MouseEvent) => {
    const imgStyle = (e.currentTarget as any).childNodes[0].getAttribute('style');
    if (!imgStyle) {
        for (let i = 0; i < document.getElementsByClassName('navigation').length; i++) {
            (document.getElementsByClassName('navigation')[i].childNodes[0] as any).setAttribute('style', '');
            (document.getElementsByClassName('navigation')[i].childNodes[2] as any).setAttribute('style', '');
        }
        (e.currentTarget as any).childNodes[0].setAttribute('style', 'transform: scale(-1);');
        (e.currentTarget as any).childNodes[2].setAttribute('style', 'display: block;');
    } else {
        (e.currentTarget as any).childNodes[0].setAttribute('style', '');
        (e.currentTarget as any).childNodes[2].setAttribute('style', '');
    }
    
  }

</script>
<header>
    <img id='logo' src={logo} alt='Logo'>
    <div id='nav'>
        <nav>
            <button id='product' class='navigation' type='button' on:click={handleClickNav}>
                <img src={arrowLight} alt='Arrow'>
                <div class='options'>
                    <span>Overview</span>
                    <span>Pricing</span>
                    <span>Marketplace</span>
                    <span>Features</span>
                    <span>Integrations</span>
                </div>
            </button>
            <button id='company' class='navigation' type='button' on:click={handleClickNav}>
                <img src={arrowLight} alt='Arrow'>
                <div class='options'>
                    <span>About</span>
                    <span>Team</span>
                    <span>Blog</span>
                    <span>Careers</span>
                </div>
            </button>
            <button id='connect' class='navigation' type='button' on:click={handleClickNav}>
                <img src={arrowLight} alt='Arrow'>
                <div class='options'>
                    <span>Contact</span>
                    <span>Newsletter</span>
                    <span>LinkedIn</span>
                </div>
            </button>
        </nav>
        <div id='authentication'>
            <button type='button'>Login</button>
            <button type='button'>Sign Up</button>
        </div>
    </div>
  
</header>
<style scoped>
  header {
    display: flex;
    width: calc(100% - 16rem);
    padding: 3rem 8rem;
    position: absolute;
    top: 0;
    z-index: 1;
  }
    #logo {
        align-self: center;
    }
    #nav {
        width: 100%;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
        nav {
            display: flex;
        }

        .navigation {
            margin-left: 4rem;
            position: relative;
            background-color: transparent;
            border-width: 0;
            font-size: 1rem;
            padding: 0;
        }
            .navigation .options {
                display: none;
                position: absolute;
                left: 50%;
                top: 100%;
                background-color: white;
                padding: 2rem 1rem;
                border-radius: 0.5rem;
                transform: translate(-50%, 1rem);
                text-align: start;
                min-width: 100%;
            }
            .navigation img {
                margin-left: 0.5rem;
            }
            .navigation .options span {
                color: hsl(207, 13%, 34%);
                font-weight: 300;
                display: block;
                margin-block-end: 0.5rem;
            }
                .navigation .options span:hover {
                    cursor: pointer;
                    font-weight: 600;
                }
                .navigation .options span:last-child {
                    margin-block-end: 0;
                }
            .navigation::before {
                color: white;
                font-weight: 600;
            }

            .navigation:hover {
                cursor: pointer;
            }
                .navigation:hover .options {
                    cursor: default;
                }
            .navigation:hover::before {
                text-decoration: underline;
            }
        
        #product::before {
            content: 'Product';
        }
        #company::before {
            content: 'Company';
        }
        #connect::before {
            content: 'Connect';
        }

    #authentication button {
        font-family: Overpass, sans-serif;
        font-weight: 600;
        padding: 1rem 2rem;
        border-radius: 2rem;
        border-width: 0;
        color: var(--light-red);
        font-size: 1rem;
    }
        #authentication button:hover {
            cursor: pointer;
        }
        #authentication button:first-child {
            color: white;
            background-color: transparent;
        }
        #authentication button:last-child:hover {
            color: white;
            background-color: var(--very-light-red);
        }
@media screen and (min-aspect-ratio: 1) and (max-width: 1024px) {
    header {
        display: flex;
        width: calc(100% - 8rem);
        padding: 3rem 4rem;
    }
}
</style>
