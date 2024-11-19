<script>
    import content from '../../content/content.json'
    import Heading from './Heading.svelte';
    let regular = content.RegularMenu
    let regular_menu = regular.heading.split(' ')
    let food = regular.fooditems
</script>

<div class="flex flex-col ml-10 mt-20">
    <div class="flex flex-col gap-5 mb-14">
        <Heading w1={regular_menu[0]} w2={regular_menu[1]} w3={regular_menu[2]}/>
        <p class="text-lg">{regular.paragraph}</p>
    </div>
    <div class="grid grid-cols-[repeat(3,24rem)] grid-rows-3 gap-y-10">
        {#each food as item}
            <div class="flex flex-col bg-[#c63451] w-72 h-[21rem] items-center pt-7 rounded-xl text-white shadow-xl">
                <img class="w-56 h-44 rounded-lg shadow-lg mb-4" src={item.img} alt="">
                <h1 class="font-space_mono font-bold text-lg text-center mb-1 mt-2">{item.text}</h1>
                <div class="flex gap-3">
                    <div class="flex">
                        {#each  Array.from({ length: 5 }, (_, i) => i) as star}
                            <img class="w-4" src={regular.star} alt="">
                        {/each}
                    </div>
                    <p class="text-sm">{item.reviews} reviews</p>
                </div>
                <div class="flex gap-3 relative top-3">
                    <h2 class="text-2xl font-bold font-space_mono">${item.price}</h2>
                    <button>{regular.buy}</button>
                </div>
            </div>
        {/each}
    </div>
</div>
