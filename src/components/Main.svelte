<script>
    import Step from "./Step.svelte"
let steps = [
    {name:"Rimedra Mağazası", icon: "fa-solid fa-cart-shopping"},
    {name:"Takvimli Yapılacaklar Listesi", icon:"fa-solid fa-calendar-days"},
    {name:"Poke", icon:"fa-solid fa-diagram-project"}
]

let benefits = [
    {name:"a self-taught developer", description: "I taught myself to code using free online resources and absolutely fell in love with the creativity and problem solving that is involved in developing and engineering innovative new online experiences. Starting of with JavaScript, HTML & CSS and evolving my knowledge base to include JavaScript frameworks, backend programming, design, cloud services and much much more."
},
    {name:"a product design & UX finatic", description: "Carefully crafting and designing amazing user experiences allows me to express and experiment with every morsel of creativity I have. I love the challenge of learning new design concepts and enabling users with amazing online experiences."
},
    {name:"an excellent communicator", description:   "Communication is key and it's a paramount value of mine. I believe in transparency and constructive communication above all else. This helps me develop deep relationships and ensures my effectiveness and productivity in any work space with any team."
},

]

</script>


<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div
        class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
    >
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
            Hi! I'm <span class="poppins text-violet-400">Tunahan</span> Demir
            <br />Full Stack
            <span class="poppins text-violet-400">Developer</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
            My <span class="text-violet-400"> most used techs</span> includes JavaScript
            (NEXT.JS or SvelteKit), TailwindCSS, Node.js + Express.js & PostgreSQL
            or Firebase/Firestore!
            </p>
            <a href="https://github.com/Tunahan-Demir"
    class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer" 
>
    <div
        class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-10 duration-200"
    ></div>
    <h4 class="relative z-10">Get in touch &rarr;</h4>
</a>
        
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img src="src\images\tunapp(4).png" alt="profile-pic" class="object-cover z[2] max-h-[70vh]" >
        </div>
    </section>
    <section id="projects" class="py-20 lg:py:32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-large sm:text-xl md:text-2xl" >
                A few of my creative endeavors.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Curious to <span class="poppins text-violet-400">see</span> my work?
            </h3>
            
        </div>
        <a href="https://github.com/Rimedra" class="mx-auto px-4 py-2 rounded-md border border-solid border-whte flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-violet-700 duration-200">
            <i class="fa-brands fa-github"></i>
        <p>Go to my GitHub</p>
   </a>
   <p class="mx-auto -mt-20 text-xs"> or click the links below</p>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>Rimedra Kitap Mağazası <strong class="text-violet-400">Next.js Commerce.js Stripe& Node.js+ Express.js!</strong> ile yapıldı. Commerce.js bir Ürün İçerik Yönetim Sistemi ve Stripe ise tüm ödeme işlemlerinin yönetilmesi için kullanılan bir çevrimiçi ödeme altyapısıdır. </p>
            </Step>
            <Step step={steps[1]}>
                <p>Takvimli Yapılacaklar Listesi <strong class="text-violet-400">Next.js Commerce.js Stripe& Node.js+ Express.js!</strong> ile yapıldı. Commerce.js bir Ürün İçerik Yönetim Sistemi ve Stripe ise tüm ödeme işlemlerinin yönetilmesi için kullanılan bir çevrimiçi ödeme altyapısıdır. </p>
            </Step>
            <Step step={steps[2]}>
                <p>Rimedra Kitap Mağazası <strong class="text-violet-400">Next.js Commerce.js Stripe& Node.js+ Express.js!</strong> ile yapıldı. Commerce.js bir Ürün İçerik Yönetim Sistemi ve Stripe ise tüm ödeme işlemlerinin yönetilmesi için kullanılan bir çevrimiçi ödeme altyapısıdır. </p>
            </Step>
            
        </div>
    </section>

    <section id="about" class="py-20 pt-10 lg:pt16 lg:-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">

        <div class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-5">
            <h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
            <h3 class="font-semibold text-3xl sm:text-4l md:text-5xl">A bit <span class="poppins text-violet-400">about</span> me.</h3>
        </div>
        <p class=" mx-auto poppins font-somibold text-lg sm:text-xl md:text-2xl">I am . . .</p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index }
                <div class="flex gap-6 sm:gap-8">
                    <p class="poppins  text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold" >
                        0{index+1}
                    </p>
                    <div class="flex flex-col gap-6 sm:gap-8">
                        <h3 class="text-2xl sm:text-3xl md:5xl">
                            {benefit.name}
                        </h3>
                        <p class="">{benefit.description}</p>
                    </div>
                </div>
            {/each
                
            }
        </div>
        <h5 class="text-2xl sm:text-3xl font-semibold text-center poppins">The <span class="text-violet-400 poppins">Complete</span> Package</h5>
        <div class="flex flex-col overflow-x-scroll gap-10 max-w-[800*x] mx-auto w-full">
            <table class="bg-white text-slate-700 rounded text-center">
                <thead class="border-b border-slate-200">
                    <tr class="">
                        <th/>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #1</th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #2</th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #3</th>
                        <th class="whitespace-nowrap bg-violet-700 text-white p-4 px-8">Me</th>
                    </tr>
                </thead>
                <tbody >
                    <tr class="border-b border-solid border-slate-200">
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap">Dedication</td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-green-500"></i></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap">Critical Thought</td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-green-500"></i></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap">Interpersonal Skills</td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-green-500"></i></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap ">Programming Ability</td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-green-500"></i></td>
                    </tr>
                </tbody>
            </table>
        </div>
        <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
            <p>Scroll to see mor e&rarr;</p>
        </div>
        <p class="mx-auto poppins font-somibold text-lg sm:text-xl md:text-2xl">So why not invest?</p>
    </section>
</main>