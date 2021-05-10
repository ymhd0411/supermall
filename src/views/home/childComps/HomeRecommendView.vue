<template>
    <div class="recommend">
        <div v-for="item in recommends" :key='item.link' class="recommend-item">
            <a :href="item.link"><img :src="item.image" alt="">
                <div>{{item.title}}</div>
            </a>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'HomeRecommendView',
        props: {
            recommends: {
                typeof: Array,
                default() {
                    return []
                }
            }
        }

    }
</script>

<style scoped>
.recommend {
    display: flex;
    width: 100%;
    text-align: center;
    font-size: 12px;
    padding: 10px 0 20px;
    border-bottom: 10px solid #eee;
}
.recommend-item {
flex: 1;
}
.recommend img {
    width: 80%;
    margin-top: 10px;
}
</style>