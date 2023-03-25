<script lang="ts">
    import heroImg from '../assets/images/bg-pattern-intro-desktop.svg'
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
  

  Designed for the future

  Introducing an extensible editor
  Blogr features an exceedingly intuitive interface which lets you focus on one thing: creating content. 
  The editor supports management of multiple blogs and allows easy manipulation of embeds such as images, 
  videos, and Markdown. Extensibility with plugins and themes provide easy ways to add functionality or 
  change the looks of a blog.

  Robust content management
  Flexible content management enables users to easily move through posts. Increase the usability of your blog 
  by adding customized categories, sections, format, or flow. With this functionality, you’re in full control.

  State of the Art Infrastructure
  With reliability and speed in mind, worldwide data centers provide the backbone for ultra-fast connectivity. 
  This ensures your site will load instantly, no matter where your readers are, keeping your site competitive.

  Free, open, simple
  Blogr is a free and open source application backed by a large community of helpful developers. It supports 
  features such as code syntax highlighting, RSS feeds, social media integration, third-party commenting tools, 
  and works seamlessly with Google Analytics. The architecture is clean and is relatively easy to learn.

  Powerful tooling
  Batteries included. We built a simple and straightforward CLI tool that makes customization and deployment a breeze, but
  capable of producing even the most complicated sites.
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
    }
        #hero img {
            position: absolute;
            top: 50%;
            left: 0;
            transform: translate(-10%, -50%);
            z-index: 0;
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
</style>