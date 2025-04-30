<script setup>
import { Disclosure } from '@headlessui/vue'
import { Bars3Icon, XMarkIcon, ShoppingCartIcon, UserCircleIcon } from '@heroicons/vue/24/outline'
import logo from '@/assets/image/logo-web.png'

const links = [
    { name: 'Esportivo', href: '#' },
    { name: 'Street', href: '#' },
]
</script>

<template>
    <Disclosure as="nav" class="bg-black bg-opacity-70 text-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-16 items-center">
                <!-- LOGO -->
                <div class="flex items-center gap-6">
                    <img :src="logo" class="h-10" alt="Logo" />

                    <!-- LINKS DESKTOP -->
                    <div class="hidden md:flex gap-4 text-sm font-medium">
                        <a v-for="(item, index) in links" :key="index" :href="item.href" class="hover:underline">
                            {{ item.name }}
                        </a>
                    </div>
                </div>

                <!-- AÇÕES -->
                <div class="hidden md:flex items-center gap-6">
                    <span class="text-sm font-semibold">R$300,00</span>
                    <ShoppingCartIcon class="h-6 w-6" />
                    <UserCircleIcon class="h-6 w-6" />
                </div>

                <!-- BOTÃO MOBILE -->
                <div class="md:hidden">
                    <Disclosure.Button
                        class="inline-flex items-center justify-center p-2 rounded-md text-white hover:text-gray-300 focus:outline-none">
                        <Bars3Icon class="block h-6 w-6" />
                    </Disclosure.Button>
                </div>
            </div>
        </div>

        <!-- MENU MOBILE -->
        <Disclosure.Panel class="md:hidden px-4 pb-4 pt-2 space-y-2">
            <div class="flex flex-col gap-2 text-sm font-medium">
                <a v-for="(item, index) in links" :key="index" :href="item.href" class="hover:underline">
                    {{ item.name }}
                </a>
                <div class="flex justify-between items-center pt-4 border-t border-white/10">
                    <span class="font-semibold">R$300,00</span>
                    <div class="flex gap-4">
                        <ShoppingCartIcon class="h-6 w-6" />
                        <UserCircleIcon class="h-6 w-6" />
                    </div>
                </div>
            </div>
        </Disclosure.Panel>
    </Disclosure>
</template>
