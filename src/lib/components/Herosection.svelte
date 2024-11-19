<script>
    import content from '../../content/content.json'
    let hero = content.HeroSection
</script>

<div class="bg-[#c63451] flex h-[25rem] relative">
    <div class="flex flex-col ml-10 absolute top-32 gap-7">
        <h1 class="font-bold text-white font-space_mono text-5xl leading-[3.5rem] w-[35rem]">{hero.heading}</h1>
        <p class="text-white text-lg font-[Consolas] w-[30rem]">{hero.paragraph}</p>
        <div class="flex gap-4 bg-white w-36 py-3 px-4 rounded-lg relative bottom-3 shadow-xl">
            <img class="w-6 " src={hero.icons.buy} alt="">
            <p class="font-bold">{hero.buy}</p>
        </div>
    </div>
    <div>
        <img class="w-[30rem] absolute right-7" src={hero.heroimg} alt="">
    </div>
</div>
