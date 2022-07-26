<template>
    <main>
        <div class="container">
            <!-- informazioni azienda -->
            <div id="info-all" class="row d-flex justify-content-evenly align-items-center mx-auto">
                <div class="info-text col-12 d-flex flex-column justify-content-around" v-for="(info , index) in informations" :key="index">
                    <div class="d-flex fs-4">
                        <font-awesome-icon :icon="['fas', info.icon]" class="mr-3" />
                        <h6>{{ info.title }}</h6>
                    </div>
                    <p>
                        {{ info.text }}
                    </p>
                    <a :href="info.url" class="text-decoration-none"> 
                        {{ info.urlText }}
                    </a>
                </div>
            </div>
        </div>
    </main>
</template>

<script>
export default {
data() {
    return {
        informations: [
            {
                icon: " fa-trophy",
                title: "WHO WE ARE",
                text: "lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quidem.",
                url: "#",
                urlText: "Learn More"
            },
            {
                icon: " fa-bolt",
                title: "WHAT WE DO",
                text: "lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quidem.",
                url: "#",
                urlText: "Learn More"
            },
            {
                icon: " fa-question",
                title: "WHY US?",
                text: "lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quidem.",
                url: "#",
                urlText: "Learn More"
            },
        ]}
    }
}
</script>

<style lang='scss' scoped>
#info-all {
    width: 60%;
    height: 30vh;

    .info-text {
        width: 33%;
        height: 55%;
        text-align: left;
            
            h6 {
                color: #272727;
            }
        }
        p {
            font-size: 0.8rem;
            color: #878787;
        }
        a {
            color: #f72b0c;
            font-style: italic;
        }
    }
</style>