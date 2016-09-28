<template>
    <div>
        <h1>Admin Page</h1>
        <p>A vue project.</p>
        <p>{{message}}</p>
        <el-radio class="radio" v-model="radio" label="1">备选项</el-radio>
        <el-radio class="radio" v-model="radio" label="2">备选项</el-radio>
        <div>
            <el-radio-group v-model="radio2">
                <el-radio :label="3">备选项</el-radio>
                <el-radio :label="6">备选项</el-radio>
                <el-radio :label="9">备选项</el-radio>
        </div>
        <div>
            <el-radio-group v-model="radio3">
                <el-radio-button label="上海"></el-radio-button>
                <el-radio-button label="北京"></el-radio-button>
                <el-radio-button label="广州" :disabled="false"></el-radio-button>
                <el-radio-button label="深圳"></el-radio-button>
            </el-radio-group>
        </div>

        </el-radio-group>
    </div>

</template>

<script>
    export default {
        name: 'app',
        data() {
            return {
                message: "hello vue 2.0",
                radio: '',
                radio2: '',
                radio3: ''
            }
        },
        created: function () {
            console.log("create");
        }
    };
</script>