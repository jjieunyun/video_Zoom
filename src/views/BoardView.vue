<template>
    <div class="board">
        <v-main>
        <h1>게시글 목록입니다</h1>
            <a v-for="n in num" :key="n">
                <router-link :to="`/board/${n}`">{{n}}</router-link>  | 
            </a>

            <!--위에 작성한 router-link의 컴포넌트가 보임-->
            <router-view></router-view>
        </v-main>
    </div>
</template>

<script>

export default {
    name: 'BoardView',
    data () {
        return {
            num : 10
        }
    }

}
</script>