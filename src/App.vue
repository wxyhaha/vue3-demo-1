<template>
  <Button @click="open">hi</Button>
  <hr/>
  <Switch v-model:value="switchValue"/>
  <hr/>
  <Tabs v-model:selected="tabSelected">
    <Tab title="tab1">内容1</Tab>
    <Tab title="tab2">内容2</Tab>
  </Tabs>
</template>

<script>
// 'gulu-ui-2021' 是我下载的老师最终版代码编译上传的库
// 'gulu-ui-1' 是老师上传的库
// 'flash-shan-ui' 是我的库
import {Button,Switch,Dialog,openDialog,Tabs,Tab} from 'gulu-ui-2021'
import 'gulu-ui-2021/dist/lib/gulu.css'

export default {
  name:'App',
  components: {Button,Switch,Dialog,Tabs,Tab},
  data(){
    return{
      switchValue:false,
      tabSelected:'tab1'
    }
  },
  methods:{
    open(){
      openDialog({title:'标题',content:'内容'})
    }
  }
};
</script>