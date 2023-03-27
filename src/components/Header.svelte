<script lang="ts">
  import logo from '../assets/images/logo.svg'
  import menu from '../assets/images/icon-hamburger.svg'
  import close from '../assets/images/icon-close.svg'
  import arrowLight from '../assets/images/icon-arrow-light.svg'
  import arrowDark from '../assets/images/icon-arrow-dark.svg'

  const handleClickNav = (e: MouseEvent) => {
    const imgStyle = (e.currentTarget as any).childNodes[0].childNodes[0].getAttribute('style');
    const imgStyle2 = (e.currentTarget as any).childNodes[0].childNodes[2].getAttribute('style');
    if (!imgStyle || !imgStyle2) {
        for (let i = 0; i < document.getElementsByClassName('navigation').length; i++) {
            (document.getElementsByClassName('navigation')[i].childNodes[0].childNodes[0] as any).setAttribute('style', '');
            (document.getElementsByClassName('navigation')[i].childNodes[0].childNodes[2] as any).setAttribute('style', '');
            (document.getElementsByClassName('navigation')[i].childNodes[2] as any).setAttribute('style', '');
        }
        (e.currentTarget as any).childNodes[0].childNodes[0].setAttribute('style', 'transform: scale(-1);');
        (e.currentTarget as any).childNodes[0].childNodes[2].setAttribute('style', 'transform: scale(-1);');
        (e.currentTarget as any).childNodes[2].setAttribute('style', 'display: block;');
    } else {
        (e.currentTarget as any).childNodes[0].childNodes[0].setAttribute('style', '');
        (e.currentTarget as any).childNodes[0].childNodes[2].setAttribute('style', '');
        (e.currentTarget as any).childNodes[2].setAttribute('style', '');
    }
  }

  const handleMenu = () => {
    const menuIcon = document.getElementById('menu').getAttribute('style');
    const closeIcon = document.getElementById('close').getAttribute('style');
    if (menuIcon) {
        document.getElementById('menu').setAttribute('style', '');
    } else {
        document.getElementById('menu').setAttribute('style', 'display: none;');
    }

    if (closeIcon) {
        document.getElementById('close').setAttribute('style', '');
    } else {
        document.getElementById('close').setAttribute('style', 'display: block;');
    }
    const displayMenu = document.getElementById('nav').getAttribute('style');
    if (!displayMenu) {
        document.getElementById('nav').setAttribute('style', 'display: block;');
    } else {
        document.getElementById('nav').setAttribute('style', '');
    }
  }

</script>
<header>
    <img id='logo' src={logo} alt='Logo'>
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <img id='menu' src={menu} alt='Menu' on:click={handleMenu}>
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <img id='close' src={close} alt='Close' on:click={handleMenu}>
    <div id='nav'>
        <nav>
            <button id='product' class='navigation' type='button' on:click={handleClickNav}>
                <div class='label'>
                    <img class='arrowLight' src={arrowLight} alt='Arrow'>
                    <img class='arrowDark' src={arrowDark} alt='Arrow'>
                </div>
                <div class='options'>
                    <span>Overview</span>
                    <span>Pricing</span>
                    <span>Marketplace</span>
                    <span>Features</span>
                    <span>Integrations</span>
                </div>
            </button>
            <button id='company' class='navigation' type='button' on:click={handleClickNav}>
                <div class='label'>
                    <img class='arrowLight' src={arrowLight} alt='Arrow'>
                    <img class='arrowDark' src={arrowDark} alt='Arrow'>
                </div>
                <div class='options'>
                    <span>About</span>
                    <span>Team</span>
                    <span>Blog</span>
                    <span>Careers</span>
                </div>
            </button>
            <button id='connect' class='navigation' type='button' on:click={handleClickNav}>
                <div class='label'>
                    <img class='arrowLight' src={arrowLight} alt='Arrow'>
                    <img class='arrowDark' src={arrowDark} alt='Arrow'>
                </div>
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
    #menu, #close {
        display: none;
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
            .navigation .arrowDark {
                display: none;
            }
            .navigation .options span {
                color: var(--very-dark-grayish-blue);
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
            .navigation .label::before {
                color: white;
                font-weight: 600;
            }

            .navigation:hover {
                cursor: pointer;
            }
                .navigation:hover .options {
                    cursor: default;
                }
            .navigation:hover .label::before {
                text-decoration: underline;
            }
        
        #product .label::before {
            content: 'Product';
        }
        #company .label::before {
            content: 'Company';
        }
        #connect .label::before {
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

@media screen and (max-aspect-ratio: 1) {
    header {
        position: fixed;
        z-index: 2;
        top: 0;
        left: 0;
        width: calc(100vw - 2rem);
        justify-content: space-between;
        padding: 1rem;
        align-items: center;
        background-image: linear-gradient(to right, #ff8b70, #ff4457);
    }
    #menu {
        display: block;
    }
    #nav {
        display: none;
        width: calc(100vw - 4rem);
        position: absolute;
        top: calc(100% + 1rem);
        left: 1rem;
        flex-direction: column;
        background-color: white;
        padding: 1rem;
        border-radius: 0.5rem;
    }
        nav {
            flex-direction: column;
            width: 100%;
            border-width: 0;
            border-block-end-width: 0.1rem;
            border-color: #efeff1;
            border-style: solid;
        }
        .navigation {
            margin-left: 0;
            color: var(--very-dark-grayish-blue);
            padding: 1rem 1rem 0 1rem;
        }
        .navigation:last-child {
            margin-block-end: 1rem;
        }
        .navigation .label {
           display: flex;
           align-items: center;
           justify-content: center;
           color: var(--very-dark-grayish-blue);
        }
        .navigation .label::before {
           color: var(--very-dark-grayish-blue);
        }

        .navigation .arrowLight {
            display: none;
        }
        .navigation .arrowDark {
            display: block;
        }
        .navigation .options {
            margin-block-start: 1rem;
            position: static;
            transform: none;
            text-align: center;
            min-width: 0;
            background-color: #efeff1;
        }
        .navigation .options span {
            margin-block-end: 1rem;
            font-weight: 600;
        }

    #authentication {
        display: grid;
        margin-block: 1rem;
    }
        #authentication button {
            width: 50%;
            justify-self: center;
        }
        #authentication button:first-child {
            color: var(--very-dark-grayish-blue);
        }
        #authentication button:last-child {
            color: white;
            background-image: linear-gradient(to right, #ff8b70, #ff4457);
        }
}
</style>
