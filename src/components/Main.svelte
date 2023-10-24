<script>
    import Step from "./Step.svelte";
    let steps = [
        {name: 'Joy', icon: 'fa-brands fa-discord', href: 'https://github.com/wanony/JoyBot'},
        {name: 'Skin Care App', icon: 'fa-brands fa-app-store-ios', href:'https://github.com/wanony/'},
        {name: 'Underwater Object Detection', icon: 'fa-solid fa-fish-fins', href: 'https://github.com/wanony/fyp'},
    ];
    let benefits = [
        {name: 'Life-long learner', description: "I'm always looking for the next challenge, and have an interest in staying up to date with the latest techology. After graduation I've been working on improving my side projects, while continuing to learn from free online resources."},
        {name: 'Realistic perfectionist', description: 'I always try to iterate on my previous work and improve it as I learn new tech. Joy was originally written in Python, and is now written in Kotlin and Java. Nothing is perfect, but if we keep improving our work, then we can get as close as possible.'},
        {name: 'Team player', description: 'I enjoy working with others as two heads are much better than one. In my experience at university and in my personal projects, having feedback and someone to communicate with helps with the problem solving process.'},
    ];
</script>

<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi, I'm <span class="poppins text-violet-400">wanony</span> <br/> graduate software
                <span class="poppins text-violet-400">developer</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="poppins text-violet-400">favourite tech</span> includes Kotlin, Python, C++, GoLang, and MySQL.
            </p>
            <a href="#" target="_blank" class="blueShadow mx-auto lg:mr-auto text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer">
                <div class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"></div>
                <h4 class="relative z-9">Get in touch &rarr;</h4>
            </a>
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img src={"images/penguin.gif"} alt="Profile image" class="object-cover z-[2] max-h-[70vh]" />
        </div>
    </section>
    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-large sm:text-xl md:text-2xl">
                A few of my creative endeavors.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Curious to <span class="poppins text-violet-400">see</span> my work?
            </h3>
        </div>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg: gap-10">
            <Step step={steps[0]}>
                <p>
                    Joy is a Discord chat bot written in <strong class="text-violet-400">Kotlin and Java</strong> that utilises the 
                    <strong
                        class="text-violet-400"
                        >JDA library, MySQL and DigitalOcean</strong
                    > to enable users to store links, and interact with many different social media APIs, including <strong class="text-violet-400">Instagram and Reddit</strong>.
                </p>
            </Step>
            <Step step={steps[1]}>
                <p>
                    Skin Carer is an app built with <strong class="text-violet-400">Swift</strong> that allows for users to
                    report changes in their skin, book appointments with their physicians and receive feedback on their reports. 
                    The app is being built for researching skin cancer
                </p>
            </Step>
            <Step step={steps[2]}>
                <p>
                    Utilised <strong class="text-violet-400">Python PyTorch, SciPy, NumPy and MMDetection</strong> to implement and 
                    train server instance segmentation machine learning models. Acquired and prepared an underwater sealife image 
                    dataset in the COCO format, and finally carrier out comparitive analysis of the models.
                </p>
            </Step>
        </div>
    </section>
    <section id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
        <div class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4">
            <h6 class="text-large sm:text-xl md:text-2xl">
                Want to know more?
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                A bit <span class="poppins text-violet-400">about</span> me.
            </h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
            I am . . .
        </p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}
                <div class="flex gap-6 sm:gap-8">
                    <p
                        class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold"
                    >
                        0{index + 1}
                    </p>
                    <div class="flex flex-col gap-6 sm:gap-8">
                        <h3 class="text-2xl sm:text-3xl md:text-5xl">
                            {benefit.name}
                        </h3>
                        <p>{benefit.description}</p>
                    </div>
                </div>
            {/each}
        </div>
    </section>
</main>