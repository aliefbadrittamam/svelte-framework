<h1>hello world</h1>


<script lang="ts">

let activeColor = $state('');

function changeColor(color: string) {
    activeColor = color;
}

</script>

<h1>
    <div class={`text-${activeColor}-500 w-full h-screen`}>
        Current Color: {activeColor} 

    

    <button class="bg-red-500 hover:bg-red-700 text-white font-bold py-2 px-4 rounded" on:click={() => changeColor('red')}>
        Red Button
    </button>
    <button class="bg-green-500 hover:bg-green-700 text-white font-bold py-2 px-4 rounded" on:click={() => changeColor('green')}>
        Green Button
    </button>
    <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded" on:click={() => changeColor('blue')}>
        Blue Button
    </button>

    <div class={`bg-${activeColor}-500 h-20 w-full mt-4`}>    </div>
    <button class="bg-gray-500 hover:bg-gray-700 text-white font-bold py-2 px-4 rounded" on:click={() => changeColor('')}>
        Reset Color
    </button>
</h1>

