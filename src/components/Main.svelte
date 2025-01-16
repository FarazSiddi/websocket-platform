<script>
    const buttons = [
      { id: 1, image: '/images/icon1.png', text: 'Button 1' },
      { id: 2, image: '/images/icon2.png', text: 'Button 2' },
      { id: 3, image: '/images/icon3.png', text: 'Button 3' },
      { id: 4, image: '/images/icon4.png', text: 'Button 4' },
      { id: 5, image: '/images/icon5.png', text: 'Button 5' },
      { id: 6, image: '/images/icon6.png', text: 'Button 6' },
      { id: 7, image: '/images/icon7.png', text: 'Button 7' },
      { id: 8, image: '/images/icon8.png', text: 'Button 8' },
      { id: 9, image: '/images/icon9.png', text: 'Button 9' }
    ];
  
    function handleClick(button) {
      alert(`Clicked on ${button.text}`);
    }
  </script>
  
  <main>
    <div class="grid grid-cols-1 lg:grid-cols-3 place-items-center min-h-[80vh] p-10 gap-12 lg:gap-10">
      {#each buttons as button}
        <button class="flex flex-col items-center justify-center bg-gray-200 p-16 cursor-pointer rounded-lg shadow-md hover:bg-gray-300" on:click={() => handleClick(button)}>
          <img class="w-12 h-12 object-contain"  alt={button.text} />
          <span class="mt-2 text-lg">{button.text}</span>
        </button>
      {/each}
    </div>
  </main>