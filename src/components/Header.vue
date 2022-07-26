<template>
    <header>
        <div class="container d-flex justify-content-around  p-5">
            <img  src="../assets/images/logo.png" alt="">
            <nav>
                <ul>
                    <li v-for="(element, index) in elementList" :key="index" class="me-5 text-uppercase fw-bold">
                        <a href="#">{{ element.text }}</a>
                    </li>
                    <li><i class="fa-solid fa-magnifying-glass"></i></li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script>
export default {
data() {
    return {
        elementList: [
            {
            text: "home",
            },
            {
            text: "pages",
            },
            {
            text: "program",
            },
            {
            text: "tickets",
            },
            {
            text: "speakers",
            },
            {
            text: "papers",
            },
            {
            text: "blog",
            },
            {
            text: "shortcodes",
            },
            {
            text: "|",
            },
        ]
    }
}
}
</script>

<style lang='scss' scoped>


img {
    height: 1.3rem;
}

ul li {
    text-decoration: none;
    display: inline-block;
    font-size: 0.7rem;
    cursor: pointer;

    &:hover {
            border-bottom: 5px solid #f72a0c;
            color: #f72a0c;
        }
}

a {
    text-decoration: none;
    color: #8f8e95;

    &:hover {
            color: #f72a0c;
        }
}
</style>