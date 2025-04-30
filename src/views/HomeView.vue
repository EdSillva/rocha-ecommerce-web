<script setup>
import AppNavbar from '../components/Navbar.vue'
// import heroImage from './assets/image/header-web.png'
</script>

<template>
    <div class="bg-black text-white min-h-screen">
        <!-- HERO SECTION -->
        <section class="flex items-center justify-center text-center px-4 py-32 text-white bg-black bg-opacity-60">
            <div>
                <h1 class="text-4xl md:text-5xl font-extrabold">Rocha Motopeças</h1>
                <p class="mt-4 text-xl font-light">A loja para a sua moto</p>
                <div class="mt-6 flex justify-center gap-4">
                    <button
                        class="bg-white text-black px-6 py-2 rounded-md font-medium hover:bg-gray-200 transition">Botão</button>
                    <button
                        class="border border-white px-6 py-2 rounded-md font-medium hover:bg-white hover:text-black transition">Botão</button>
                </div>
            </div>
        </section>
    </div>
</template>
