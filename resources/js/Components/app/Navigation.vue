<script setup>
   import {Link} from '@inertiajs/vue3';
   import ApplicationLogo from "@/Components/ApplicationLogo.vue";
   import CreateNewDropdown from "@/Components/app/CreateNewDropdown.vue";
   import NavLink from "@/Components/NavLink.vue"
</script>

<template>
       <nav class="min-w-[200px]">
        <Link href="/" class="h-[80px] px-3 flex items-center gap-3">
            <ApplicationLogo
                class="block h-9 w-auto fill-current text-gray-800"
            />
            LaraStorage
        </Link>
         <div class="px-3">
            <CreateNewDropdown/>
            <div>
                <NavLink href="" :active="$page.props.route_name === 'myFiles'">My Files</NavLink>
                <NavLink href="" :active="$page.props.route_name === 'file.sharedWithMe'">Shared with me</NavLink>
                <NavLink href="" :active="$page.props.route_name === 'file.sharedByMe'">Shared by me</NavLink>
                <NavLink href="" :active="$page.props.route_name === 'trash'">Trash</NavLink>
            </div>
         </div>
       </nav>
</template>



