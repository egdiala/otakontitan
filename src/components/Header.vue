<template>
    <div class="center examplex">
        <vs-navbar dark text-white square center-collapsed v-model="active">
        <template #left>
            <img src="https://vuesax.com/logos/logo-vuesax-logotipo-vuesax-png-4.png" width="150" alt="">
        </template>
        <vs-navbar-item :active="active == 'home'" id="home">
            Home
        </vs-navbar-item>
        <vs-navbar-item :active="active == 'docs'" id="docs">
            Gallery
        </vs-navbar-item>
        <template #right>
            <vs-switch dark v-model="active5" @click="$vs.theme = dark">
                <template #circle>
                    <i v-if="!active5" class='bx bxs-moon' ></i>
                    <i v-else class='bx bxs-sun' ></i>
                </template>
            </vs-switch>
        </template>
        </vs-navbar>
    </div>
</template>

<script>
    export default {
        data:() => ({
            active: 'home',
            active5: false,
        })
    }
</script>

<style scoped>
.examplex {
    margin-bottom: 10px;
}
</style>