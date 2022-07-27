<template>
    <main>
        <div class="container-fluid">
            <!-- informazioni azienda -->
            <div id="info-general" class="row d-flex justify-content-between align-items-center mx-auto">
                <div class="info-text col-12 d-flex flex-column justify-content-around position-relative" v-for="(info , index) in informations" :key="index">
                    <div class="d-flex fs-4">
                        <font-awesome-icon :icon="['fas', 'fa-trophy']" class="mr-3" />
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
            <!-- fine informazioni azienda -->

            <!-- countdown -->
            <div id="countdown" class="row d-flex align-items-center">
                <div id="count-card" class="d-flex flex-column justify-content-around">
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
                    <div id="sub-update">
                        <input type="text" placeholder="Please fill your email"
                        class="p-3 mx-3">
                        <button class="p-3 px-4">
                            SUBSCRIBE
                        </button>
                    </div>
                </div>
            </div>
            <!-- fine countdown -->
            <!-- speakers -->
            <div id="speakers-section" class="row d-flex flex-column justify-content-center">

                <div id="speakers-team" class="d-flex flex-wrap mx-auto">
                    <div id="navigation" class="d-flex justify-content-between align-items-center mb-5">
                        <h2 class="fw-bold fs-1">
                            SPEAKERS
                        </h2>

                        <div id="arrow-section-speaker" class="d-flex gap-1">
                            <button href="#" class="px-3 py-2">
                                <font-awesome-icon icon="fas fa-angle-left" />
                            </button>
                            <button href="#" class="btn px-3 py-2">
                                <font-awesome-icon icon="fas fa-angle-right" />
                            </button>
                        </div>
                    </div>

                    <div class="d-flex justify-content-between">
                        <div class="single-speaker d-flex flex-column justify-content-evenly text-center"
                        v-for="(speaker, index) in speakers" :key="index">
                            <img :src="speaker.img" :alt="speaker.alt">
                            <h5 class="mt-3 mb-0">
                                {{ speaker.name }}
                            </h5>
                            <span>
                                {{ speaker.job }}
                            </span>
                        </div>
                    </div>
                </div>
            </div>
            <!-- fine speakers -->

            <!-- program -->
            <div id="section-program" class="row d-flex justify-content-around align-items-center">

                <div id="all-program" class="d-flex flex-column justify-content-around">
                    <!-- introduzione -->
                    <div id="program-top" class="d-flex justify-content-between align-items-center mb-5">
                        <h1 class="align-self-start fw-bolder">
                            PROGRAM
                        </h1>
                        <p class="text-start me-5">
                            This conference run through all 4 days from 23 - 26 May 2016.
                            We also provide free lunch and coffee break in each day.
                        </p>
                        <span class="ps-5">
                            View Full Program
                        </span>
                    </div>

                    <div id="program-bottom" class="d-flex flex-column text-start">

                        <div class="d-flex">
                            <div class="single-day p-3"
                            v-for="(day, index) in days" :key="index">
                                <ul class="ms-2 my-0 p-0">
                                    <li>
                                        <a href="#">
                                            <h6 class="fw-bolder">
                                                {{ day.nDay }}
                                            </h6>
                                            <span>
                                                {{ day.date }}
                                            </span>
                                        </a>
                                    </li>
                                </ul>
                            </div>
                        </div>

                        
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
                text: "Donec id elit non mi porta gravida at eget me tus. Sed posuere consectetur estat lobo rtis. Cum sociis natoque.",
                url: "#",
                urlText: "Learn More"
            },
            {
                icon: "fas fa-bolt",
                title: "WHAT WE DO",
                text: "Donec id elit non mi porta gravida at eget me tus. Sed posuere consectetur estat lobo rtis. Cum sociis natoque.",
                url: "#",
                urlText: "Learn More"
            },
            {
                icon: "fas fa-question",
                title: "WHY US?",
                text: "Donec id elit non mi porta gravida at eget me tus. Sed posuere consectetur estat lobo rtis. Cum sociis natoque.",
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
        ],
        speakers: [
            {
                img: require ("../assets/images/speaker-6.jpg"),
                alt: "patrick spencer img",
                name: "PATRICK SPENCER",
                job: "S&P Analyzer"
            },
            {
                img: require("../assets/images/speaker-5.jpg"),
                alt: "janet_jones_img",
                name: "JANET JONES",
                job: "Newyork Post's GM"
            },
            {
                img: require("../assets/images/speaker-4.jpg"),
                alt: "michael dover img",
                name: "MICHAEL DOVER",
                job: "Starbuck's CEO"
            },
            {
                img: require("../assets/images/speaker-3.jpg"),
                alt: "angelina holy img",
                name: "ANGELINA HOLY",
                job: "Maxii's Manager"
            },
        ],
        days: [
            {
                nDay: "DAY 1",
                date: "23 May 2016"
            },
            {
                nDay: "DAY 2",
                date: "23 May 2030"
            },
            {
                nDay: "DAY 3",
                date: "24 May 2030"
            },
            {
                nDay: "DAY 4",
                date: "25 May 2030"
            },
            {
                nDay: "DAY 5",
                date: "26 May 2030"
            }, 
            {
                nDay: "",
                date: ""
            },
        ],
        }
    }
}
</script>

<style lang='scss' scoped>
/* informazioni azienda */
#info-general {
    width: 60%;
    height: 30vh;

    svg {
    position: absolute;
    top: -3px;
    left: -40px;
    color: #c6c1bd;
    }
    .info-text {
        width: 30%;
        height: 55%;
            
            h6 {
                color: #272727;
                letter-spacing: 2px;
            }
        }
        p {
            font-size: 0.9rem;
            color: #868686;
            margin-top: 1rem;
        }
        a {
            color: #f72b0c;
            font-style: italic;
        }
    }

/* countdown */
#countdown {
    height: 70vh;
    background: url(../assets/images/coutdown-bg1.jpg);
    background-size: contain;
    background-position: center;
    #count-card {
        height: 68%;
            h1 {
                font-size: 50px;
                font-weight: 700;
            }
            .card {
                background-color: #000;
                color: #fff;
            }
        }
        #sub-update {
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

                &:hover {
                    background-color: #f72a0c;
                    color: #fff;
                }
            }
        }
        h5 {
                display: flex;
                justify-content: center;
                align-items: center;
                font-size: 1.3rem;
                letter-spacing: 2px;
                margin: 0;
            }
    }

/* speakers */
    #speakers-section {
    height: 55vh;
    background: #f3f3f3;
    #speakers-team {
        width: 60%;
        height: 40vh;
            #navigation {
                width: 100%;
                    h2 {
                        letter-spacing: 2px;
                    }

                #arrow-section-speaker {
                    button {
                        font-size: 11px;
                        border: 0;
                        border-radius: 3px;
                        background: #f72b0c;
                        color: #fff;
                    }
                }
            }
            img {
                border-radius: 4px;
                width: 100%;
                height: 70%;
            }
            .single-speaker {
                span {
                    color: #868686;
                    font-size: 13px;
                }
                h5 {
                letter-spacing: 2px;
                font-size: 1rem;
            }
        }
    }
}

/* program */
#section-program {
    width: 100%;
    height: 70vh;
    #all-program {
        width: 60%;
        #program-top {
            p {
                width: 45%;
                font-size: 15px;
                opacity: 0.6;
            }
            span {
                font-size: 14px;
                color: #f72b0c;
            }
        }
        #program-bottom {
            background: #f72b0c;
            .single-day {
                width: 30%;     
                border-right: 1px solid #be281a;
                
                &:last-child {
                    border: 0;
                }
                &:hover {
                    background: #be281a;
                }
                
                li {
                    list-style-type: none;
                    a {
                        text-decoration: none;
                        color: #fff;
                        span {
                            font-size: 13px;
                        }
                    }
                }
            }
            
        }
            
    }
}
</style>