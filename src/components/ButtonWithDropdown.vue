<template>
    <main-dropdown>
        <template> 
            <img class="h-10 w-10 cursor-pointer rounded-full border-2 border-gray-400 object-cover" src="../assets/profile.png" alt="profile image">
            <transition enter-active-class="transition-all duration-100 ease-out" leave-active-class="transition-all duration-100 ease-in" enter-class="opacity-0 scale-75"
                enter-to-class="opacity-100 scale-100" leave-class="opacity-100 scale-100" leave-to-class="opacity-0 scale-75">
                <div class="origin-top-right absolute right-0 mt-2 w-64 bg-white border overflow-hidden rounded-lg shadow-md">
                    <ul>
                        <li>
                            <a to="/profile" class="rounded-t-lg block px-4 py-3 hover:bg-gray-100">
                                <div class="font-semibold ">{{ username }}</div>
                                <div class="text-gray-700">{{ email }}</div>
                            </a>
                        </li>
                        <li class="hover:bg-gray-100">
                            <a class="font-semibold block px-4 py-3" to="/profile">Profile</a>
                        </li>
                        <li class="hover:bg-gray-100">
                            <a class="font-semibold block px-4 py-3" to="/profile">Sign Out</a>
                        </li>
                    </ul>
                </div>
            </transition>
        </template>
    </main-dropdown>
</template>

<script>
import MainDropdown from "@/components/MainDropdown";
export default {
    name: "button-with-dropdown",
    data() {
        return {
            username: "John Wick",
            email: "dontkillmydog@johnwick.com"
        };
    },
    components: { MainDropdown }
};
</script>