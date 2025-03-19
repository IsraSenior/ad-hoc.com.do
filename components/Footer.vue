<template>
    <footer class="bg-secondary">
        <div class="mx-auto max-w-7xl overflow-hidden px-6 py-12 lg:px-8">
            <nav class="-mb-6 flex flex-wrap justify-center gap-x-12 gap-y-3 text-sm/6" aria-label="Footer">
                <a v-for="(item, index) in menu" :key="index" :href="item.hash" class="text-white hover:text-primary">{{
                    item.label }}</a>
            </nav>
            <ul class="mt-16 flex justify-center gap-x-10">
                <li><a href="#" target="_blank" rel="noopener noreferrer" class="text-white hover:text-primary"><svg
                            xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"
                            fill="currentColor">
                            <path
                                d="M20.947 8.305a6.53 6.53 0 0 0-.419-2.216 4.61 4.61 0 0 0-2.633-2.633 6.606 6.606 0 0 0-2.186-.42c-.962-.043-1.267-.055-3.709-.055s-2.755 0-3.71.055a6.606 6.606 0 0 0-2.185.42 4.607 4.607 0 0 0-2.633 2.633 6.554 6.554 0 0 0-.419 2.185c-.043.963-.056 1.268-.056 3.71s0 2.754.056 3.71c.015.748.156 1.486.419 2.187a4.61 4.61 0 0 0 2.634 2.632 6.584 6.584 0 0 0 2.185.45c.963.043 1.268.056 3.71.056s2.755 0 3.71-.056a6.59 6.59 0 0 0 2.186-.419 4.615 4.615 0 0 0 2.633-2.633c.263-.7.404-1.438.419-2.187.043-.962.056-1.267.056-3.71-.002-2.442-.002-2.752-.058-3.709zm-8.953 8.297c-2.554 0-4.623-2.069-4.623-4.623s2.069-4.623 4.623-4.623a4.623 4.623 0 0 1 0 9.246zm4.807-8.339a1.077 1.077 0 0 1-1.078-1.078 1.077 1.077 0 1 1 2.155 0c0 .596-.482 1.078-1.077 1.078z">
                            </path>
                            <circle cx="11.994" cy="11.979" r="3.003"></circle>
                        </svg></a></li>

                <li>
                    <a href="#" target="_blank" rel="noopener noreferrer" class="text-white hover:text-primary">
                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"
                            fill="currentColor">
                            <circle cx="4.983" cy="5.009" r="2.188"></circle>
                            <path
                                d="M9.237 8.855v12.139h3.769v-6.003c0-1.584.298-3.118 2.262-3.118 1.937 0 1.961 1.811 1.961 3.218v5.904H21v-6.657c0-3.27-.704-5.783-4.526-5.783-1.835 0-3.065 1.007-3.568 1.96h-.051v-1.66H9.237zm-6.142 0H6.87v12.139H3.095z">
                            </path>
                        </svg>
                    </a>
                </li>

                <li>
                    <a href="#" target="_blank" rel="noopener noreferrer" class="text-white hover:text-primary">
                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"
                            fill="currentColor">
                            <path
                                d="M13.397 20.997v-8.196h2.765l.411-3.209h-3.176V7.548c0-.926.258-1.56 1.587-1.56h1.684V3.127A22.336 22.336 0 0 0 14.201 3c-2.444 0-4.122 1.492-4.122 4.231v2.355H7.332v3.209h2.753v8.202h3.312z">
                            </path>
                        </svg>
                    </a>
                </li>
            </ul>
            <p class="mt-10 text-center text-sm/6 text-white">&copy; 2025 Ad-Hoc. Todos los derechos reservados.
            </p>
        </div>
    </footer>

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
])
</script>
