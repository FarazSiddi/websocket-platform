<script>
    export let y;

    let tabs = [
        { name: "Stats", link: "#stats" },
        { name: "Settings", link: "#settings" },
    ];
</script>

<header class={"sticky z-[10] top-0 duration-200 px-6 py-6 flex items-center justify-between border border-solid bg-slate-300 border-slate-900 text-slate-900"}>
    <h1 class="font-medium">
        Welcome, <b class="font-bold poppins">Username</b>!
    </h1>
    <div class="sm:flex ml-auto pr-4 items-center gap-4 hidden">
        {#each tabs as tab, index}
          <a class="duration-200 hover:text-cyan-500" href={tab.link}>
            <p>{tab.name}</p>
          </a>
        {/each}
    </div>
    <a href="#logout" class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-white text-neutral-950">
        <div class="absolute top-0 right-full w-full h-full bg-cyan-400 opacity-20 group-hover:translate-x-full z-0 duration-200">

        </div>
        <h4 class="relative z-9">Log Out</h4>
    </a>
</header>