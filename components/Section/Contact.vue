<template>
    <section id="contacto" class="relative isolate bg-secondary-50 px-6 py-24 sm:py-32 lg:px-8">
        <div class="mx-auto max-w-xl lg:max-w-4xl">
            <div class="max-w-4xl">
                <h2><span class="mb-6 block font-display text-base font-semibold text-primary">Contacto</span><span
                        class="sr-only"> - </span><span
                        class="block font-sans tracking-tight [text-wrap:balance] text-4xl font-medium sm:text-5xl text-secondary">Somos
                        expertos en comunicación y marketing estratégico.</span>
                </h2>
                <div class="mt-6 text-xl text-secondary-400">
                    <p>El fin es que llegues a un mayor número de clientes, de manera más eficiente y efectiva.</p>
                </div>
            </div>
            <div class="mt-16 flex flex-col gap-16 sm:gap-y-20 lg:flex-row">
                <form action="#" method="POST" class="lg:flex-auto">
                    <div class="grid grid-cols-1 gap-x-8 gap-y-6 sm:grid-cols-2">
                        <div>
                            <label for="first-name" class="block text-sm/6 font-semibold text-secondary">Nombres</label>
                            <div class="mt-2.5">
                                <input type="text" name="first-name" id="first-name" autocomplete="given-name"
                                    class="block w-full rounded-full bg-secondary-50 focus:bg-white px-3.5 py-2 text-base text-secondary outline-1 -outline-offset-1 outline-secondary placeholder:text-secondary-400 focus:outline-2 focus:-outline-offset-2 focus:outline-primary">
                            </div>
                        </div>
                        <div>
                            <label for="last-name"
                                class="block text-sm/6 font-semibold text-secondary">Apellidos</label>
                            <div class="mt-2.5">
                                <input type="text" name="last-name" id="last-name" autocomplete="family-name"
                                    class="block w-full rounded-full bg-secondary-50 focus:bg-white px-3.5 py-2 text-base text-secondary outline-1 -outline-offset-1 outline-secondary placeholder:text-secondary-400 focus:outline-2 focus:-outline-offset-2 focus:outline-primary">
                            </div>
                        </div>
                        <div>
                            <label for="email" class="block text-sm/6 font-semibold text-secondary">Correo
                                electrónico</label>
                            <div class="mt-2.5">
                                <input type="email" name="email" id="email" autocomplete="email"
                                    class="block w-full rounded-full bg-secondary-50 focus:bg-white px-3.5 py-2 text-base text-secondary outline-1 -outline-offset-1 outline-secondary placeholder:text-secondary-400 focus:outline-2 focus:-outline-offset-2 focus:outline-primary">
                            </div>
                        </div>
                        <div>
                            <label for="phone" class="block text-sm/6 font-semibold text-secondary">Teléfono</label>
                            <div class="mt-2.5">
                                <input type="tel" name="phone" id="phone" autocomplete="phone"
                                    class="block w-full rounded-full bg-secondary-50 focus:bg-white px-3.5 py-2 text-base text-secondary outline-1 -outline-offset-1 outline-secondary placeholder:text-secondary-400 focus:outline-2 focus:-outline-offset-2 focus:outline-primary">
                            </div>
                        </div>
                        <div class="sm:col-span-2">
                            <label for="message" class="block text-sm/6 font-semibold text-secondary">Mensaje</label>
                            <div class="mt-2.5">
                                <textarea id="message" name="message" rows="4"
                                    class="block w-full rounded-3xl bg-secondary-50 focus:bg-white px-3.5 py-2 text-base text-secondary outline-1 -outline-offset-1 outline-secondary placeholder:text-secondary-400 focus:outline-2 focus:-outline-offset-2 focus:outline-primary"></textarea>
                            </div>
                        </div>
                    </div>
                    <div class="mt-10">
                        <button type="submit"
                            class="block w-full rounded-full bg-secondary px-3.5 py-2.5 text-center text-sm font-semibold text-white shadow-xs hover:bg-secondary-500 focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-secondary">¡Conversemos!</button>
                    </div>
                </form>

                <div class="lg:mt-6 lg:w-80 lg:flex-none">
                    <figure>
                        <blockquote class="text-lg/8 font-semibold text-secondary">
                            <p>Ad-hoc</p>
                        </blockquote>
                        <div class="mt-6 flex gap-x-6">
                            <div>
                                <p class="text-sm/6 text-secondary-600">Es una locución latina que significa
                                    literalmente <i>«para esto»</i>.</p>
                                <p class="text-sm/6 text-secondary-600 mt-4">Se refiere a una solución específicamente
                                    elaborada para un problema o fin preciso y, por tanto, no generalizable ni
                                    utilizable para otros propósitos.</p>
                                <p class="text-sm/6 text-secondary-600 mt-4">En sentido amplio, ad hoc puede traducirse
                                    como: <i>«específico»</i> o <i>«específicamente»</i>; <i>«especial»</i> o
                                    <i>«especializado»</i>
                                </p>
                            </div>
                        </div>
                    </figure>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>

</script>