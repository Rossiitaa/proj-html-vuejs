<template>
    <main>
        <div class="container">
            <!-- informazioni azienda -->
            <div id="info-general" class="row d-flex justify-content-evenly align-items-center mx-auto">
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
            <!-- countdown -->
        <div class="container-fluid">
            <div id="countdown" class="row d-flex align-items-center">
                <div id="count-card" class="d-flex flex-column justify-content-between">
                    <div class=" d-flex justify-content-center">
                        <div class="card align-items-center py-4 px-5 mx-2"
                        v-for="(count, index) in countdown" :key="index" :style="`background: ${count.bg}; opacity: ${count.transp}`">
                            <h1>
                                {{ count.number }}
                            </h1>
                            <span>
                                {{ count.text }}
                            </span>
                        </div>
                    </div>

                    <h5 class="fw-bold">
                        SUBSCRIBE FOR UPDATES
                    </h5>
                    <div id="update">
                        <input type="text" placeholder="Please fill your email"
                        class="p-3 mx-3">
                        <button class="p-3 px-4">
                            SUBSCRIBE
                        </button>
                    </div>
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
                icon: "fas fa-trophy",
                title: "WHO WE ARE",
                text: "lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quidem.",
                url: "#",
                urlText: "Learn More"
            },
            {
                icon: "fas fa-bolt",
                title: "WHAT WE DO",
                text: "lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quidem.",
                url: "#",
                urlText: "Learn More"
            },
            {
                icon: "fas fa-question",
                title: "WHY US?",
                text: "lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quidem.",
                url: "#",
                urlText: "Learn More"
            },
        ],
        countdown: [
            {
                number: "3399",
                text: "DAYS",
                bg: "@000",
                transp: "0.8"
            },
            {
                number: "17",
                text: "HOURS",
                bg: "@000",
                transp: "0.7"
            },
            {
                number: "28",
                text: "MINS",
                bg: "@000",
                transp: "0.5"
            },
            {
                number: "17",
                text: "SECS",
                bg: "@000",
                transp: "0.3"
            },
        ]
        }
    }
}
</script>

<style lang='scss' scoped>
#info-general {
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
            color: #868686;
        }
        a {
            color: #f72b0c;
            font-style: italic;
        }
    }

#countdown {
    height: 50vh;
    background: url(../assets/images/coutdown-bg1.jpg);
    background-size: contain;
    background-position: center;
    #count-card {
        height: 70%;
            h1 {
                font-size: 50px;
                font-weight: 700;
            }
            .card {
                background-color: #000;
                color: #fff;
            }
        }
        #update {
            font-size: 13px;
            width: 100%;
            display: flex;
            justify-content: center;
            
            input {
                outline: 0;
                border: 0;
                width: 22%;
            }
            button {
                font-weight: 700;
                border-width: 0 0 3px 0;
                border-color: #d92719;
                background: #f72b0c;
                color: #fff;
            }
        }
        h5 {
                display: flex;
                justify-content: center;
            }
    }
</style>