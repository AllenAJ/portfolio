<template>
    <v-app class="white home">
        <v-container fluid>
            <v-row>
                <v-col cols="md4 xs6">
                    <center>
                        <v-avatar size="250">
                            <v-img src="../assets/img.jpg">
                            </v-img>
                        </v-avatar>
                    </center>
                </v-col>
                <v-col cols="md6 xs4">
                    <br><br>
                    <h1 :style="config.nameStyle">{{ config.name }}</h1>
                    <!-- <hr /> -->
                    <br>
                    <p class="headline">{{ config.tagline }}</p>
                    <div class="icon-row">
                        <span class="icon-holder" v-for="(item,i) in config.socials" :key="i">
                            <v-tooltip bottom>
                                <template v-slot:activator="{ on }">
                                    <v-btn color="#15171c" dark v-on="on" text icon :href="item.link" target="_blank" slot="activator">
                                        <v-icon>{{item.icon}}</v-icon>
                                    </v-btn>
                                </template>
                                <span>{{ item.name }}</span>
                            </v-tooltip>
                        </span>
                    </div>
                </v-col>
            </v-row>
        </v-container>
    </v-app>
</template>
<style scoped>
/* 
    hr{
        outline: none;
        border: 0;
        width: 250px;
        height: 2px;
        background: #15171c;
    } */

    .home{
        padding-top: 64px;
        padding-bottom: 64px;
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

    .icon-row{
        margin-top: 12px;
    }

    .icon-holder{
        padding-right: 12px;
    }

</style>
<script>
import config from '../conf/data.json';
export default {
    data() {
        return {
            config: config
        }
    },
};
</script>
