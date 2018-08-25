<template>
    <div class="p-relative">
        <p class="container x92 y40 ym10 b-border t-pointer x-between" @click="showProduct=!showProduct">
            <span>{{selectProduct||'选择产品'}}</span>
            <span>
                <i class="ym5 fa fa-sort" aria-hidden="true"></i>
            </span>
        </p>
        <v-block :show="showProduct" :size="'x92 y240'">
            <div slot="block">
                <ul>
                    <li class="y30 t-pointer" :class="{'t-current':item === selectProduct}" v-for="(item,index) in options" :key="index" @click="checkProduct(item)">{{item}}</li>
                </ul>
            </div>
        </v-block>
    </div>
</template>
<script>
export default {
    data() {
        return {
            showProduct: 0,
            selectProduct: undefined,

            options: [
                'aaa',
                'bbb',
                'ccc',
                'eee',
                'fff',
                'xxx',
                'yyy',
                'zzz'
            ]
        }
    },
    methods: {
        checkProduct(item) {
            this.selectProduct = item
            this.showProduct = 0
        }
    }
}
</script>

<style lang="css" scoped>
</style>

