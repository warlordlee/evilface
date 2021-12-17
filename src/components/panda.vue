<template>
    <div class="common-container">
        <div class="panda-container left" :class="bg">
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
        name: "panda",
        data() {
            return {
                title: '',
                bg: 'panda1',
                sex: [
                    {label: '对讲机熊猫', value: 'panda1',},
                    {label: 'pose熊猫', value: 'panda2',},
                    {label: '抽烟熊猫', value: 'panda3',}
                ]
            }
        }
    }
</script>

<style scoped lang="less">
    .title {
        font-weight: bolder;
        letter-spacing: 2px;
        position: absolute;
        width: 100%;
        text-align: center;
        font-size: 55px;
        color: black;
    }
    .panda-container {
        width: 500px;
        height: 450px;
        position: relative;
    }
    .panda1{
        background: url("../assets/panda/pd1.png");
        background-size: 100% 100%;
    }
    .panda2{
        background: url("../assets/panda/pd2.gif") center center no-repeat;
        background-size: 90% 80%;
    }
    .panda3{
        background: url("../assets/panda/pd3.gif") center center no-repeat;
        background-size: 100% 80%;
    }
    .panda1-title{
        top: 350px;
    }
    .panda2-title{
        top: 320px;
    }
    .panda3-title{
        top: 315px;
    }
    .mg-left {
        margin-left: 10px;
    }
</style>
