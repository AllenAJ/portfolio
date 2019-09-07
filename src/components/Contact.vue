<template>
    <v-app class="contact">
        <v-container>
            <v-row>
                <v-col cols="md-4">
                    <h1 :style="config.contactTitleStyle">{{ config.contactTitle }}</h1>
                </v-col>
            </v-row>
            <v-row>
                <v-col cols="md-4">
                    <h1 :style="config.authorStyle">{{ config.author }}</h1>
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

    .contact{
        background: #7075ff;
        padding-top: 40px;
        padding-bottom: 40px;
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

    .about-bttns{
        margin-left: 20px;
        margin-right: 20px;
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