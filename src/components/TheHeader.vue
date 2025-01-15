<script setup lang="ts">
import {
    DropdownMenu,
    DropdownMenuContent,
    DropdownMenuItem,
    DropdownMenuLabel,
    DropdownMenuSeparator,
    DropdownMenuTrigger,
    DropdownMenuSub,
    DropdownMenuSubContent,
    DropdownMenuSubTrigger,
    DropdownMenuPortal
} from '@/components/ui/dropdown-menu'
import { CoHamburgerMenu } from '@kalimahapps/vue-icons';
import { useColorMode } from '@vueuse/core'


const mode = useColorMode()
</script>

<template>
    <div class="sticky z-40 bg-background/80 backdrop-blur-lg  p-2">
        <DropdownMenu>
            <div class="max-h-16 flex justify-between items-center">
                <img class="w-20 h-full" src="@/assets/log.png" />
                <DropdownMenuTrigger class="h-full">
                    <CoHamburgerMenu class="w-6 h-6  mx-2 text-primary dark:text-foreground transition-all " />
                </DropdownMenuTrigger>
            </div>
            <DropdownMenuContent>
                <DropdownMenuLabel>My Account
                </DropdownMenuLabel>
                <DropdownMenuSub>
                    <DropdownMenuSubTrigger>Theme</DropdownMenuSubTrigger>
                    <DropdownMenuPortal>
                        <DropdownMenuSubContent>
                            <DropdownMenuItem @click="mode = 'light'">Light</DropdownMenuItem>
                            <DropdownMenuItem @click="mode = 'dark'">Dark</DropdownMenuItem>
                            <DropdownMenuItem @click="mode = 'auto'">Auto</DropdownMenuItem>
                        </DropdownMenuSubContent>
                    </DropdownMenuPortal>
                </DropdownMenuSub>
                <DropdownMenuSeparator />
                <DropdownMenuItem>Profile</DropdownMenuItem>
                <DropdownMenuItem>Settings</DropdownMenuItem>
            </DropdownMenuContent>
        </DropdownMenu>
    </div>

</template>