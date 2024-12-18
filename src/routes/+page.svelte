<script>
    let mensajeCifrado = ""; 
    let desplazamiento = 0; 
    let mensajeDescifrado = ""; 
  
    function descifrarMensaje() {
      mensajeDescifrado = ""; 
  
      for (let i = 0; i < mensajeCifrado.length; i++) {
        let letra = mensajeCifrado[i]; 
        let codigo = mensajeCifrado.charCodeAt(i); 
  
        
        if (codigo >= 65 && codigo <= 90) {
          let nuevaLetra = codigo - desplazamiento;
          if (nuevaLetra < 65) {
            nuevaLetra = nuevaLetra + 26;
          }
          mensajeDescifrado = mensajeDescifrado + String.fromCharCode(nuevaLetra);
        }
        
        else if (codigo >= 97 && codigo <= 122) {
          let nuevaLetra = codigo - desplazamiento;
          if (nuevaLetra < 97) {
            nuevaLetra = nuevaLetra + 26;
          }
          mensajeDescifrado = mensajeDescifrado + String.fromCharCode(nuevaLetra);
        }
        
        else {
          mensajeDescifrado = mensajeDescifrado + letra;
        }
      }
    }
  </script>
  
  <style>
    :global(body){
        display: flex;
        justify-content: center;
        align-items: center;
        min-height: 100vh;
    }
    .contenedor {
      width: 400px;
      border: 2px solid gray;
      padding: 10px;
      margin: 20px;
      text-align: center;
      border-radius: 10px;
    }
  
    input {
      margin-top: 10px;
      display: block;
      margin: 0 auto;
    }
  
    textarea {
      display: block;
      margin: 10px auto;
      width: 90%;
      height: 80px;
      resize: none;
    }
  
    button {
      background: #b0d8e6;
      border: 1px solid #0000ff;
      padding: 5px 10px;
    }
  </style>
  
  <div class="contenedor">
    <h2>Descifrador César</h2>
    <input type="text" placeholder="Escribe el mensaje cifrado" bind:value={mensajeCifrado}/>
    <p>Desplazamiento: {desplazamiento}</p>
    <input type="range" min="0" max="25" bind:value={desplazamiento}/>
    <textarea placeholder="Mensaje descifrado" bind:value={mensajeDescifrado}
      readonly
    ></textarea>
    <button on:click={descifrarMensaje}>DESCIFRAR</button>
  </div>