<style>
#side{
    width:100%;
}
.pa{
    position:absolute;
    width:100%;
    height:100%;
}
#sideContent{
    background: rgba(0,0,0,.2) url(../assets/p.png);
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    text-align:center;
    color:white;
}
.guide-btn{
    padding:5px 15px;
    border:1px solid white;
    position:absolute;
    bottom:20px;
    width:80%;
    margin:0 auto;
    left:50%;
    transform:translate(-50%);
}
</style>
<template>
    <div id="side" >
        <video webkit-playsinline="" class="pa" autoplay loop muted id="sideVideo" src="http://media.jinzhe.net/themes/happy/side.mp4" style="left: 0;top: 0;">
        </video>
        <div class="pa" id="sideContent">
            <h1 class="guide-top">Vue-music</h1>
            <div class="guide-btn" v-link="{path:'/home/select'}">
                <h2>
                    欢迎使用
                </h2>
            </div>
        </div>
    </div>
	
</template>

<script >
	export default{
		data(){ 
			
			return {
				nav:[
					{
						tit:'推荐',
						url:'/home/select'
					},
					{
						tit:'喜欢',
						url:'/home/love'
					},
					{
						tit:'搜索',
						url:'/home/search'
					},
				]
				
			}
		},
		methods:{
			getIPAdress:function(){
				var vm=this
				  this.$http({
	                method:'GET',
	                url:'http://localhost:8081',
	               }).then(function(data){
	            	vm.adressIP=data.body
	              var ip=sessionStorage.getItem('adressIP')
	            	if(ip==''||ip==null){
	            		sessionStorage.setItem('adressIP',data.body)
	            		window.location.href="http://"+data.body+":6789"
	            	}
	               })

			}
		},
		ready:function(){
			this.getIPAdress()
		}
	}
</script>