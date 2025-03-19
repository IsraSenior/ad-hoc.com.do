<template>
    <section id="servicios" class="py-16 lg:py-32">
        <div class="mx-auto max-w-7xl px-6 lg:px-8">
            <div class="mx-auto max-w-2xl lg:max-w-none">
                <div class="max-w-4xl">
                    <h2><span class="mb-6 block font-display text-base font-semibold text-primary">Servicios</span><span
                            class="sr-only"> - </span><span
                            class="block font-sans tracking-tight [text-wrap:balance] text-4xl font-medium sm:text-5xl text-secondary">El
                            fin es que llegues a un mayor número de clientes, de manera más eficiente y efectiva.</span>
                    </h2>
                    <div class="mt-6 text-xl text-secondary-400">
                        <p>Trabajamos desde una perspectiva amplia e integrada reconociendo el alcance de cada punto de
                            contacto y la interdependencia de sus efectos.</p>
                    </div>
                </div>
            </div>
        </div>

        <div class="mx-auto max-w-7xl px-6 lg:px-8 mt-16">
            <div class="mx-auto max-w-2xl lg:max-w-none">
                <div class="h-full grid grid-cols-1 md:grid-cols-2 gap-10 lg:gap-20">
                    <div class="w-full flex-none relative h-full">
                        <div
                            class="sticky justify-center lg:justify-end top-10 flex aspect-719/680 w-full rounded-4xl overflow-hidden">
                            <img src="https://picsum.photos/800/500?random=1" alt="">
                        </div>
                    </div>
                    <div class="">
                        <ul role="list"
                            class="text-base text-neutral-600 mt-16 lg:mt-0 lg:w-1/2 lg:min-w-[33rem] lg:pl-4">
                            <li v-for="(service, index) in services" :key="index"
                                class="group mt-6 first:mt-0 border-t border-secondary border-dotted first:border-t-0 pt-6 first:pt-0">
                                <div class="relative">
                                    <div class="relative flex items-center justify-between">
                                        <div>
                                            <strong class="font-semibold text-secondary">{{ service.title }}.
                                            </strong> <br>
                                            <span class="text-primary font-normal">{{ service.intro }}</span>
                                        </div>
                                        <div class="px-5">
                                            <button @click.prevent="toogleService(index)">
                                                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
                                                    stroke-width="1.5" stroke="currentColor" class="size-6">
                                                    <path v-if="currentService !== index" stroke-linecap="round"
                                                        stroke-linejoin="round" d="M12 4.5v15m7.5-7.5h-15" />
                                                    <path v-else stroke-linecap="round" stroke-linejoin="round"
                                                        d="M5 12h14" />
                                                </svg>
                                            </button>
                                        </div>
                                    </div>

                                    <Transition v-if="index === currentService"
                                        enter-active-class="transition ease-out duration-100"
                                        enter-from-class="transform opacity-0 scale-95"
                                        enter-to-class="transform opacity-100 scale-100"
                                        leave-active-class="transition ease-in duration-75"
                                        leave-from-class="transform opacity-100 scale-100"
                                        leave-to-class="transform opacity-0 scale-95">
                                        <div class="relative">
                                            <div class="mt-4 relative text-secondary-400">
                                                {{ service.content }}
                                            </div>

                                            <ul v-if="service?.items" class="mt-4 list-disc list-inside">
                                                <li v-for="(item, index_i) in service?.items" :key="index_i"
                                                    v-html="item" class="text-secondary-400">
                                                </li>
                                            </ul>

                                            <ul v-if="service?.groupedItems" class="mt-4">
                                                <li v-for="(item_g, index_i) in service?.groupedItems" :key="index_i"
                                                    class="mt-4">
                                                    <span class="font-semibold">{{ item_g?.title }}</span>
                                                    <ul class="mt-4 list-disc list-inside">
                                                        <li v-for="(item_l, index_g) in item_g?.items" :key="index_g"
                                                            v-html="item_l" class="text-secondary-400"></li>
                                                    </ul>
                                                </li>
                                            </ul>
                                        </div>
                                    </Transition>
                                </div>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
const services = ref([
    {
        title: "Eventos",
        intro: "Poderosas plataformas que crean experiencias y conectan.",
        content: "Las experiencias cuentan más que las palabras. Se trata de sumergir a los asistentes en la esencia de la marca, de compartir momentos que despierten emociones y construyan vínculos genuinos con la marca.",
        items: [
            "Planificación y conceptualización (lanzamientos e inauguraciones, convenciones, eventos culturales, ruedas de prensa, entre otros).",
            "Gestión logística.",
            "Producción audiovisual y multimedia.",
            "Gestión de invitados y experiencia del cliente.",
            "Coordinación de relaciones públicas y media relations.",
        ]
    },
    {
        title: "Relaciones Públicas",
        intro: "Escuchar, informar, persuadir para lograr consenso.",
        content: "Desempeñan un papel importante esencial en las estrategias de comunicación. Su principal objetivo será siempre el de fortalecer los vínculos con los distintos públicos para lograr fidelidad y apoyo.",
        items: [
            "Plan estratégico de reputación corporativa",
            "Plan estratégico de gestión de crisis",
            "Plan de relacionamiento empresarial",
            "Plan de relacionamiento de directivos",
            "Estrategia de opinión pública y movilización social",
            "Gobernanza y asuntos públicos",
            "Relaciones con los medios",
            "Elaboración / redacción de textos",
        ]
    },
    {
        title: "Corporativo",
        intro: "El curso de acción debe ser conscientemente anticipado.",
        content: "Las empresas exigen ser gestionadas a través de un plan estratégico capaz de administrar las percepciones, emociones, opiniones y actitudes de los diferentes grupos de interés y de guiar hacia el logro de objetivos.",
        items: [
            "Comunicación interna / externa",
            "Cultura organizacional",
            "Fusiones y adquisiciones / reestructuraciones",
            "Gestión de crisis",
            "Posicionamiento y formación de directivos y portavoces",
        ]
    },
    {
        title: "Comunidad",
        intro: "Crear un negocio fuerte y un mundo mejor no son metas contradictorias.",
        content: "Solo cuando una marca se ha definido a sí misma y sus valores es cuando puede identificar las causas o iniciativas de responsabilidad que se alinean con su historia.",
        items: [
            "Responsabilidad Social Corporativa (RSC)",
            "Ética corporativa y comunicación social",
            "Acción social",
        ]
    },
    {
        title: "Riesgo",
        intro: "Preverlo todo es imposible. Se trata de anticiparse.",
        content: "Dotar a la empresa de mecanismos que eviten o atenúen los efectos de contingencias potenciales.",
        items: [
            "Anticipación",
            "Gestión",
            "Recuperación",
            "Seguimiento",
        ]
    },
    {
        title: "Posicionamiento de valor",
        intro: "Las grandes marcas ya no se anuncian, se relacionan.",
        content: "Deben convertir cada contacto con el cliente en experiencias que generen emociones memorables. Crear experiencias 360º haciendo partícipes a sus clientes.",
        items: null,
        groupedItems: [
            {
                title: "Desarrollo de estrategias de marca",
                items: [
                    "Programas estratégicos de mercadeo / servicio al cliente",
                    "Programas de lealtad / reconocimiento",
                    "Programas de monitoreo de calidad(procesos, servicio, imagen...)",
                    "Activaciones promocionales / patrocinios",
                ]
            },
            {
                title: "Desarrollo de contenido",
                items: [
                    "Periodismo de marca(Copywriting y Redacción)",
                    "Digital(identidad digital, inteligencia y manejo de redes)",
                    "Desarrollo web",
                    "Capacitación de influenciadores",
                ]
            }
        ]
    },
    {
        title: "Aplicación de insights",
        intro: "Enfocar la mira en la audiencia es esencial para estrategias que resuenen.",
        content: "La investigación de mercado es la columna vertebral de cualquier estrategia de negocios. Empodera para la toma de decisiones y alerta de amenazas y oportunidades que se aproximan.",
        items: [
            "Mystery Shoppers",
            "Inmersión / talleres para desarrollo de estrategias (consumidores y clientes)",
            "Captura de insights para contestar preguntas clave",
        ]
    },
]);
const currentService = ref(0);
const toogleService = (index) => {
    currentService.value = currentService.value === index ? null : index;
}
</script>