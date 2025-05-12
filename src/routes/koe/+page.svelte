<script lang='ts'>
    let name = $state('reynal');
    let umur = $state(89);
    let activeColor = $state('');
    
    function ubahUsia() {
      umur = umur + 1;
    }
    
    function ubahWarna(color: string) {
      activeColor = color;
    }
    
    function resetWarna() {
      activeColor = '';
    }
  </script>
  
  <h1>halo {name} umur {umur}</h1>
  <div>
  <button class="bg-red-500 hover:bg-yellow-400 text-white font-bold py-2 px-4 rounded mr-2" on:click={() => ubahWarna('red')}>
  Red
  </button>
  
  <button class="bg-blue-500 hover:bg-yellow-400 text-white font-bold py-2 px-4 rounded mr-2" on:click={() => ubahWarna('blue')}>
  Blue
  </button>
  
  <button class="bg-green-500 hover:bg-yellow-400 text-white font-bold py-2 px-4 rounded mr-2" on:click={() => ubahWarna('green')}>
  Green
  </button>
  
  <button style={activeColor ? background-color: ${activeColor} : ''} class="hover:bg-gray-400 text-white font-bold py-2 px-4 rounded" on:click={resetWarna}>
  Reset Warna
  </button>
  
  <p class="mt-4">
  <button class="bg-green-500 hover:bg-green-600 text-white font-bold py-2 px-4 rounded" on:click={ubahUsia}>
    Tambah Usia
  </button>
  </p>
  
  </div>