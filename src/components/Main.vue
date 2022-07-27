<template>
    <main>
        <div class="container-fluid p-0 m-0">
            <!-- informazioni azienda -->
            <div id="info-general" class="row d-flex justify-content-between align-items-center mx-auto">
                <div class="info-text col-12 d-flex flex-column justify-content-around position-relative" v-for="(info , index) in informations" :key="index">
                    <div class="d-flex fs-4">
                        <font-awesome-icon :icon="info.icon" class="mr-3" />
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

                    <div id="program-top" class="d-flex justify-content-between align-items-center mb-5">
                        <h1 class="align-self-start fw-bolder">
                            PROGRAM
                        </h1>
                        <p class="text-start me-5">
                            This conference run through all 4 days from 23 - 26 May 2016.
                            We also provide free lunch and coffee break in each day.
                        </p>
                        <a href="#" class="ps-5">
                            View Full Program
                        </a>
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

                        <div id="info-program" class="d-flex justify-content-around align-items-center">
                                <div id="info-left" class="d-flex flex-column align-items-center">
                                    <ul class="m-0 p-0">
                                        <li class="p-1">
                                            <a href="#">
                                                <font-awesome-icon icon="fas fa-clock"  class="me-2"/>
                                                <span>
                                                    09:00 - 10:30
                                                </span>
                                            </a>
                                        </li>
                                        <li class="p-1">
                                            <a href="#">
                                                <font-awesome-icon icon="fas fa-location-arrow" class="me-2"/>
                                                <span>
                                                    ROOM A
                                                </span>
                                            </a>
                                        </li>
                                        <li class="p-1">
                                            <a href="#">
                                                <font-awesome-icon icon="fas fa-user" class="me-2"/>
                                                <span>
                                                    LAURENCE FRANCIS
                                                </span>
                                            </a>
                                        </li>
                                    </ul>
                                </div>

                            <div class="info-right d-flex flex-column justify-content-around">
                                <h4>
                                    WELCOMING AND INTRODUCTION
                                </h4>
                                <p>
                                    Vestibulum id ligula porta felis euismod semper. Nullam quis risus eget urna mollis ornare vel eu leo. Donec
                                    ullamcorper nulla non metus auctor fringilla. Aenean lacinia bibendum nulla sed consectetur...
                                </p>
                                <img src="../assets/images/speaker-8-150x150.jpg" alt="speaker_img"
                                class="rounded-1">
                            </div>
                        </div> 
                    </div>
                </div>
            </div>    
            <!-- fine program -->

            <!-- map -->
            <div id="map" class="row">
                <div class="d-flex flex-wrap my-2 px-0 position-relative">
                    <div v-for="(map, index) in maps" :key="index">
                        <img :src="map.item" :alt="map.alt" class="">
                    </div>
                    <div class="position-absolute top-0 start-0 m-3 shadow-sm d-flex">
                        <a href="#">
                            <h5 class="p-2 fw-bold">
                                Map
                            </h5>
                        </a>
                        <a href="#">
                            <h5 class="p-2">
                                Satellite
                            </h5>
                        </a>
                    </div>
                    <span class="position-absolute bottom-0 end-0 pe-2" style="font-size: 12px">
                        Map data &#169;2020 Google 200 m Terms of Use Report a map error
                    </span>
                    <span class="position-absolute bottom-0 pe-2">
                        <img src="../assets/images/google4.png" alt="" style="width:10% height:10%">
                    </span>
                </div>
                
            </div>

            <!-- location -->
            <div id="location-bg" class="row m-0">
                <div class="d-flex flex-column justify-content-center gap-2 text-center">
                    <h1 class="fw-bold pb-4">
                        LOCATION
                    </h1>
                    <h2 class="fw-bold fs-4">
                        GD BUILDING, GRAND CONFERENCE ROOM
                    </h2>

                    <div>
                        <font-awesome-icon icon="fas fa-location-arrow" class="me-2" />
                        <span>
                            11 GD Building, River Mail, New york, USA 8879
                        </span>
                    </div>

                    <div class="mb-4">
                        <a href="#" id="check" class="text-decoration-none">
                            Check For Accommodations Here
                        </a>
                    </div>

                    <div class="d-flex justify-content-between pt-2 mx-auto border-top border-2" style="width: 24%">
                        <a href="#" style="color: #ffffff" class="text-decoration-none">
                            <font-awesome-icon icon="fas fa-phone" class="me-2" />
                                +1-112-222-3344
                        </a>
                        <a href="#" style="color: #ffffff" class="text-decoration-none">
                            <font-awesome-icon icon="fas fa-envelope" class="me-2" />
                                Contact@TheKeynoteTheme.com
                        </a>
                    </div>
                </div>
                
            </div>

            <!-- recent news -->
            <div id="news-section" class="row d-flex justify-content-around align-items-center">
                <div v-for="(news,index) in newsList" :key="index">
                    <img :src="news.img" :alt="news.alt" class="mb-4">
                        <ul>
                            <li>
                                <h6  class="mb-2">
                                    {{ news.date }}
                                </h6>
                            </li>
                            <li>
                                <h5 class="mb-4 fw-bold">
                                    {{ news.title }}
                                </h5>
                            </li>
                            <li>
                                <p class="mb-4">
                                    {{ news.text }}
                                </p>
                            </li>
                            <li>
                                <a href="#">
                                    <span>
                                        {{ news.urlText }}
                                    </span>
                                </a>
                            </li>
                        </ul>
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
        maps: [
            {
                item: require ("../assets/images/vt (17).png"),
                alt: "vt-17-map"
            },
            {
                item: require ("../assets/images/vt (11).png"),
                alt: "vt-17-map"
            },
            {
                item: require ("../assets/images/vt (1).png"),
                alt: "vt-17-map"
            },
            {
                item: require ("../assets/images/vt (5).png"),
                alt: "vt-17-map"
            },
            {
                item: require ("../assets/images/vt (4).png"),
                alt: "vt-17-map"
            },
            {
                item: require ("../assets/images/vt (9).png"),
                alt: "vt-17-map"
            },
            {
                item: require ("../assets/images/vt (20).png"),
                alt: "vt-17-map"
            },
            {
                item: require ("../assets/images/vt (13).png"),
                alt: "vt-17-map"
            },
            {
                item: require ("../assets/images/vt (12).png"),
                alt: "vt-17-map"
            },
            {
                item: require ("../assets/images/vt (2).png"),
                alt: "vt-17-map"
            },
            {
                item: require ("../assets/images/vt.png"),
                alt: "vt-17-map"
            },
            {
                item: require ("../assets/images/vt (3).png"),
                alt: "vt-17-map"
            },
            {
                item: require ("../assets/images/vt (15).png"),
                alt: "vt-17-map"
            },
            {
                item: require ("../assets/images/vt (18).png"),
                alt: "vt-17-map"
            },

        ],
        newsList: [
            {

            }
        ]
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
    width: 100%;
    height: 70vh;
    background: url(../assets/images/coutdown-bg1.jpg);
    background-size: contain;
    background-position: center;
    margin: 0;
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
    width: 100%;
    height: 55vh;
    background: #f3f3f3;
    margin: 0;
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
    margin: 0;
    #all-program {
        width: 60%;
        #program-top {
            p {
                width: 45%;
                font-size: 15px;
                opacity: 0.6;
            }
            a {
                font-size: 17px;
                color: #f72b0c;
                text-decoration: none;
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
            #info-program {
                height: 30vh;
                background: #f6f6f6;
                #info-left {
                    width: 49%;
                    height: 22vh;
                    ul {
                        width: 70%;
                        li {
                            padding: 20px;
                            list-style-type: none;
                            a {
                                color: #868686;
                                text-decoration: none;
                                font-size: 12px;
                                
                                &:hover span {
                                    color: #f72b0c;
                                }
                            }
                        }
                    }
                }
                .info-right {
                    height: 25vh;

                    h4 {
                        letter-spacing: 2px;
                    }
                    p {
                        color: #868686;
                        opacity: 0.8;
                    }
                    img {
                        width: 6%;
                    }
                }
            }
        }
            
    }
}

/* map */
#map {
    width: 100%;
    margin: 0;
    img {
        width: 100%;
        height: 271.7px;
    }
    span {
        img {
            width: 100%;
            height: 100%;
        }
    }
}

/* location */
#location-bg {
    width: 100%;
    height: 45vh;
    background: url(../assets/images/location-bg.jpg);
    background-position: center;
    color: #fff;
        h1, h2 {
            letter-spacing: 5px;
        }
        #check {
            color: #f72a0c;
        }
}
</style>