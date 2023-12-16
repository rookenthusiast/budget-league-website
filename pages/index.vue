<template>
    <section class="hero">
        <div class="container">
            <h1>EDH ON A BUDGET</h1>
            <h2>Proxy friendly leagues</h2>
            <v-card-text class="pa-0 pt-4" style="width: 50dvw;">
                <v-text-field rounded variant="solo" label="@ Enter email address" single-line><template #append-inner>
                        <v-btn color="indigo" rounded="xl">Join league</v-btn>
                    </template> </v-text-field>
            </v-card-text>
        </div>
    </section>
    <section class="details">
        <div class="card-container">
            <v-card class="mx-auto" max-width="400" rounded="xl" color="#5162FF" v-for="card in cards">
                <v-img class="align-end text-white" height="200" :src="card.imgSource" cover>
                </v-img>

                <v-card-title>{{ card.title }}</v-card-title>

                <v-card-text>
                    <div>Dorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam eu turpis molestie, dictum est
                        a, mattis tellus. Sed dignissim, metus nec fringilla accumsan, risus sem sollicitudin lacus, ut
                        interdum tellus elit sed risus. Maecenas eget condimentum velit, sit amet feugiat lectus.
                    </div>
                </v-card-text>
            </v-card>
        </div>
    </section>
    <section class="discord">
        <div class="discord-hero">
            <h2>Join us on our Discord</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Esse, aspernatur, fugit hic natus perferendis
                officiis mollitia assumenda tempore voluptatibus expedita atque quo. Aliquam expedita eaque quas suscipit
                dolor, sunt voluptas!</p>
                <v-img class='discord-logo' src="/images/discord.png" height="200px"></v-img>
        </div>
    </section>
</template>
<script setup>
const cards = ref([{ title: "What is budget league?", imgSource: "/images/bird-1.jpg" }, { title: "Who the duck are we?", imgSource: "/images/819129e0-the-goose-mother.jpg" }, { title: "how much does it cost?", imgSource: "/images/112637.hq.jpg" }])
</script>
<style>
.hero {
    position: relative;
    height: 100dvh;
}

.hero::before {
    content: "";
    position: absolute;
    background-image: url('/images/home-background.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: bottom;
    top: 0px;
    width: 100%;
    height: 100%;
    z-index: -1;
    opacity: 0.5;
    /* you need to match the shadow color to your background or image border for the desired effect*/
    mask-image: linear-gradient(#000 0 80%,rgba(0,0,0,0));
    /* Here is your opacity */
}

.container {
    max-width: 80dvw;
    padding: 200px 0;
    margin-left: auto;
    margin-right: auto;
    color: #fff;
}

.details {
    height: 100dvh;
    padding: 200px 0;
    margin-left: auto;
    margin-right: auto;
    background: linear-gradient(180deg, #2B2A6A 14.3%, #2B2A6A 72.8%);
    background-size: cover;
    background-repeat: no-repeat;
}

.discord {
    height: 100dvh;
    padding: 200px 0;
    background: linear-gradient(0deg, #1F76C9 14.3%, #2B2A6A 72.8%);
    background-size: cover;
    background-repeat: no-repeat;
}
.discord-hero {
    margin-left: auto;
    margin-right: auto;
    max-width: 60dvw;
    text-align: center;
    align-items: center;
    color:#fff;
}

.discord-logo {
    -webkit-filter: invert(100%); /* Safari/Chrome */
    filter: invert(100%);
}

.main>section {
    scroll-snap-align: start;
    scroll-snap-stop: always;
}


.card-container {
    display: flex;
    justify-content: space-around;
    align-items: center;
}
</style>
