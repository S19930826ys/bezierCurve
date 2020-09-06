<template>
<div class="bezier">
    <div class="bezierTitle">bezier</div>
    <div class="bezierCtrlList">
        <!-- 选择曲线 -->
        <div class="chioceCurveBox">
            <select name="chioceCurve" id="chioceCurve">
                <option value="val.value" :key="key" v-for="(val,key) in curveList">{{val.name}}</option>
            </select>
        </div>
        <!-- 输入起点终点，控制点 -->
        <div class="inputPointBox">
            <ul class="pointList">
                <li class="point">
                    <input type="text" v-model="startPoint " />
                </li>
                <li class="ctrlPoint point">
                    <input type="text" v-model="startPoint " />
                </li>
                <li class="endPoint point">
                    <input type="text" v-model="startPoint " />
                </li>
            </ul>
        </div>
    </div>
    <div class="bezierCureBox">
        <svg>
            <path />
        </svg>
    </div>
</div>
</template>

<script>
export default {
    name: "bezierCurve",
    props: {
        msg: String,
    },
    data: function () {
        return {
            curveList: [{
                    name: "一次贝塞尔曲线",
                    value: "first",
                },
                {
                    name: "二次贝塞尔曲线",
                    value: "two",
                },
                {
                    name: "三次贝塞尔曲线",
                    value: "three",
                },
            ],
        };
    },
};
</script>

<style scoped>
.bezierTitle {
    font-size: 30px;
    color: #f00;
}
</style>
