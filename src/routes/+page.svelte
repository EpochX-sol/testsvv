<script>
  import LoginForm from '../components/LoginForm.svelte';
  import RightContent from '../components/RightContent.svelte';
  import Header from '../components/Header.svelte';
</script>

<div class="page-container">
  <Header />
  <div class="main-content">
    <div class="left-section">
      <LoginForm />
    </div>
    <div class="right-section">
      <RightContent />
    </div>
  </div>
</div>

<style>
  .page-container {
    min-height: 100vh;
    background-color: #1a2332;
  }

  .main-content {
    display: grid;
    grid-template-columns: 1fr 1fr;
    min-height: 100vh;
    padding-top: 80px; 
  }

  .left-section {
    padding: 2rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background-color: white;
  }

  .right-section {
    height: calc(100vh - 80px); 
    overflow: hidden;
  }
 
  @media (max-width: 1024px) {
    .main-content {
      grid-template-columns: 1fr;
    }

    .right-section {
      display: none;
    }
  }
</style>