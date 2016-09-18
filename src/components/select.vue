
<template>
	<!--<div>
		<swiper  :height="sehe" :list="list" :loop=true auto></swiper>
	</div>-->
	
	<div class="lis" >
		<ul>
			
			<li v-link="{path:'/playsong', query: {hash:i.hash,singername:i.singername,songname:i.songname}}" v-for="i in musicdata">
				<i class="icon"> 	</i>
				<h6 >{{i.songname}}</h6>
				<span>{{i.singername}}</span>
			</li>
			
		</ul>
	
	</div>
		
	
</template>

<script>
//import Swiper from 'vux/src/components/swiper'
//import Scroller from 'vux/src/components/scroller'

//import Songlist from './songlist'

export default {
  components: {
	
	
  },
   data: function () {
  
    return {
    	pullupconfig:{
		    content: 'Pull Up To Refresh',
		  pullUpHeight: 800,
		  height: 800,
		  autoRefresh: false,
		  downContent: 'Release To Refresh',
		  upContent: 'Pull Up To Refresh',
		  loadingContent: '加载中...',
		  clsPrefix: 'xs-plugin-pullup-'
    	},
    	musicdata:[
				{
				"filename": "Dj Okawari - Flower Dance - 钢琴版纯音乐",
				"songname": "Flower Dance",
				"m4afilesize": 1097671,
				"filesize": 4301086,
				"bitrate": 128,
				"othername": "钢琴版纯音乐",
				"isnew": 0,
				"duration": 268,
				"hash": "e8f7a857d339ed8604d5b99a37d6a5a7",
				"singername": "Dj Okawari",
				"extname": "mp3",
				"album_name": "Libyus Music Sound History 2004-2010 Mixed by DJ OKAWARI"
				},
				{
				"filename": "Dj Okawari - Luv Letter - 钢琴版纯音乐",
				"songname": "Luv Letter",
				"m4afilesize": 1139791,
				"filesize": 4326294,
				"bitrate": 128,
				"othername": "钢琴版纯音乐",
				"isnew": 0,
				"duration": 270,
				"hash": "166ccc460414603cc50a4418e5ce4363",
				"singername": "Dj Okawari",
				"extname": "mp3",
				"album_name": "Euphony"
				},
				{
				"filename": "李宗盛 - 给自己的歌 - 2010台北纵贯线终点演唱会",
				"songname": "给自己的歌",
				"m4afilesize": 1163851,
				"filesize": 4444132,
				"bitrate": 128,
				"othername": "2010台北纵贯线终点演唱会",
				"isnew": 0,
				"duration": 277,
				"hash": "cee5848662ce9479a86f8d644e985504",
				"singername": "李宗盛",
				"extname": "mp3",
				"album_name": ""
				},
				{
				"filename": "李宗盛 - 山丘 (Live)",
				"songname": "山丘 (Live)",
				"m4afilesize": 1523447,
				"filesize": 5943625,
				"bitrate": 128,
				"othername": "",
				"isnew": 0,
				"duration": 371,
				"hash": "6afc4311ff9bc531c603c1a3bdb136bd",
				"singername": "李宗盛",
				"extname": "mp3",
				"album_name": ""
				},
				{
				"fileHead": 100,
				"q": 0,
				"fileSize": 2690318,
				"hash": "0C4AD687E2BD89177DC2AEB0DC2C6418",
				"topic_remark": "",
				"songname": "旧的童年",
				"singername": "高晓松",
				"url": "http://song.music.response.itmf.cn/23807a53c12268a15b0fc46868a5a97a/57d91b89/G003/M03/1F/10/o4YBAFUBOHGAHGQ4ACkNDgKkfws160.mp3",
				"fileName": "高晓松 - 旧的童年",
				"topic_url": "",
				"req_hash": "0C4AD687E2BD89177DC2AEB0DC2C6418",
				"bitRate": 128,
				"extName": "mp3",
				"timeLength": 167
				},
				{
				"filename": "高晓松 - 模范情书",
				"songname": "模范情书",
				"m4afilesize": 1069260,
				"filesize": 6312594,
				"bitrate": 128,
				"othername": "",
				"isnew": 0,
				"duration": 395,
				"hash": "cd25b1187b6b109089778de54489fe48",
				"singername": "高晓松",
				"extname": "mp3",
				"album_name": ""
				},
				{"filename":"Richard Sanderson - Reality【《初吻》原声带】",
				"songname":"Reality",
				"m4afilesize":1200116,
				"filesize":4633167,
				"bitrate":128,
				"album_name":"Remember the Words",
				"isnew":0,"duration":288,
				"singername":"Richard Sanderson",
				"extname":"mp3",
				"hash":"0bb59209f057e7ce2e5c758ceae3a348",
				"othername":""},
				{
				"filename": "徳永英明 - なごり雪【译名:残雪】",
				"songname": "なごり雪",
				"m4afilesize": 1237195,
				"filesize": 4733865,
				"bitrate": 128,
				"album_name": "HIDEAKI TOKUNAGA VOCALIST BOX(A)",
				"isnew": 0,
				"duration": 295,
				"singername": "徳永英明",
				"extname": "mp3",
				"hash": "25a7ac92785c8caa166437f5e0a94a4c",
				"othername": ""
				},
				{
				"filename": "徳永英明 - 恋におちて -Fall In Love-【译名:坠入恋河-Fall in Love-】",
				"songname": "恋におちて -Fall In Love-",
				"m4afilesize": 1382437,
				"filesize": 5267666,
				"bitrate": 128,
				"album_name": "HIDEAKI TOKUNAGA VOCALIST BOX(A)",
				"isnew": 0,
				"duration": 329,
				"singername": "徳永英明",
				"extname": "mp3",
				"hash": "ec926db2781774b9cfb081f176e04598",
				"othername": ""
				},
				{
				"filename": "徳永英明 - 駅【译名:车站】",
				"songname": "駅",
				"m4afilesize": 1185036,
				"filesize": 4512414,
				"bitrate": 128,
				"album_name": "HIDEAKI TOKUNAGA VOCALIST BOX(A)",
				"isnew": 0,
				"duration": 282,
				"singername": "徳永英明",
				"extname": "mp3",
				"hash": "26b90ea23a0ad6ec2773210523fedfb4",
				"othername": ""
				},
			],
    sehe:'1.5rem',
      list: [{
        url: '#',
        img: 'http://y.gtimg.cn/music/photo_new/T003R720x288M000001rxGT337UYwO.jpg?max_age=2592000',
        title: ''
      }, {
        url: '#',
        img: 'http://y.gtimg.cn/music/photo_new/T003R720x288M0000044RhzK0AVklU.jpg?max_age=2592000',
        title: ''
      }, {
        url: '#',
        img: 'http://y.gtimg.cn/music/photo_new/T003R720x288M000001jBJH14I90uD.jpg?max_age=2592000',
        title: ''
      },{
        url: '#',
        img: 'http://y.gtimg.cn/music/photo_new/T003R720x288M000002jVSob2ZJVW6.jpg?max_age=2592000',
        title: ''
      }
      ]
    }
  },
  		methods:{
			sel:function(){
				/*
				var se=this.val
				var vm=this
	          	var keyurl='/?s=周杰伦&size=20&page=1'
	           
	            this.$http({
	                method:'GET',
	                
	                url:'http://apis.baidu.com/geekery/music/query'+keyurl,
	               	headers: {apikey: 'f10cc71196d45d16a90bc9741c2fbe71'},
	                }).then(function(data){
	                	var d=JSON.parse(data.data)
	                	vm.musicdata=d.data.data
										console.log(vm.musicdata)
	               })
								 */
				
			}
		},
  	ready(){
  		 	this.sel()
  		 	
  	}
}

</script>
<style>

.lis ul{
		margin: 0;
		padding: 0;
		
	}
	.lis li{
		list-style: none;
		margin: 0;
		padding: 0;
		height: 55px;
		position: relative;
		padding-left: 56px;
		overflow: hidden;
		&:hover{
			background-color:#f4f4f4;
			color:#f4f4f4;
		}
		
	}
	.lis .icon{
		position: absolute;
		left: 18px;
		top: 18px;
		height: 20px;
		width: 22px;
		background-position: 0 0;
	}
	
	
	.lis .icon:after,.lis .icon{
		
		background-image: url('../assets/search_sprite.png');
		background-size:22px 30px ;
		background-repeat:no-repeat;
	}
	.lis h6{
		    margin: 10px 0 2px;
    line-height: 18px;
    font-size: 16px;
    font-weight: normal;
    color: #000;
   	overflow: hidden; 
	white-space: nowrap; 
	text-overflow: ellipsis;
	}
	.lis span{
		color: #808080;
		overflow: hidden; 
		white-space: nowrap; 
		text-overflow: ellipsis;
	}
	.lis li:hover{
		background-color:#f4f4f4;
	}
</style>



