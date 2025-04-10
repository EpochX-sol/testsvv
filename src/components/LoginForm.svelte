<script lang="ts">
  let email = '';
  let password = '';
  let rememberMe = false;
</script>

<div class="login-container">
  <div class="login-card">
    <h1>Welcome back</h1>
    <p class="subtitle">Log in to access your SMASH account</p>
    
    <form>
      <div class="form-group">
        <label for="email">Email address</label>
        <div class="input-wrapper">
          <span class="input-icon">
            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
              <path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/>
              <polyline points="22,6 12,13 2,6"/>
            </svg>
          </span>
          <input 
            type="email" 
            id="email"
            bind:value={email}
            placeholder="name@company.com"
          />
        </div>
      </div>

      <div class="form-group">
        <label for="password">Password</label>
        <div class="input-wrapper">
          <span class="input-icon">
            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
              <rect x="3" y="11" width="18" height="11" rx="2" ry="2"/>
              <path d="M7 11V7a5 5 0 0 1 10 0v4"/>
            </svg>
          </span>
          <input 
            type="password" 
            id="password"
            bind:value={password}
            placeholder="••••••••"
          />
        </div>
      </div>

      <div class="form-options">
        <label class="remember-me">
          <input 
            type="checkbox" 
            bind:checked={rememberMe}
          />
          <span class="checkbox-custom">
            <svg xmlns="http://www.w3.org/2000/svg" width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round">
              <polyline points="20 6 9 17 4 12"/>
            </svg>
          </span>
          <span>Remember me</span>
        </label>
        <a href="/forgot-password" class="forgot-link">Forgot password?</a>
      </div>

      <button type="submit" class="login-button">Log in</button>

      <div class="signup-prompt">
        Don't have an account? <a href="/signup">Sign up</a>
      </div>
    </form>
  </div>
</div>

<style> 

  .login-card {
    background-color: #1e2837;
    padding: 2rem;
    border-radius: 12px;
    width: 450px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  }

  h1 {
    font-size: 1.75rem;
    font-weight: 600;
    color: white;
    margin-bottom: 0.5rem;
  }

  .subtitle {
    color: #8892a2;
    font-size: 0.9375rem;
    margin-bottom: 2rem;
  }

  .form-group {
    margin-bottom: 1.25rem;
  }

  label {
    display: block;
    color: white;
    font-size: 0.875rem;
    margin-bottom: 0.5rem;
  }

  .input-wrapper {
    position: relative;
  }

  .input-icon {
    position: absolute;
    left: 1rem;
    top: 50%;
    transform: translateY(-50%);
    color: #8892a2;
    display: flex;
    align-items: center;
  }

  input[type="email"],
  input[type="password"] {
    width: 100%;
    padding: 0.75rem 1rem 0.75rem 2.75rem;
    background-color: #2a3545;
    border: 1px solid #3a4555;
    border-radius: 6px;
    color: white;
    font-size: 0.9375rem;
    transition: border-color 0.2s;
  }

  input[type="email"]::placeholder,
  input[type="password"]::placeholder {
    color: #8892a2;
  }

  input[type="email"]:focus,
  input[type="password"]:focus {
    outline: none;
    border-color: #ff5631;
  }

  .form-options {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 1.5rem;
  }

  .remember-me {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    color: #8892a2;
    font-size: 0.875rem;
    cursor: pointer;
  }

  .remember-me input[type="checkbox"] {
    display: none;
  }

  .checkbox-custom {
    width: 1.25rem;
    height: 1.25rem;
    background-color: #2a3545;
    border: 1px solid #3a4555;
    border-radius: 4px;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: all 0.2s;
  }

  .checkbox-custom svg {
    opacity: 0;
    color: white;
    transition: opacity 0.2s;
  }

  .remember-me input[type="checkbox"]:checked + .checkbox-custom {
    background-color: #ff5631;
    border-color: #ff5631;
  }

  .remember-me input[type="checkbox"]:checked + .checkbox-custom svg {
    opacity: 1;
  }

  .forgot-link {
    color: #ff5631;
    text-decoration: none;
    font-size: 0.875rem;
    transition: color 0.2s;
  }

  .forgot-link:hover {
    color: #e64e2c;
  }

  .login-button {
    width: 100%;
    padding: 0.75rem;
    background-color: #ff5631;
    color: white;
    border: none;
    border-radius: 6px;
    font-size: 0.9375rem;
    font-weight: 500;
    cursor: pointer;
    transition: background-color 0.2s;
    margin-bottom: 1.5rem;
  }

  .login-button:hover {
    background-color: #e64e2c;
  }

  .signup-prompt {
    text-align: center;
    color: #8892a2;
    font-size: 0.875rem;
  }

  .signup-prompt a {
    color: #ff5631;
    text-decoration: none;
    transition: color 0.2s;
  }

  .signup-prompt a:hover {
    color: #e64e2c;
  }
</style> 