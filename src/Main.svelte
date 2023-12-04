<script>
    import { Link } from 'svelte-routing';
  </script>
  
  <main>
    <h1>Main Component</h1>
    <p>Welcome to the very first version of my Svelte frontend site</p>
    <Link to="/signup">Not an account already? Sign up!</Link>
  </main>
  
  <style>
    main {
      text-align: center;
      padding: 1em;
      max-width: 240px;
      margin: 0 auto;
    }
  
    h1 {
      color: #ff3e00;
      text-transform: uppercase;
      font-size: 2em;
      font-weight: 100;
    }
  </style>
  