<script lang="ts">
    import heroImg from '../assets/images/bg-pattern-intro-desktop.svg'
    import editorDesktop from '../assets/images/illustration-editor-desktop.svg'

    import phone from '../assets/images/illustration-phones.svg'
</script>
<main>
    <section id='hero'>
        <img src={heroImg} alt='Intro'>
        <div>
            <h1>A modern publishing platform</h1>
            <p>Grow your audience and build your online brand</p>
            <button type="button">Start for Free</button>
            <button type="button">Learn more</button>
        </div>
    </section>
    <section id='design'>
        <h1>Designed for the future</h1>
        <div class='paragraph'>
            <article>
                <div>
                    <h2>Introducing an extensible editor</h2>
                    <p>
                        Blogr features an exceedingly intuitive interface which lets you focus on one thing: creating content. 
                        The editor supports management of multiple blogs and allows easy manipulation of embeds such as images, 
                        videos, and Markdown. Extensibility with plugins and themes provide easy ways to add functionality or 
                        change the looks of a blog.
                    </p>
                </div>
                <div>
                    <h2>Robust content management</h2>
                    <p>
                        Flexible content management enables users to easily move through posts. Increase the usability of your blog 
                        by adding customized categories, sections, format, or flow. With this functionality, you're in full control.
                    </p>
                </div>
            </article>
            <div class='backgroundImg'>
                <img src={editorDesktop} alt='Editor'>
            </div>
        </div>
    </section>
    <section id='art'>
        <div>
            <img src={phone} alt='Phone'>
        </div>
        <article>
            <h1>State of the Art Infrastructure</h1>
            <p>
                With reliability and speed in mind, worldwide data centers provide the backbone for ultra-fast connectivity. 
                This ensures your site will load instantly, no matter where your readers are, keeping your site competitive.
            </p>
        </article>
    </section>
    <section id='reason'>
        <article>
            <div>
                <h2>Free, open, simple</h2>
                <p>
                    Blogr is a free and open source application backed by a large community of helpful developers. It supports 
                    features such as code syntax highlighting, RSS feeds, social media integration, third-party commenting tools, 
                    and works seamlessly with Google Analytics. The architecture is clean and is relatively easy to learn.
                </p>
            </div>
            <div>
                <h2>Powerful tooling</h2>
                <p>
                    Batteries included. We built a simple and straightforward CLI tool that makes customization and deployment a breeze, but
                    capable of producing even the most complicated sites.
                </p>
            </div>
        </article>
    </section>
</main>
<style scoped>
    #hero {
        display: flex;
        justify-content: center;
        align-items: center;
        position: relative;
        background-image: linear-gradient(to right, #ff8b70, #ff4457);
        height: 100vh;
        overflow: hidden;
        border-radius: 0 0 0 10rem;
    }
        #hero img {
            position: absolute;
            top: 50%;
            left: 0;
            transform: translate(0, -50%);
            z-index: 0;
            max-width: 150%;
        }

        #hero div {
            position: relative;
            z-index: 1;
            text-align: center;
            color: white;
        }
            #hero div h1 {
                font-size: clamp(2rem, 4vw, 4rem);
            }
            #hero div button {
                font-family: Ubuntu, sans-serif;
                font-weight: 600;
                padding: 1rem 2rem;
                border-style: solid;
                border-color: white;
                border-radius: 2rem;
                border-width: 0.1rem;
                color: var(--light-red);
                font-size: 1rem;
            }
                #hero div button:last-child {
                    background-color: transparent;
                    color: white;
                }
            #hero div button:hover {
                cursor: pointer;
            }
    #design {
        position: relative;
    }
        #design h1 {
            color: var(--very-dark-blue);
            position: absolute;
            top: 0rem;
            left: 50%;
            transform: translate(-50%);
            text-align: center;
            font-size: clamp(2rem, 3vw, 3rem);
        }

    .paragraph {
        margin-block-start: 8rem;
        display: grid;
        grid-template-columns: 50% 50%;
    }
        .paragraph article {
            padding: 15%;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }
            .paragraph article h2 {
                color: var(--very-dark-blue);
                font-size: clamp(1.5rem, 2vw, 2rem);
            }
            .paragraph article p {
                color: var(--very-dark-grayish-blue);
                line-height: 2rem;
            }

        .backgroundImg {
            position: relative;
        }
            .backgroundImg img {
                width: 130%;
                transform: translate(3%);
            }

    #art {
        display: grid;
        justify-content: center;
        grid-template-columns: 50% 50%;
        color: white;
        background-image: linear-gradient(to right, hsl(237, 17%, 21%), hsl(237, 23%, 32%));
        border-radius: 0 8rem 0 2rem;
        margin-block: 5rem;
    }
        #art article {
            padding: 15% 15% 15% 0;
        }
            #art article h1 {
                margin-block-start: 0;
                font-size: clamp(2rem, 3vw, 3rem);
            }
            #art article p {
                line-height: 2rem;
                margin-block-end: 0;
            }
        #art div{
            overflow: visible;
            position: relative;
        }
            #art div img {
                position: absolute;
                top: 50%;
                left: 50%;
                transform: translate(-50%, -50%);
            }

@media screen and (max-aspect-ratio: 1) {
    #hero {
        background-image: linear-gradient(135deg, #ff8b70, #ff4457);
    }
    #hero img {
        left: 50%;
        transform: translate(-45%, -45%);
        max-width: 400%;
    }
}
</style>
