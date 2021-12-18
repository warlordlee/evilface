<template>
    <div class="common-container">
        <div class="ms-container left" :class="bg">
            <div class="title" :class="'ms5'===bg?'ms5-title':''">
                {{title}}
            </div>
            <div class="book" v-if="bg === 'ms1'">
                {{book}}
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
                <el-form-item label="书名" v-if="bg === 'ms1'">
                    <el-input v-model="book"  maxlength="10"></el-input>
                </el-form-item>
            </el-form>
        </div>
    </div>
</template>

<script>
    export default {
        name: "ms",
        data() {
            return {
                title: '',
                bg: 'ms1',
                book: '',
                sex: [
                    {label: '看书蘑菇头', value: 'ms1',},
                    {label: '甲方蘑菇头', value: 'ms2',},
                    {label: '开车蘑菇头', value: 'ms3',},
                    {label: '数钱蘑菇头', value: 'ms4',},
                    {label: '经典蘑菇头', value: 'ms5',},
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
        top: 350px;
    }
    .ms5-title{
        top: 300px;
    }

    .ms-container {
        width: 500px;
        height: 450px;
        position: relative;
    }

    .ms1 {
        background: url("../assets/ms/ms2.jpg") center center no-repeat;
        background-size: 80% 80%;
    }

    .ms2 {
        background: url("../assets/ms/ms1.jpg") center center no-repeat;
        background-size: 70% 80%;
    }

    .ms3 {
        background: url("../assets/ms/ms3.jpg") center center no-repeat;
        background-size: 75% 80%;
    }

    .ms4 {
        background: url("../assets/ms/ms4.jpg") center center no-repeat;
        background-size: 75% 80%;
    }

    .ms5 {
        background: url("../assets/ms/ms5.jpg") center center no-repeat;
        background-size: 85% 90%;
    }

    .mg-left {
        margin-left: 10px;
    }
    @reg: -6deg;
    .book{
        position: absolute;
        top: 242px;
        left: 195px;
        color: white;
        font-weight: bold;
        font-size: 14px;
        width: 80px;
        transform:rotate(@reg);
        -ms-transform:rotate(@reg); 	/* IE 9 */
        -moz-transform:rotate(@reg); 	/* Firefox */
        -webkit-transform:rotate(@reg); /* Safari 和 Chrome */
        -o-transform:rotate(@reg); 	/* Opera */
    }
</style>
