<template>
    <v-app class="portfolio white">
        <v-container fluid>
            <v-row>
                <v-col cols="md-4 offset-md-4" class="text-center">
                    <h1 :style="config.nameStyle">{{ config.portfolioTitle }}</h1>
                </v-col>
            </v-row>
            <br>
            <v-row>
                <v-col cols="md-6 offset-md-3" class="text-center">
                    <p>
                        {{ config.portfolioDescription }}
                    </p>
                </v-col>
            </v-row>
            <br>
            <v-row>
                <v-col cols="md-6 offset-md-3" class="text-center">
                    <span v-for="(item, i) in config.hashtags" :key="i" :style="config.hashtagStyle">
                        #{{ item }} &nbsp;
                    </span>
                </v-col>
            </v-row>
        </v-container>
    </v-app>
</template>
<style scoped>

    /* hr{
        outline: none;
        border: 0;
        width: 200px;
        height: 2px;
        background: #15171c;
    } */

    .portfolio{
        padding-top: 90px;
        padding-bottom: 90px;
    }

     >>>.v-application--wrap{
        min-height: 0!important;
    }

    h1{
        font-weight: 800;
    }

    p{
        font-weight: 300!important;
    }

</style>
<script>
import config from '../../src/conf/data.json';
export default {
    data() {
        return {
            config: config
        }
    },
};
</script>