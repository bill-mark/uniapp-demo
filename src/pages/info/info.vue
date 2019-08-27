<template>
	<view>
		<view>{{title}}</view>
	</view>
</template>

<script>
	export default{
		data(){
            return {
            	title:''
            }
		},
        onLoad(e){
          uni.showLoading({
          	title:"加载中. 888"
          }),
          uni.request({
          	url:'https://unidemo.dcloud.net.cn/api/news/36kr/'+e.newsid,
          	method:'GET',
          	data:{},
          	success:res=>{
          		//console.log(res)
          		this.title = res.data.title
          		uni.hideLoading()
          	}
          })
        }
	}
</script>

<style>
	
</style>