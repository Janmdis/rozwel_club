<template>
    <div class="container">
        <div class="cheader">
            <div class="authorImg"></div>
            <div class="author">
                <div>Rozwel</div>
                <div class="job">Web Programmer & Hibrid Player</div>
            </div>
            <div class="author">
                <div>Who am I?</div>
                <div class="intro">一个26岁热爱前端和新鲜事物的逗比-v-我会在这里分享我收集到的前端知识，你可以通过rozwel@sina.com联系我</div>
            </div>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.container {
    width: 100%;
    padding: 30px 0;
    background-color: orange;
    .cheader {
        width: 1170px;
        margin: 0 auto;
        display: flex;
        flex-flow: row nowrap;
        justify-content: space-between;
        align-items: center;
        .authorImg {
            min-height: 180px;
            min-width: 180px;
            border-radius: 50%;
            background: url('~assets/img/rozwel.jpg') no-repeat center;
        }
        .author {
            padding: 20px;
            color: white;
            font-size: 38px;
            display: flex;
            flex-flow: column nowrap;
            align-items: center;
            .job {
                font-size: 18px;
                margin-top: 20px;
            }
            .intro {
                font-size: 16px;
                margin-top: 20px;
            }
        }
    }
}
</style>
