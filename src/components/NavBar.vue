<template>
    <nav class="navbar navbar-expand-lg bg-light">
        <div class="container">
            <a class="navbar-brand" href="#">KangTravel</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav me-auto">
                    <li class="nav-item">
                        <router-link class="nav-link" to="/">Home</router-link>
                    </li>
                    <li class="nav-item">
                        <router-link class="nav-link" to="/wisata">Paket Wisata</router-link>
                    </li>
                </ul>

                <ul class="navbar-nav">
                    <li class="nav-item ">
                        <router-link class="nav-link" to="/Keranjang">Keranjang
                            <b-icon-bag></b-icon-bag>
                            <span class="badge bg-success me-2">0</span>
                        </router-link>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</template>

<script>
export default {
    name : "NavBar"
}
</script>

<style>
    .navbar {
        position:absolute;
    }
</style>