<script>
  import Header from './Header.svelte';
</script>

<div class="right-content">
  <div class="content">
    <div class="top-text">
      <h1>Elevate Your Game</h1>
      <p>Join the leading platform for personalized coaching and skill development.</p>
    </div>
    
    <div class="testimonial">
      <p class="quote">"SMASH has transformed how I train and coach my athletes."</p>
      <p class="author">— Professional Coach</p>
    </div>
  </div>
</div>

<style>
  .right-content {
    background-color: #ff5631;
    color: white;
    height: 100%;
    position: relative;
    overflow: hidden;
  }

  .content {
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    padding: 8rem 2rem;
    position: relative;
    z-index: 1;
  }

  .top-text {
    text-align: center;
    max-width: 600px;
    margin: 0 auto;
  }

  h1 {
    font-size: 2.5rem;
    font-weight: 700;
    margin-bottom: 1rem;
    line-height: 1.2;
  }

  p {
    font-size: 1.25rem;
    line-height: 1.6;
    margin: 0;
  }

  .testimonial {
    text-align: center;
    max-width: 600px;
    margin: 0 auto;
  }

  .quote {
    font-style: italic;
    font-size: 1.25rem;
    margin-bottom: 0.5rem;
  }

  .author {
    font-weight: 600;
  }
 
  .right-content::after {
    content: '';
    position: absolute;
    top: 55%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 300px;
    height: 300px;
    background: rgba(255, 255, 255, 0.1);
    border-radius: 50%;
    pointer-events: none;
  }
</style> 