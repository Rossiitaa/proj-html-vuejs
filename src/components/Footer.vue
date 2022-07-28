<template>
    <footer>
        <div id="footer" class="row d-flex justify-content-between mx-auto">

            <div id="footer-top" class="d-flex flex-column justify-content-start mx-auto">
                <div class="footer-content d-flex justify-content-center gap-5 ms-5">

                    <div class="about-us d-flex flex-column text-start ms-5">
                        <h6 class="mb-4">
                            ABOUT US
                        </h6>
                        <p class="mb-4">
                            Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.
                        </p>

                        <a href="#" class="d-flex gap-3 fs-4">
                            <font-awesome-icon :icon="['fab', 'facebook-square']" />
                            <font-awesome-icon :icon="['fab', 'twitter-square']" />
                            <font-awesome-icon :icon="['fab', 'linkedin']" />
                            <font-awesome-icon :icon="['fab', 'google-plus']" />
                            <font-awesome-icon :icon="['fab', 'pinterest-square']" />
                            <font-awesome-icon :icon="['fab', 'flickr']" />
                        </a>
                    </div>
                    
                    <div class="recent-news d-flex flex-column align-items-start text-start">
                        <ul class="p-0">
                            <li>
                                <h6 class="mb-4">
                                    RECENT NEWS
                                </h6>
                            </li>
                            <li class="mb-3">
                                <a href="#">
                                    <font-awesome-icon icon="fas fa-angle-right"
                                    class="me-2" />
                                    SEM PORTA MOLLIS PARTURIENT
                                </a>
                            </li>
                            <li class="mb-3">
                                <a href="#">
                                    <font-awesome-icon icon="fas fa-angle-right"
                                    class="me-2" />
                                    NULLAM LOREM MATTIS PURUS
                                </a>
                            </li>
                            <li class="mb-3">
                                <a href="#">
                                    <font-awesome-icon icon="fas fa-angle-right"
                                    class="me-2" />
                                    NIBH SEM SIT ULLAMCORPER
                                </a>
                            </li>
                            <li class="mb-3">
                                <a href="#">
                                    <font-awesome-icon icon="fas fa-angle-right"
                                    class="me-2" />
                                    DONEC LUCTUS IMPERDIET
                                </a>
                            </li>
                            <li>
                                <a href="#">
                                    <font-awesome-icon icon="fas fa-angle-right"
                                    class="me-2" />
                                    MAGNA PARS STUDIORUM
                                </a>
                            </li>
                        </ul>
                    </div>

                    <div class="get-your-seat d-flex flex-column text-start">
                        <h6 class="mb-4">
                            GET YOUR SEAT!
                        </h6>
                        <p class="mb-4">
                            Book for your seat before it's too rate. We provide variety of ticket options.
                        </p>

                        <div id="check-tickets">
                            <button class="p-3 px-4">
                                CHECK OUT TICKETS!
                            </button>
                        </div>
                    </div>

                    <div class="gallery-image d-flex flex-column text-start" v-for="(gallery, index) in listGallery" :key="index">
                        <h6 class="mb-4">
                            GALLERY FROM LAST YEAR
                        </h6>

                        <div class="single-image d-flex flex-wrap gap-2">
                            <img :src="gallery.tile1" alt="cups of coffee">
                            <img :src="gallery.tile2" alt="conference with woman">
                            <img :src="gallery.tile3" alt="desk with person">
                            <img :src="gallery.tile4" alt="conference with man">
                            <img :src="gallery.tile5" alt="coffee meeting">
                            <img :src="gallery.tile6" alt="rockable cards">
                            <img :src="gallery.tile7" alt="personal items">
                            <img :src="gallery.tile8" alt="desk setup">
                            <img :src="gallery.tile9" alt="woman on the phone">
                            <img :src="gallery.tile10" alt="rockable cards 2">
                            <img :src="gallery.tile11" alt="sea">
                            <img :src="gallery.tile12" alt="clothes">
                        </div>
                    </div>
                </div>
            </div>

            <div id="footer-bottom" class="d-flex justify-content-center align-items-center">

                <div id="text-footer-bottom" class="d-flex justify-content-around">
                    <span>
                        &copy; Copyright GooLayers, All Right Reserved
                    </span>

                    <span>
                        <a href="#">About Us</a> | <a href="#">Accommodation</a> | <a href="#">Call For Paper</a> | <a href="#">Contatct Us</a>
                    </span>
                </div>

            </div>
        </div>
    </footer>
</template>

<script>
export default {
name: 'Footer',
    data() {
        return {
            listGallery: [
                {
                    tile1: require("../assets/images/photodune-7770665-two-white-coffee-mug-with-diy-decoration-o (1).jpg"),
                    tile2: require("../assets/images/photodune-8523683-speaker-at-business-convention-and-present.jpg"),
                    tile3: require("../assets/images/photodune-6745579-modern-creative-man-relaxing-on-workspace-.jpg"),
                    tile4: require("../assets/images/photodune-8522811-speaker-at-business-conference-and-present (1).jpg"),
                    tile5: require("../assets/images/photodune-8797753-multiethnic-people-with-startup-business-t (1).jpg"),
                    tile6: require("../assets/images/card04-150x150.jpg"),
                    tile7: require("../assets/images/photodune-6745606-man-wristwatch-calendar-key-and-glasses-on.jpg"),
                    tile8: require("../assets/images/photodune-6745585-modern-creative-workspace-m-150x150.jpg"),
                    tile9: require("../assets/images/6426608875_186070f8ca_o-150x150.jpg"),
                    tile10: require("../assets/images/card01-150x150.jpg"),
                    tile11: require("../assets/images/13349065283_64d09b067c_o-150x150.jpg"),
                    tile12: require("../assets/images/photodune-8795110-overhead-of-essentials-denim-clothes-m-150.jpg")
                }
            ]
        }
    }
}
</script>

<style lang='scss' scoped>
#footer {
    width: 100%;
    height: 47vh;
    background: #272727;

    #footer-top {
        width: 100%;
        height: 33vh;
        margin-top: 4rem;

        h6 {
            color: #fff;
            font-size: 12px;
            font-weight: 700;
            letter-spacing: 3px;
        }

        p {
            color: #adadad;
            font-size: 13px;
        }

        .about-us {
            width: 12%;

            a {
                color: #ffffff;
            }
        }

        .recent-news {
            

            li {
                list-style-type: none;

                a {
                    text-decoration: none;
                    color: #878787;
                    font-size: 11px;
                }
            }
        }

        .get-your-seat {
            width: 13%;

            #check-tickets {

                button {
                    font-weight: 700;
                    font-size: 12px;
                    border-width: 0 0 3px 0;
                    border-color: #d92719;
                    background: #f72b0c;
                    color: #ffffff;
                }
            }
        }

        .gallery-image {
            width: 20%;

            .single-image {
                width: 80%;

                img {
                    max-width: 100%;
                    height: 6vh;
                }
            }
        }
    }
    #footer-bottom {
        height: calc(100% - 39vh);
        background: #171717;

        #text-footer-bottom {
            width: 80%;
            font-size: 13px;

            span {
                color: #4d4d4a;

                &:last-child {
                    color: #6c6a6b;
                }
            a {
                text-decoration: none;
                color: #4d4d4a;
                letter-spacing: 1px;
            }
            }
        }
    }
}
</style>