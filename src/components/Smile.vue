<template>
    <div class="smile">
        <div class="logo"></div>
        <div class="main">
            <div class="tips">
                <div class="title"><img src="../assets/huodongzhuti.png"></div>
                <p>晒出萌新照，为班级集赞</p>
            </div>
            <div class="tips">
                <div class="title"><img src="../assets/cangyuduixiang.png"></div>
                <p>2018级新生</p>
            </div>
            <div class="tips">
                <div class="title"><img src="../assets/huodongshijian.png"></div>
                <p>即将启动，敬请期待</p>
            </div>
            <div class="tips">
                <div class="title"><img src="../assets/cangyufangshi.png"></div>
                <p class="pppx">关注微信公众号重邮小帮手，进入“线上互动”，点击“最美班级墙”，即可上传照片或进行点赞。</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    mounted() {
        document.querySelector('.tab').style.height = '1100px'
        document.querySelector('.activity').style.maxHeight = '1350px'
    },
    beforeDestroy() {
        document.querySelector('.tab').style.height = '1500px'
        document.querySelector('.activity').style.maxHeight = '1725px'
    }
}
</script>


<style lang="less" scoped>
    .smile {
        width: 832px;
        height: 1227px;
        padding: 4px 75px 60px 91px;
    }
    .logo {
        width: 826px;
        height: 460px;
        background: url('../assets/smile.jpg') no-repeat;
        background-size: 100% 100%;
        border: solid 4.5px #432a92;
    }
    .main {
        width: 90%;
        height: 190px;
        background: #d5fbff;
        margin-top: 40px;
        border: solid 4.5px #432a92;
        padding: 40px 5%;
    }
    .tips {
        width: 100%;
        height: 45px;
        display: flex;
        align-items: center;
        p {
            line-height: 20px;
            padding: 0 30px;
            font-size: 16px;
            color: #4c7ac3;
        }
    }
    .pppx {
        margin-top: 30px;
    }
    .title {
        img {
            width: 100px;
        }
    }
</style>
