<template>
    <div class="common-container">
        <div class="fish-container left" :class="bg">
            <div class="title" :class="bg+'-title'">
                {{title}}
            </div>
        </div>
        <div class="left">
            <el-form label-width="110px">
                <el-form-item label="图片">
                    <el-select v-model="bg" placeholder="请选择">
                        <el-option
                                v-for="item in sex"
                                :key="item.value"
                                :label="item.label"
                                :value="item.value">
                        </el-option>
                    </el-select>
                </el-form-item>
                <el-form-item label="文字">
                    <el-input v-model="title"></el-input>
                </el-form-item>
            </el-form>
        </div>
    </div>
</template>

<script>
    export default {
        name: "fish",
        data() {
            return {
                title: '',
                bg: 'fish1',
                sex: [
                    {label: '摸鱼鸭', value: 'fish1',},
                    {label: '蘑菇头摸鱼', value: 'fish2',}
                ]
            }
        }
    }
</script>

<style scoped lang="less">
    .title {
        color: #686868;
        font-weight: bolder;
        letter-spacing: 2px;
    }
    .fish-container {
        width: 550px;
        height: 450px;
        position: relative;
    }
    .fish1{
        background: url("../assets/fish/fh1.jpg");
        background-size: 100% 100%;
    }
    .fish2{
        background: url("../assets/fish/fh2.jpg") no-repeat center center;
        background-size: 80% 100%;
    }
    .fish1-title{
        margin-top: 65px;
        font-size: 42px;
    }
    .fish2-title{
        position: absolute;
        width: 100%;
        text-align: center;
        bottom: 0;
        font-size: 45px;
        font-weight: bolder;
        color: black;
    }

    .mg-left {
        margin-left: 10px;
    }
</style>
