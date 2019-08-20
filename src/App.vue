<template>
    <div class="app-trip">
        <h1 class="title">{{title}}</h1>
        <Countdown :date="dateBegin"></Countdown>
    </div>
</template>

<script>
    import Countdown from './components/Countdown.vue';

    export default {
        name: 'Trip',
        components: {
            Countdown
        },
        data() {
            return {
                dateBegin: "2020-09-11 06:00:00",
                title: "#Pérou2020",
            }
        },
    }
</script>

<style lang="scss">
    @import "../src/assets/font/trip.css";

    .app-trip {
        align-items: center;
        bottom: 0;
        background-color: #34495e;
        left: 0;
        position: absolute;
        right: 0;
        top: 0;
    }

    .countdown {
        display: flex;
        justify-content: center;
    }

    .block {
        display: flex;
        flex-direction: column;
        margin: 30px;
        @media all and (max-width: 599px) and (min-width: 50px) {
            margin: 10px;
        }
    }

    .text {
        color: #1abc9c;
        font-size: 25px;
        font-family: 'Roboto Condensed', serif;
        font-weight: 35;
        margin-top: 10px;
        margin-bottom: 10px;
        text-align: center;
        @media all and (max-width: 599px) and (min-width: 50px) {
            font-size: 15px;
        }
    }

    .digit {
        color: #ecf0f1;
        font-size: 120px;
        font-weight: 100;
        font-family: 'Roboto', serif;
        margin: 10px;
        text-align: center;
        @media all and (max-width: 599px) and (min-width: 50px) {
            font-size: 45px;
            margin: 5px;
        }
    }

    .title {
        color: #ecf0f1;
        font-size: 5em;
        font-weight: 100;
        font-family: 'Roboto', serif;
        margin: 50px;
        text-align: center;
        @media all and (max-width: 599px) and (min-width: 50px) {
            margin: 30px;
            margin-top: 50px;
            font-size: 3.5em;
        }
    }

</style>
