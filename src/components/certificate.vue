<template>
    <div class="common-container">
        <div class="certificate-container left">
            <div class="title">
                {{title}}
            </div>
            <div class="name">
                <span>{{name}}</span>
                <span class="mg-left" style="font-weight: bolder">{{0 ===mail?'女士':'先生'}}</span>
            </div>
            <div class="sub">
               <div> {{subTitle}}</div>
                <div> {{subTitle2}}</div>
                <div> {{subTitle3}}</div>
            </div>
            <div class="org">
                {{org}}
            </div>
            <div class="date">
                {{date}}
            </div>
        </div>
        <div class="left">
            <el-form label-width="110px">
                <el-form-item label="证书名称">
                    <el-input v-model="title"></el-input>
                </el-form-item>
                <el-form-item label="性别">
                    <el-select v-model="mail" placeholder="请选择">
                        <el-option
                                v-for="item in sex"
                                :key="item.value"
                                :label="item.label"
                                :value="item.value">
                        </el-option>
                    </el-select>
                </el-form-item>
                <el-form-item label="姓名">
                    <el-input v-model="name"></el-input>
                </el-form-item>
                <el-form-item label="描述">
                    <el-input v-model="subTitle"></el-input>
                </el-form-item>
                <el-form-item label="描述2">
                    <el-input v-model="subTitle2"></el-input>
                </el-form-item>
                <el-form-item label="描述3">
                    <el-input v-model="subTitle3"></el-input>
                </el-form-item>
            </el-form>
        </div>
    </div>
</template>

<script>
    export default {
        name: "certificate",
        data() {
            return {
                name: '',
                date:'2021年12月16日',
                title: '',
                subTitle: '鉴于您在职业生涯中惊人的优异表现,特此授予',
                subTitle2:'',
                subTitle3:'',
                mail: '',
                org:'英国皇家摸鱼协会杭州分会',
                sex: [{label: '先生', value: 1,}, {label: '女士', value: 0}]
            }
        }
    }
</script>

<style scoped lang="less">
    .certificate-container {
        width: 650px;
        height: 450px;
        background: url("../assets/card1.jpg");
        background-size: 100% 100%;
        position: relative;
    }

    .title {
        color: #686868;
        margin-top: 95px;
        font-size: 22px;
        font-weight: bolder;
        letter-spacing: 2px;
    }
    .name{
        position: absolute;
        top: 175px;
        left: 125px;
    }
    .sub{
        position: absolute;
        top: 205px;
        left: 145px;
        width: 425px;
        font-size: 13px;
        color: #9c958a;
        letter-spacing: 1px;
        text-align: left;
    }
    .date{
        position: absolute;
        right: 60px;
        bottom: 61px;
        font-size: 13px;
        font-weight: bold;
        color: #9c958a;
    }
    .org{
        position: absolute;
        right: 60px;
        bottom: 85px;
        font-size: 13px;
        font-weight: bold;
        color: #9c958a;
    }
    .mg-left{
        margin-left: 10px;
    }
</style>
