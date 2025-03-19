<template>
    <section id="nosotros">
        <div class="mx-auto max-w-7xl px-6 lg:px-8">
            <div class="mx-auto max-w-2xl lg:mx-0 lg:max-w-none">
                <div class="mt-6 flex flex-col gap-x-8 gap-y-20 lg:flex-row">
                    <div class="max-w-4xl">
                        <h2><span class="mb-6 block font-display text-base font-semibold text-primary">Sobre
                                nosotros</span><span class="sr-only"> - </span><span
                                class="block font-sans tracking-tight [text-wrap:balance] text-4xl font-medium sm:text-5xl text-secondary">Nuestra
                                misión</span>
                        </h2>
                        <div class="mt-6 text-xl text-secondary-400">
                            <p>Es ayudar a empresas y organizaciones a impulsar sus proyectos ofreciendo
                                una
                                Solución Personalizada de Comunicación y Marketing Holístico que potencie su notoriedad
                                y
                                se traduzca en ganancias.</p> <br>

                            <p>Desarrollamos, diseñamos y aplicamos estrategias, programas, procesos y actividades de
                                marketing y relaciones públicas para ofrecer una experiencia de marca coherente.</p>
                            <div class="mt-10 flex items-center gap-x-6">
                                <a href="#servicios"
                                    class="rounded-full bg-secondary px-3.5 py-2.5 text-sm font-semibold text-white shadow-xs hover:bg-secondary-500 focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-secondary">Nuestros
                                    Servicios</a>
                                <a href="#contacto"
                                    class="text-sm/6 font-semibold text-secondary hover:text-primary">Contáctanos<span
                                        aria-hidden="true">→</span></a>
                            </div>
                        </div>
                    </div>
                    <div class="lg:flex lg:flex-auto items-center lg:justify-center">
                        <dl class="w-64 space-y-8 xl:w-80">
                            <div class="flex flex-col-reverse gap-y-4">
                                <!-- <dt class="text-base/7 text-secondary-600">Estrategias de Marketing</dt> -->
                                <dd class="text-2xl font-semibold tracking-tight text-secondary hover:text-primary">
                                    Estrategias de
                                    Marketing</dd>
                            </div>
                            <div class="flex flex-col-reverse gap-y-4">
                                <!-- <dt class="text-base/7 text-secondary-600">Branding y creación de contenido</dt> -->
                                <dd class="text-2xl font-semibold tracking-tight text-secondary hover:text-primary">
                                    Branding y creación de
                                    contenido</dd>
                            </div>
                            <div class="flex flex-col-reverse gap-y-4">
                                <!-- <dt class="text-base/7 text-secondary-600">Relaciones públicas y gestión de reputación</dt> -->
                                <dd class="text-2xl font-semibold tracking-tight text-secondary hover:text-primary">
                                    Relaciones públicas y
                                    gestión de reputación</dd>
                            </div>
                        </dl>
                    </div>
                </div>
            </div>
        </div>

        <div class="bg-white py-12 md:py-32">
            <div class="mx-auto grid max-w-7xl grid-cols-1 gap-20 px-6 lg:px-8 xl:grid-cols-3">
                <div class="mx-auto max-w-2xl lg:mx-0">
                    <h2 class="text-4xl font-semibold tracking-tight text-pretty text-secondary sm:text-5xl">Nuestros
                        fundadores
                    </h2>
                    <p class="mt-6 text-lg/8 text-secondary-600">Entendemos que la unión de energías lo es todo porque
                        <i>“todo importa”</i>.
                    </p>
                </div>
                <ul role="list"
                    class="mx-auto grid max-w-2xl grid-cols-1 gap-x-6 gap-y-20 sm:grid-cols-2 lg:mx-0 lg:max-w-none lg:gap-x-8 xl:col-span-2">
                    <li v-for="(person, index) in fundadores" :key="index">
                        <img class="aspect-3/2 w-full rounded-2xl object-cover" :src="person.image" :alt="person.name">
                        <h3 class="mt-6 text-lg/8 font-semibold text-secondary">{{ person.name }}</h3>
                        <p class="text-base/7 text-secondary-600">{{ person.title }}</p>
                        <p class="mt-4 text-base/7 text-secondary-600" v-html="person.quote"></p>
                        <ul role="list" class="mt-6 flex gap-x-6">
                            <li>
                                <a href="#" class="text-gray-400 hover:text-gray-500">
                                    <span class="sr-only">X</span>
                                    <svg class="size-5" fill="currentColor" viewBox="0 0 20 20" aria-hidden="true">
                                        <path
                                            d="M11.4678 8.77491L17.2961 2H15.915L10.8543 7.88256L6.81232 2H2.15039L8.26263 10.8955L2.15039 18H3.53159L8.87581 11.7878L13.1444 18H17.8063L11.4675 8.77491H11.4678ZM9.57608 10.9738L8.95678 10.0881L4.02925 3.03974H6.15068L10.1273 8.72795L10.7466 9.61374L15.9156 17.0075H13.7942L9.57608 10.9742V10.9738Z" />
                                    </svg>
                                </a>
                            </li>
                            <li>
                                <a href="#" class="text-gray-400 hover:text-gray-500">
                                    <span class="sr-only">LinkedIn</span>
                                    <svg class="size-5" fill="currentColor" viewBox="0 0 20 20" aria-hidden="true">
                                        <path fill-rule="evenodd"
                                            d="M16.338 16.338H13.67V12.16c0-.995-.017-2.277-1.387-2.277-1.39 0-1.601 1.086-1.601 2.207v4.248H8.014v-8.59h2.559v1.174h.037c.356-.675 1.227-1.387 2.526-1.387 2.703 0 3.203 1.778 3.203 4.092v4.711zM5.005 6.575a1.548 1.548 0 11-.003-3.096 1.548 1.548 0 01.003 3.096zm-1.337 9.763H6.34v-8.59H3.667v8.59zM17.668 1H2.328C1.595 1 1 1.581 1 2.298v15.403C1 18.418 1.595 19 2.328 19h15.34c.734 0 1.332-.582 1.332-1.299V2.298C19 1.581 18.402 1 17.668 1z"
                                            clip-rule="evenodd" />
                                    </svg>
                                </a>
                            </li>
                        </ul>
                    </li>
                </ul>
            </div>
        </div>

        <!-- Image section -->
        <div class="my-24 xl:mx-auto xl:max-w-7xl xl:px-8">
            <img src="https://images.unsplash.com/photo-1529156069898-49953e39b3ac?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2832&q=80"
                alt="" class="aspect-5/2 w-full object-cover xl:rounded-3xl">
        </div>
    </section>
</template>

<script setup>
const fundadores = ref([
{
        name: "Alexander Santana",
        quote: `"Una estrategia de comunicación no solo proyecta la imagen de una marca, sino que construye relaciones de valor y confianza duraderas. En Ad-hoc, nos comprometemos a crear soluciones integrales, que no solo amplifiquen la presencia de nuestros clientes, sino que generen conexiones auténticas y sostenibles con sus audiencias."`,
        title: "CTO",
        image: "https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=8&w=1024&h=1024&q=80"
    },
    {
        name: "Nathalie Jackson",
        quote: `“En Ad-hoc validamos cada necesidad para diseñar estrategias que realmente generen impacto. Creemos en construir relaciones sólidas entre marcas y audiencias, guiados por un profundo entendimiento del valor de cada conexión."`,
        title: "CEO",
        image: "https://images.unsplash.com/photo-1517365830460-955ce3ccd263?ixlib=rb-=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=8&w=1024&h=1024&q=80"
    },
    
])
</script>