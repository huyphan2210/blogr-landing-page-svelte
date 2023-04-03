<script lang="ts">
  import logo from '../assets/images/logo.svg'
</script>
<footer>
  <img src={logo} alt='Logo'>
  <div class='navigation-footer'>
    <h3>Product</h3>
    <div>
      <span>Overview</span>
      <span>Pricing</span>
      <span>Marketplace</span>
      <span>Features</span>
      <span>Integrations</span>
    </div>
  </div>
  <div class='navigation-footer'>
    <h3>Company</h3>
    <div>
      <span>About</span>
      <span>Team</span>
      <span>Blog</span>
      <span>Careers</span>
    </div>
  </div>
  <div class='navigation-footer'>
    <h3>Connect</h3>
    <div>
      <span>Contact</span>
      <span>Newsletter</span>
      <span>LinkedIn</span>
    </div>
  </div>
  <div id='challenger'>
    Challenge by <a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>. 
    Coded by <a href="https://github.com/huyphan2210" target="_blank">Huy Phan</a>.
  </div>
</footer>
<style scoped>
  footer {
    position: relative;
    display: grid;
    grid-template-columns: 25% 25% 25% 25%;
    padding: 5rem 10rem;
    background-color: var(--very-dark-black-blue);
    border-radius: 0 10rem 0 0;
    color: white;
  }
    .navigation-footer h3 {
      font-size: 1rem;
    }

    .navigation-footer div {
      margin-block-start: 2rem;
    }

      .navigation-footer div span {
        display: block;
        margin-block-end: 1rem;
        color: var(--grayish-blue);
      }
        .navigation-footer div span:hover {
          cursor: pointer;
          text-decoration: underline;
        }
  
  #challenger {
    position: absolute;
    left: 50%;
    bottom: 1vh;
    transform: translate(-50%);
  }

@media screen and (max-aspect-ratio: 1) and (max-width: 767px) {
  footer {
    display: flex;
    flex-direction: column;
    padding: 4rem;
    text-align: center;
    align-items: center;
  }
  footer img {
    width: 40%;
    margin-bottom: 4rem;
  }

  #challenger {
    margin-block-start: 4rem;
    position: static;
    transform: none;
  }
}
</style>
