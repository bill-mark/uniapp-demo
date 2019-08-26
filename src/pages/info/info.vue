<template>
	<view>
		
	</view>
</template>

<script>
	export default{
        onLoad(e){
          console.log('info')
          console.log(e)
          uni.request({
          	url:'https://unidemo.dcloud.net.cn/api/news/36kr/'+e.newsid,
          	method:'GET',
          	data:{}
          })
        }
	}
</script>

<style>
	
</style>