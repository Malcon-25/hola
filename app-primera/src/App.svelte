<script>
    let username = '';
    let email = '';
    let guardar = false;
  
    const handleSave = async () => {
      
      console.log('Guardando datos:', { username, email });
    };
  </script>
  
  {#if guardar}
    <div>
      <p>Bienvenido, {username}!</p>
      <button on:click={() => (guardar = false)}>Cerrar sesión</button>
    </div>
  {:else}
    <form>
      <label>
        Usuario:
        <input type="text" bind:value={username} />
      </label>
      <br />
      <label>
        Email:
        <input type="email" bind:value={email} />
      </label>
      <br />
      <button type="button" on:click={handleSave}>Guardar</button>
    </form>
  {/if}
  