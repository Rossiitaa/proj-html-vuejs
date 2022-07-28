<template>
    <header>
        <div class="container">
            <div class="d-flex justify-content-around p-5 pb-3">
                <img  src="../assets/images/logo.png" alt="">
                <nav>
                    <ul>
                        <li v-for="(element, index) in elementList" :key="index" class="me-4 text-uppercase fw-bold">
                            <a href="#" class="fw-bold">{{ element.text }}</a>
                        </li>
                        <li><i class="fa-solid fa-magnifying-glass"></i></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>
</template>

<script>
export default {
name: 'Header',
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
    height: 20px;
}

ul li {
    text-decoration: none;
    display: inline-block;
    font-size: 0.7rem;
    cursor: pointer;
    padding-bottom: 5px;

    &:hover {
            border-bottom: 3px solid #f72a0c;
            color: #f72a0c;
        }
}

a {
    text-decoration: none;
    color: #8f8e95;
    letter-spacing: 2px;
    font-size: 12px;

    &:hover {
            color: #f72a0c;
        }
}
</style>