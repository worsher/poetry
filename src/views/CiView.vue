<template>
    <div class="ci">
        <div class="title">{{ci.rhythmic}}</div>
        <div class="author">{{ci.author}}</div>
        <div class="content">
            <div v-for="(item , index) in ci.paragraphs"
            class="line" 
            :key="index">
                {{item}}
            </div>
        </div>
    </div>	
</template>

<script type="text/javascript">
    import ci01 from "chinese-poetry/chinese-poetry/ci/ci.song.1000.json"
    let length = ci01.length
	export default {
		name : "ci-view",
        data (){
            return {
                ci : ci01[_.random(0 , length)]
            }
        }
	};
</script>

<style lang="scss" scoped="">
    .ci{
        min-width : 280px;
        margin : auto;
        margin-top : 10px;
        .title {
            font-size : 24px;
            font-weight : bold;
        }
        .author{
            width : 280px;
            text-align : right;
            font-weight : 600;
            margin : auto;
        }
        .content {
            font-size : 18px;
            .line {
                height : 30px;
            }
        }
    }
    
</style>