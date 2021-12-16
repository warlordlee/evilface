<template>
    <div class="main pad">
        <el-tabs v-model="activeName" @tab-click="handleClick">
            <el-tab-pane label="证件" name="first">
                <certificate></certificate>
            </el-tab-pane>
            <el-tab-pane label="熊猫头" name="second">

            </el-tab-pane>
            <el-tab-pane label="蘑菇人" name="third">

            </el-tab-pane>
        </el-tabs>
    </div>
</template>

<script>
    import certificate from "@/components/certificate";
    export default {
        name: "face",
        components:{
            certificate
        },
        data(){
            return{
                activeName:'first'
            }
        },
        methods:{
            handleClick(){

            }
        }
    }
</script>

<style scoped lang="less">
    .pad{
        padding: 30px 60px;
    }
</style>
