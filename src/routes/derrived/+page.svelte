<script lang='ts'>
    let name = $state('alief');
    let umur = $state(140);

    const kuadratumur = $derived(umur * umur)

    
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

  <h1>halo umur say adaalh {umur} dan kuadrat umur saya adalah : {kuadratumur}</h1>
  
  

