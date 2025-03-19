<template>
    <header class="pointer-events-none relative z-50 flex flex-none flex-col">
        <div class="fixed top-0 z-10 h-16 pt-6 w-full">
            <div class="sm:px-8 w-full">
                <div class="mx-auto w-full max-w-7xl lg:px-8">
                    <div class="relative px-4 sm:px-8 lg:px-12">
                        <div class="mx-auto max-w-2xl lg:max-w-5xl">
                            <div class="relative flex items-center gap-4">
                                <div class="flex flex-1">
                                    <div class="h-auto w-auto">
                                        <a aria-label="Home" class="pointer-events-auto" href="/">
                                            <img src="/logo.svg" class="h-16 drop-shadow-lg shadow-secondary/5" alt="">
                                        </a>
                                    </div>
                                </div>

                                <div class="flex flex-1 justify-end md:justify-center">
                                    <div class="pointer-events-auto md:hidden"><button @click="toogle = true"
                                            class="group flex items-center rounded-full bg-white/90 px-4 py-2 text-sm font-medium text-secondary ring-1 shadow-lg shadow-secondary/5 ring-secondary-900/5 backdrop-blur-sm"
                                            type="button">Menu<svg viewBox="0 0 8 6" aria-hidden="true"
                                                class="ml-3 h-auto w-2 stroke-secondary-500 group-hover:stroke-secondary-700">
                                                <path d="M1.75 1.75 4 4.25l2.25-2.5" fill="none" stroke-width="1.5"
                                                    stroke-linecap="round" stroke-linejoin="round"></path>
                                            </svg></button>

                                        <div v-if="toogle"
                                            class="fixed inset-0 z-50 bg-secondary-800/40 backdrop-blur-xs duration-150 data-closed:opacity-0 data-enter:ease-out data-leave:ease-in">
                                        </div>

                                        <div v-if="toogle" class="fixed inset-x-4 top-8 z-50 origin-top rounded-3xl bg-white p-8
                                            ring-1 ring-secondary-900/5 duration-150 data-closed:scale-95
                                            data-closed:opacity-0 data-enter:ease-out data-leave:ease-in">
                                            <div class="flex flex-row-reverse items-center justify-between">
                                                <button @click.prevent="toogle = false" aria-label="Close menu"
                                                    class="-m-1 p-1" type="button" data-headlessui-state="open active"
                                                    data-open="" data-active=""><svg viewBox="0 0 24 24"
                                                        aria-hidden="true" class="h-6 w-6 text-secondary-500 ">
                                                        <path d="m17.25 6.75-10.5 10.5M6.75 6.75l10.5 10.5" fill="none"
                                                            stroke="currentColor" stroke-width="1.5"
                                                            stroke-linecap="round" stroke-linejoin="round"></path>
                                                    </svg>
                                                </button>

                                            </div>
                                            <nav class="mt-6">
                                                <ul
                                                    class="-my-2 divide-y divide-secondary-100 text-base text-secondary-800">
                                                    <li v-for="(item, index) in menu" :key="index"><a @click.native="toogle=false"
                                                            class="block py-2 text-center" :href="item.hash">{{
                                                                item.label }}</a></li>
                                                </ul>
                                                <div class="mt-6">
                                                    <a href="#contacto" type="button" @click.native="toogle=false"
                                                        class="w-full flex items-center justify-center rounded-full bg-secondary px-3 py-1.5 text-sm font-semibold text-white shadow-lg hover:bg-secondary-500 focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-secondary-600">Contacto</a>

                                                    <ul class="flex items-center justify-center space-x-4 mt-6">
                                                        <li><a href="#" target="_blank" rel="noopener noreferrer"><svg
                                                                    xmlns="http://www.w3.org/2000/svg" width="24"
                                                                    height="24" viewBox="0 0 24 24" fill="currentColor">
                                                                    <path
                                                                        d="M20.947 8.305a6.53 6.53 0 0 0-.419-2.216 4.61 4.61 0 0 0-2.633-2.633 6.606 6.606 0 0 0-2.186-.42c-.962-.043-1.267-.055-3.709-.055s-2.755 0-3.71.055a6.606 6.606 0 0 0-2.185.42 4.607 4.607 0 0 0-2.633 2.633 6.554 6.554 0 0 0-.419 2.185c-.043.963-.056 1.268-.056 3.71s0 2.754.056 3.71c.015.748.156 1.486.419 2.187a4.61 4.61 0 0 0 2.634 2.632 6.584 6.584 0 0 0 2.185.45c.963.043 1.268.056 3.71.056s2.755 0 3.71-.056a6.59 6.59 0 0 0 2.186-.419 4.615 4.615 0 0 0 2.633-2.633c.263-.7.404-1.438.419-2.187.043-.962.056-1.267.056-3.71-.002-2.442-.002-2.752-.058-3.709zm-8.953 8.297c-2.554 0-4.623-2.069-4.623-4.623s2.069-4.623 4.623-4.623a4.623 4.623 0 0 1 0 9.246zm4.807-8.339a1.077 1.077 0 0 1-1.078-1.078 1.077 1.077 0 1 1 2.155 0c0 .596-.482 1.078-1.077 1.078z">
                                                                    </path>
                                                                    <circle cx="11.994" cy="11.979" r="3.003"></circle>
                                                                </svg></a></li>

                                                        <li>
                                                            <a href="#" target="_blank" rel="noopener noreferrer">
                                                                <svg xmlns="http://www.w3.org/2000/svg" width="24"
                                                                    height="24" viewBox="0 0 24 24" fill="currentColor">
                                                                    <circle cx="4.983" cy="5.009" r="2.188"></circle>
                                                                    <path
                                                                        d="M9.237 8.855v12.139h3.769v-6.003c0-1.584.298-3.118 2.262-3.118 1.937 0 1.961 1.811 1.961 3.218v5.904H21v-6.657c0-3.27-.704-5.783-4.526-5.783-1.835 0-3.065 1.007-3.568 1.96h-.051v-1.66H9.237zm-6.142 0H6.87v12.139H3.095z">
                                                                    </path>
                                                                </svg>
                                                            </a>
                                                        </li>

                                                        <li>
                                                            <a href="#" target="_blank" rel="noopener noreferrer">
                                                                <svg xmlns="http://www.w3.org/2000/svg" width="24"
                                                                    height="24" viewBox="0 0 24 24" fill="currentColor">
                                                                    <path
                                                                        d="M13.397 20.997v-8.196h2.765l.411-3.209h-3.176V7.548c0-.926.258-1.56 1.587-1.56h1.684V3.127A22.336 22.336 0 0 0 14.201 3c-2.444 0-4.122 1.492-4.122 4.231v2.355H7.332v3.209h2.753v8.202h3.312z">
                                                                    </path>
                                                                </svg>
                                                            </a>
                                                        </li>
                                                    </ul>
                                                </div>
                                            </nav>
                                        </div>
                                    </div>

                                    <nav class="pointer-events-auto hidden md:block">
                                        <ul
                                            class="flex rounded-full bg-white/90 px-3 text-sm font-medium text-secondary ring-1 shadow-lg shadow-secondary/5 ring-secondary-900/5 backdrop-blur-sm">
                                            <li v-for="(item, index) in menu" :key="index"><a
                                                    class="relative block px-3 py-2 transition hover:text-secondary-500"
                                                    :href="item.hash">{{ item.label }}</a></li>
                                        </ul>
                                    </nav>
                                </div>

                                <div class="justify-end md:flex-1 hidden md:flex">
                                    <div class="">
                                        <a href="#contacto"
                                            class="rounded-full bg-secondary px-3 py-1.5 text-sm font-semibold text-white shadow-lg shadow-secondary/5 hover:bg-secondary-500 focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-secondary-600">Contacto</a>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>

<script setup>
const menu = ref([
    {
        label: "Nosotros",
        hash: "#nosotros"
    },
    {
        label: "Servicios",
        hash: "#servicios"
    },
    {
        label: "Portafolio",
        hash: "#portafolio"
    },
]);
const toogle = ref(false);
</script>