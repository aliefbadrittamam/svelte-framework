<script lang="ts">
    let nama = $state('Amir');
    let umur = $state(22);
    let bg = $state('bg-white');
  
    function ubahUsia() {
      umur = umur + 1;
    }
  
    function setBg(color: string) {
          bg = color;
      }
  
  </script>
  
  <h1>Hallo {nama} berusia: {umur}</h1>
  
  <p>
    <button onclick={ubahUsia}>Tambah Usia</button>
  </p>
  
  <div class={min-h-screen flex flex-col items-center justify-center transition-colors ${bg}}>
  
      <div class="space-x-4">
          <button onclick={() => setBg('bg-red-500')} class="px-4 py-2 bg-red-500 text-white"> Merah </button>
          <button onclick={() => setBg('bg-green-500')} class="px-4 py-2 bg-green-500 text-white"> Hijau </button>
          <button onclick={() => setBg('bg-blue-500')} class="px-4 py-2 bg-blue-500 text-white"> Biru </button>
      <button onclick={() => setBg('bg-white')} class="px-4 py-2 bg-white text-black"> Normal </button>
      </div>
  
  </div>