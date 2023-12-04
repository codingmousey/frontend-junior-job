<script>
    let username = '';
    let password = '';
    let passwordCheck = '';
    let registrationError = '';
  </script>
  
  <section>
    <h2>Signup</h2>
  
    <form on:submit>
      <label>
        Username:
        <input type="text" bind:value={username} />
      </label>
  
      <label>
        Password:
        <input type="password" bind:value={password} />
      </label>
  
      <label>
        Confirm Password:
        <input type="password" bind:value={passwordCheck} />
      </label>
  
      <button type="submit">Sign up</button>
    </form>
  </section>
  
  <style>
    section {
      text-align: center;
      padding: 2em;
    }
  
    h2 {
      color: #ff3e00;
    }
  
    form {
      display: flex;
      flex-direction: column;
      max-width: 300px;
      margin: 0 auto;
    }
  
    label {
      margin-top: 1em;
      display: flex;
      flex-direction: column;
    }
  
    input {
      margin-top: 0.5em;
      padding: 0.5em;
    }
  
    button {
      margin-top: 1em;
      padding: 0.5em 1em;
      cursor: pointer;
      background-color: antiquewhite;
    }
  </style>
  