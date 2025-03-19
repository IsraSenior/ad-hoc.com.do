<template>
    <section id="portafolio" class="bg-secondary-50 py-24 sm:py-32">
        <div class="mx-auto max-w-7xl px-6 lg:px-8">
            <div class="grid grid-cols-1 items-center gap-x-8 gap-y-16 lg:grid-cols-2">
                <div class="mx-auto w-full max-w-xl lg:mx-0 flex flex-start h-full">
                    <div>
                        <h2><span
                                class="mb-6 block font-display text-base font-semibold text-primary">Portafolio</span><span
                                class="sr-only"> - </span><span
                                class="block font-sans tracking-tight [text-wrap:balance] text-4xl font-medium sm:text-5xl text-secondary">En
                                Ad-hoc,
                                convertimos marcas en experiencias y estrategias en resultados concretos.</span>
                        </h2>
                        <p class="mt-6 text-xl text-secondary-400">Contamos con experiencia en los sectores: Retail,
                            Zona
                            Franca, Logística, Industrial, Energía, Turismo, Financiero, Tecnología,
                            Bebidas, Gobierno, Inmobiliario, Salud, Educación, Entretenimiento, ONGs.</p>
                        <!-- <div class="mt-8 flex items-center gap-x-6">
                        <a href="#"
                            class="rounded-full bg-secondary px-3.5 py-2.5 text-sm font-semibold text-white shadow-xs hover:bg-secondary-500 focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">Contáctanos</a>
                    </div> -->
                    </div>
                </div>

                <div>
                    <div class="grid grid-cols-3 gap-10 border-b border-dashed pb-14">
                        <div class="col-span-1 flex items-center justify-center">
                            <img class="h-auto w-full object-contain object-left"
                                :src="`/logos/${portfolio[currentPorfolio].logo}`"
                                :alt="portfolio[currentPorfolio].name">
                        </div>

                        <ul class="col-span-2 list list-disc flex items-start justify-center flex-col">
                            <li v-for="(item, index) in portfolio[currentPorfolio].items" :key="index">
                                {{ item }}
                            </li>
                        </ul>
                    </div>
                    <div
                        class="mt-14 mx-auto grid w-full max-w-xl grid-cols-3 items-center gap-y-12 sm:gap-y-14 lg:mx-0 lg:max-w-none lg:pl-8">
                        <div class="group grayscale hover:grayscale-0 cursor-pointer flex items-center justify-center"
                            @click.prevent="currentPorfolio = index" v-for="(client, index) in portfolio" :key="index">
                            <img class="h-auto max-h-[115px] w-2/3 object-contain object-left"
                                :src="`/logos/${client.logo}`" :alt="client.name">
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
const portfolio = ref([
    {
        name: "Texaco",
        logo: "texaco-logo.svg",
        items: [
            "Desarrollo y ejecución de programa monitoreo de servicio e imagen a nivel nacional.",
        ]
    },
    {
        name: "Nigua Free Zone",
        logo: "nfz-logo.svg",
        items: [
            "Reposicionamiento de valor.",
            "Creación de nueva visión de marca.",
            "RSCE.",
            "WeCare.",
            "Evento (1er. picazo expansión)"
        ]
    },
    {
        name: "Pioneer Investment Funds",
        logo: "pioneer-logo.svg",
        items: [
            "Acompañamiento corporativo estratégico de Pioneer y sus activos.",
        ]
    },
    {
        name: "CARDNET",
        logo: "cardnet-logo.svg",
        items: [
            "Acompañamiento estratégico, fortalecimiento de imagen y proyección pública.",
        ]
    },
    {
        name: "CRISFER.",
        logo: "crisfer-logo.png",
        items: [
            "Desarrollo y ejecución de programa de lealtad.",
            "Gestión de Crisis"
        ]
    },
    {
        name: "ADOSAFI",
        logo: "adosafi-logo.svg",
        items: [
            "Evento Internacional FIAFIN (2 ediciones).",
        ]
    },
    {
        name: "Club Med Miches Playa Esmeralda",
        logo: "miches-logo.svg",
        items: [
            "Evento (1er. Picazo / Inauguración)",
            ""
        ]
    },
    {
        name: "The St. Regis Cap Cana.",
        logo: "st-regis-logo.svg",
        items: [
            "Evento (1er. picazo)",
        ]
    },
    {
        name: "ViBIENda",
        logo: "vibienda-logo.svg",
        items: [
            "Evento (lanzamiento)",
        ]
    }
]);
const currentPorfolio = ref(0)
</script>
