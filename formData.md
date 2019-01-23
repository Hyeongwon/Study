## FormData

### Http
- Header

<!DOCTYPE html>
<!-- saved from url=(0029)https://sjh836.tistory.com/81 -->
<html lang="ko"><head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
<link rel="stylesheet" type="text/css" href="./HTTP 구조 (https, request, response, 주요 상태코드)_files/menubar.css"><!--[if lt IE 9]><script src="https://t1.daumcdn.net/tistory_admin/lib/jquery/jquery-1.12.4.min.js"></script><![endif]--><!--[if gte IE 9]>
<!--><script src="./HTTP 구조 (https, request, response, 주요 상태코드)_files/jquery-3.2.1.min.js.다운로드"></script><!--<![endif]-->
<script>var tjQuery = jQuery.noConflict(true);</script><style type="text/css">.tt_article_useless_p_margin p {padding-top:0 !important;padding-bottom:0 !important;margin-top:0 !important;margin-bottom:0 !important;}</style><meta name="referrer" content="always"><link rel="icon" href="https://t1.daumcdn.net/tistory_admin/static/top/favicon_0630.ico"><link rel="apple-touch-icon" href="https://i1.daumcdn.net/thumb/C180x180/?fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F215DB34E585E3EC136">
<link rel="apple-touch-icon" sizes="76x76" href="https://i1.daumcdn.net/thumb/C76x76/?fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F215DB34E585E3EC136">
<link rel="apple-touch-icon" sizes="120x120" href="https://i1.daumcdn.net/thumb/C120x120/?fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F215DB34E585E3EC136">
<link rel="apple-touch-icon" sizes="152x152" href="https://i1.daumcdn.net/thumb/C152x152/?fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F215DB34E585E3EC136"><meta name="description" content="1. 특징 인터넷상에서 데이터를 주고 받기 위한 서버/클라이언트 모델을 따르는 전송 프로토콜 애플리케이션 레벨의 프로토콜로 TCP/IP위에서 작동 클라이언트에서 요청(request)를 보내면 서버는 요청을 처리해서..">

<!-- BEGIN OPENGRAPH -->
<link rel="canonical" href="https://sjh836.tistory.com/81"><meta property="og:type" content="article"><meta property="og:url" content="https://sjh836.tistory.com/81"><meta property="og:site_name" content="빨간색코딩"><meta property="og:title" content="HTTP 구조 (https, request, response, 주요 상태코드)"><meta name="by" content="빨간색소년"><meta property="og:description" content="1. 특징 인터넷상에서 데이터를 주고 받기 위한 서버/클라이언트 모델을 따르는 전송 프로토콜 애플리케이션 레벨의 프로토콜로 TCP/IP위에서 작동 클라이언트에서 요청(request)를 보내면 서버는 요청을 처리해서.."><meta property="og:image" content="https://t1.daumcdn.net/cfile/tistory/216CF8395963739014"><meta property="article:section" content="IT 인터넷">
<!-- END OPENGRAPH -->



<!-- BEGIN TWITTERCARD -->
<meta name="twitter:card" content="summary_large_image"><meta name="twitter:site" content="@TISTORY"><meta name="twitter:title" content="HTTP 구조 (https, request, response, 주요 상태코드)"><meta name="twitter:description" content="1. 특징 인터넷상에서 데이터를 주고 받기 위한 서버/클라이언트 모델을 따르는 전송 프로토콜 애플리케이션 레벨의 프로토콜로 TCP/IP위에서 작동 클라이언트에서 요청(request)를 보내면 서버는 요청을 처리해서.."><meta property="twitter:image" content="https://t1.daumcdn.net/cfile/tistory/216CF8395963739014">
<!-- END TWITTERCARD -->



<!-- BEGIN DAUMAPP -->
<meta property="dg:plink" content="https://sjh836.tistory.com/81"><meta name="plink" content="https://sjh836.tistory.com/81"><meta name="title" content="HTTP 구조 (https, request, response, 주요 상태코드)"><meta name="article:media_name" content="빨간색코딩"><meta property="article:mobile_url" content="https://sjh836.tistory.com/m/81"><meta property="article:pc_url" content="https://sjh836.tistory.com/81"><meta property="article:mobile_view_url" content="https://sjh836.tistory.com/m/81"><meta property="article:pc_view_url" content="https://sjh836.tistory.com/81"><meta property="article:talk_channel_view_url" content="https://sjh836.tistory.com/m/81"><meta property="article:pc_service_home" content="https://www.tistory.com"><meta property="article:mobile_service_home" content="https://www.tistory.com/m"><meta property="article:txid" content="2548253_81"><meta property="article:published_time" content="2017-07-10T21:30:38+09:00"><meta property="og:regDate" content="20170710213038"><meta property="article:modified_time" content="2017-07-10T21:31:19+09:00">
<!-- END DAUMAPP -->



<!-- BEGIN STRUCTURED_DATA -->
<script type="application/ld+json">{"@context":"http:\/\/schema.org","@type":"BlogPosting","mainEntityOfPage":{"@id":"https:\/\/sjh836.tistory.com\/81"},"url":"https:\/\/sjh836.tistory.com\/81","headline":"HTTP \uad6c\uc870 (https, request, response, \uc8fc\uc694 \uc0c1\ud0dc\ucf54\ub4dc)","description":"1. \ud2b9\uc9d5 \uc778\ud130\ub137\uc0c1\uc5d0\uc11c \ub370\uc774\ud130\ub97c \uc8fc\uace0 \ubc1b\uae30 \uc704\ud55c \uc11c\ubc84\/\ud074\ub77c\uc774\uc5b8\ud2b8 \ubaa8\ub378\uc744 \ub530\ub974\ub294 \uc804\uc1a1 \ud504\ub85c\ud1a0\ucf5c \uc560\ud50c\ub9ac\ucf00\uc774\uc158 \ub808\ubca8\uc758 \ud504\ub85c\ud1a0\ucf5c\ub85c TCP\/IP\uc704\uc5d0\uc11c \uc791\ub3d9 \ud074\ub77c\uc774\uc5b8\ud2b8\uc5d0\uc11c \uc694\uccad(request)\ub97c \ubcf4\ub0b4\uba74 \uc11c\ubc84\ub294 \uc694\uccad\uc744 \ucc98\ub9ac\ud574\uc11c..","author":{"@type":"Person","name":"\ube68\uac04\uc0c9\uc18c\ub144"},"image":{"@type":"ImageObject","url":"https:\/\/t1.daumcdn.net\/cfile\/tistory\/216CF8395963739014","width":"800px","height":"800px"},"datePublished":"20170710T21:30:38+09:00","dateModified":"20170710T21:31:19+09:00","publisher":{"@type":"Organization","name":"TISTORY","logo":{"@type":"ImageObject","url":"https:\/\/t1.daumcdn.net\/tistory_admin\/static\/images\/openGraph\/opengraph.png","width":"800px","height":"800px"}}}</script>
<!-- END STRUCTURED_DATA -->


	<meta name="google-site-verification" content="J6gjC12ax3nj36QN4ZojFmxzna5TIKyxL2VPo_C8nTI">
	
	<meta name="viewport" content="user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0, width=device-width">
	<title>HTTP 구조 (https, request, response, 주요 상태코드)</title>
	<link rel="alternate" type="application/rss+xml" title="빨간색코딩" href="https://sjh836.tistory.com/rss">

	<link rel="stylesheet" href="./HTTP 구조 (https, request, response, 주요 상태코드)_files/style.css">
	<link rel="stylesheet" href="./HTTP 구조 (https, request, response, 주요 상태코드)_files/font.css">

	<!--[if lt IE 9]>
	<script src="//t1.daumcdn.net/tistory_admin/lib/jquery/jquery-1.12.4.min.js"></script>
	<![endif]-->
	<!--[if gte IE 9]><!-->
	<script src="./HTTP 구조 (https, request, response, 주요 상태코드)_files/jquery-3.2.1.min.js.다운로드"></script>
	<!--<![endif]-->

<style type="text/css">
		#daumSearchBox {
			height: 21px;
			background-image : url(//i1.daumcdn.net/imgsrc.search/search_all/show/tistory/plugin/bg_search2_2.gif);
			margin: 5px auto ;
			padding: 0;
		}
		#daumSearchBox input {
			background: none;
			margin : 0;
			padding : 0;
			border : 0;
		}
		#daumSearchBox #daumLogo {
			width: 34px;
			height: 21px;
			float: left;
			margin-right: 5px;
			background-image : url(//i1.daumcdn.net/img-media/tistory/img/bg_search1_2_2010ci.gif);
		}
		#daumSearchBox #show_q {
			background-color: transparent;
			border: none;
			font: 12px Gulim, Sans-serif;
			color: #555;
			margin-top: 4px;
			margin-right: 15px;
			float: left;
		}

		#daumSearchBox #show_btn {
			background-image : url(//i1.daumcdn.net/imgsrc.search/search_all/show/tistory/plugin/bt_search_2.gif);
			width: 37px;
			height: 21px;
			float: left;
			margin:0;
			cursor:pointer;
			text-indent:-1000em;
		}
	</style><link rel="stylesheet" href="./HTTP 구조 (https, request, response, 주요 상태코드)_files/lightbox.min.css">
<link rel="stylesheet" type="text/css" href="./HTTP 구조 (https, request, response, 주요 상태코드)_files/style(1).css">
<script type="text/javascript" src="./HTTP 구조 (https, request, response, 주요 상태코드)_files/profile.js.다운로드"></script>
	<style type="text/css">
		.another_category { border: 1px solid #E5E5E5; padding: 10px 10px 5px; margin:10px 0; clear: both; }
		.another_category h4 { font-size: 12px !important; margin: 0 !important; border-bottom: 1px solid #E5E5E5 !important; padding: 2px 0 6px !important; }
		.another_category h4 a { font-weight: bold !important; }
		.another_category table { table-layout: fixed; border-collapse: collapse; width: 100% !important; margin-top: 10px !important; }
		* html .another_category table { width: auto !important; }
		*:first-child+html .another_category table { width: auto !important; }
		.another_category th, .another_category td { padding: 0 0 4px !important; }
		.another_category th { text-align: left; font-size: 12px !important; font-weight: normal;  word-break: break-all; overflow: hidden; line-height: 1.5; }
		.another_category td { text-align: right; width: 80px; font-size: 11px; }
		.another_category th a { font-weight: normal; text-decoration: none; border: none !important; }
		.another_category th a.current{ font-weight: bold; text-decoration: none !important; border-bottom: 1px solid !important; }
		.another_category th span { font-weight: normal; text-decoration: none; font: 10px Tahoma, Sans-serif; border: none !important; }

		.another_category_color_gray, .another_category_color_gray h4 { border-color: #E5E5E5 !important; }
		.another_category_color_gray * { color: #909090 !important; }
		.another_category_color_gray th a.current{border-color:#909090 !important;}
		.another_category_color_gray h4, .another_category_color_gray h4 a { color: #737373 !important; }


		.another_category_color_red, .another_category_color_red h4 { border-color: #F6D4D3 !important;  }
		.another_category_color_red * { color: #E86869 !important; }
		.another_category_color_red th a.current{border-color:#E86869 !important;}
		.another_category_color_red h4, .another_category_color_red h4 a { color: #ED0908 !important; }


		.another_category_color_green, .another_category_color_green h4 { border-color: #CCE7C8 !important; }
		.another_category_color_green * { color: #64C05B !important; }
		.another_category_color_green th a.current{border-color:#64C05B !important;}
		.another_category_color_green h4, .another_category_color_green h4 a { color: #3EA731 !important; }


		.another_category_color_blue, .another_category_color_blue h4 { border-color: #C8DAF2 !important; }
		.another_category_color_blue * { color: #477FD6 !important; }
		.another_category_color_blue th a.current{border-color:#477FD6 !important;}
		.another_category_color_blue h4, .another_category_color_blue h4 a { color: #1960CA !important; }


		.another_category_color_violet, .another_category_color_violet h4 { border-color: #E1CEEC !important;  }
		.another_category_color_violet * { color:#9D64C5 !important; }
		.another_category_color_violet th a.current{border-color:#9D64C5 !important;}
		.another_category_color_violet h4, .another_category_color_violet h4 a { color: #7E2CB5 !important; }
	</style>
<script type="text/javascript">
        window.TistoryBlog = {
            url: "https://sjh836.tistory.com",
            tistoryUrl: "https://sjh836.tistory.com",
			manageUrl: 'https://sjh836.tistory.com/manage'
        };
        var servicePath = "";
        var blogURL = "";
    </script>

	<script> (function() { window.orgjQuery = window.jQuery; window.jQuery = tjQuery })()</script>
    <script src="./HTTP 구조 (https, request, response, 주요 상태코드)_files/uoclike.min.js.다운로드"></script>
	<script> (function() { window.jQuery = window.orgjQuery; delete window.orgjQuery })()</script>
    <script>
		(function($) {
			$.fn.extend({
				size: function () {
					return this.length
				}
			});
			$.fn.UOCLike.defaults.updateServiceCategory = true;
					})(tjQuery)
    </script>
        <script type="text/javascript" src="./HTTP 구조 (https, request, response, 주요 상태코드)_files/base.js.다운로드"></script>
        <link rel="stylesheet" type="text/css" href="./HTTP 구조 (https, request, response, 주요 상태코드)_files/dialog.css">
            <link rel="stylesheet" type="text/css" href="./HTTP 구조 (https, request, response, 주요 상태코드)_files/postBtn.css">
    <script src="./HTTP 구조 (https, request, response, 주요 상태코드)_files/kakao.min.js.다운로드"></script><style type="text/css">#DragSchLayer{display:block;position:absolute;z-index:1000;width:61px;height:31px;margin:-30px 0px 0px -5px;background:url(//search1.daumcdn.net/search/statics/common/pi/btn_drag_rect.png);cursor:pointer}             @media             only screen and (-webkit-min-device-pixel-ratio: 1.5),             only screen and (min-device-pixel-ratio: 1.5),             only screen and (min-resolution: 1.5dppx) {             #DragSchLayer{background-image:url(//search1.daumcdn.net/search/statics/common/pi/r2/btn_drag_rect.png);background-size:61px 31px}}            </style><script type="text/javascript" async="" src="./HTTP 구조 (https, request, response, 주요 상태코드)_files/td.min.js.다운로드"></script><link rel="stylesheet" type="text/css" href="./HTTP 구조 (https, request, response, 주요 상태코드)_files/uoclike.min-20150408-2.css"></head>

<body id="tt-body-page">
<script type="text/javascript">
	(function() {
		if (!window.T) {
			window.T = {}
		}
		window.T.config = {"TOP_SSL_URL":"https:\/\/www.tistory.com","PREVIEW":false,"ROLE":"guest","PREV_PAGE":"\/82","NEXT_PAGE":"\/80","BLOG":{"isDormancy":false,"title":"\ube68\uac04\uc0c9\ucf54\ub529"},"NEED_COMMENT_LOGIN":false,"COMMENT_LOGIN_CONFIRM_MESSAGE":"","LOGIN_URL":"https:\/\/www.tistory.com\/auth\/login\/?redirectUrl=http%3A%2F%2Fsjh836.tistory.com%2F81","DEFAULT_URL":"https:\/\/sjh836.tistory.com","USER":{"name":null,"homepage":null}};
	})();
</script>

<script type="text/javascript" src="./HTTP 구조 (https, request, response, 주요 상태코드)_files/common.js.다운로드"></script>
<div style="margin:0; padding:0; border:none; background:none; float:none; clear:none; z-index:0"></div>

	<div id="dkIndex">
		<!--웹접근성용 바로가기 링크 모음-->
		<a href="https://sjh836.tistory.com/81#dkBody">본문 바로가기</a>
	</div>
	<div id="dkWrap" class="wrap_skin">
		<!-- 카테고리버튼 클릭시 'navi_on' 클래스 부여 -->
		<div id="dkHead" role="banner" class="area_head">
			<h1 class="screen_out">빨간색코딩</h1>
			<button type="button" class="btn_cate">
				<span class="ico_skin ico_cate">카테고리</span>
			</button>
			<div class="area_search ">
				<button type="button" class="btn_search">
					<span class="ico_skin ico_search">검색하기</span>
				</button>
				
					<form action="https://sjh836.tistory.com/81#" method="get" class="frm_search box_search" onsubmit="try{window.location.href=&#39;/search/&#39;+looseURIEncode(document.getElementsByName(&#39;search&#39;)[0].value);document.getElementsByName(&#39;search&#39;)[0].value=&#39;&#39;;return false;}catch(e){}">
						<fieldset>
							<legend class="screen_out">검색하기</legend>
							<label for="search" class="lab_search screen_out">Search</label>
							<input type="text" name="search" id="search" class="tf_search" placeholder="Search" value="" data-value="">
							<span class="ico_skin ico_search"></span>
						</fieldset>
					</form>
				
			</div>
			<div class="area_profile">
				<div class="tit_post">
					<a href="https://sjh836.tistory.com/" class="link_post">빨간색코딩</a>
				</div>
				<span class="thumb_profile">
                <img src="./HTTP 구조 (https, request, response, 주요 상태코드)_files/215DB34E585E3EC136" class="img_profile" alt="프로필사진">
            </span>
				<span class="txt_profile">빨간색소년</span>
			</div>
		</div>
		<hr class="hide">
		<div id="dkContent" class="cont_skin" role="main">
			<div id="cMain">
				<div id="mFeature" class="wrap_sub">
					<div class="cont_sub">
						<div class="inner_sub">
							<div class="area_sub">
								<div role="navigation" class="area_navi">
									<ul class="tt_category">
	<li class="">
		<a class="link_tit" href="https://sjh836.tistory.com/category">
			분류 전체보기							<span class="c_cnt">(164)</span>
			
					</a>

				<ul class="category_list">
							<li class="">
					<a class="link_item" href="https://sjh836.tistory.com/category/Java">
						Java													<span class="c_cnt">(32)</span>
						
											</a>

					
				</li>
							<li class="">
					<a class="link_item" href="https://sjh836.tistory.com/category/C">
						C													<span class="c_cnt">(10)</span>
						
											</a>

					
				</li>
							<li class="">
					<a class="link_item" href="https://sjh836.tistory.com/category/%EB%94%94%EC%9E%90%EC%9D%B8%ED%8C%A8%ED%84%B4">
						디자인패턴													<span class="c_cnt">(2)</span>
						
											</a>

					
				</li>
							<li class="">
					<a class="link_item" href="https://sjh836.tistory.com/category/%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98">
						알고리즘													<span class="c_cnt">(2)</span>
						
											</a>

					
				</li>
							<li class="">
					<a class="link_item" href="https://sjh836.tistory.com/category/Spring">
						Spring													<span class="c_cnt">(16)</span>
						
											</a>

					
				</li>
							<li class="">
					<a class="link_item" href="https://sjh836.tistory.com/category/Web">
						Web													<span class="c_cnt">(21)</span>
						
											</a>

					
				</li>
							<li class="">
					<a class="link_item" href="https://sjh836.tistory.com/category/node.js">
						node.js													<span class="c_cnt">(17)</span>
						
											</a>

					
				</li>
							<li class="">
					<a class="link_item" href="https://sjh836.tistory.com/category/python">
						python													<span class="c_cnt">(1)</span>
						
											</a>

					
				</li>
							<li class="">
					<a class="link_item" href="https://sjh836.tistory.com/category/%EB%B9%8C%EB%93%9C%EB%8F%84%EA%B5%AC">
						빌드도구													<span class="c_cnt">(1)</span>
						
											</a>

					
				</li>
							<li class="">
					<a class="link_item" href="https://sjh836.tistory.com/category/Git">
						Git													<span class="c_cnt">(7)</span>
						
											</a>

					
				</li>
							<li class="">
					<a class="link_item" href="https://sjh836.tistory.com/category/network">
						network													<span class="c_cnt">(17)</span>
						
											</a>

					
				</li>
							<li class="">
					<a class="link_item" href="https://sjh836.tistory.com/category/database">
						database													<span class="c_cnt">(7)</span>
						
											</a>

					
				</li>
							<li class="">
					<a class="link_item" href="https://sjh836.tistory.com/category/R">
						R													<span class="c_cnt">(7)</span>
						
											</a>

					
				</li>
							<li class="">
					<a class="link_item" href="https://sjh836.tistory.com/category/%EB%B9%85%EB%8D%B0%EC%9D%B4%ED%84%B0">
						빅데이터													<span class="c_cnt">(5)</span>
						
											</a>

					
				</li>
							<li class="">
					<a class="link_item" href="https://sjh836.tistory.com/category/Linux">
						Linux													<span class="c_cnt">(9)</span>
						
											</a>

					
				</li>
							<li class="">
					<a class="link_item" href="https://sjh836.tistory.com/category/assembly">
						assembly													<span class="c_cnt">(1)</span>
						
											</a>

					
				</li>
							<li class="">
					<a class="link_item" href="https://sjh836.tistory.com/category/%EC%9E%90%EA%B2%A9%EC%A6%9D">
						자격증													<span class="c_cnt">(6)</span>
						
											</a>

					
				</li>
							<li class="">
					<a class="link_item" href="https://sjh836.tistory.com/category/%EC%9D%BC%EC%83%81">
						일상													<span class="c_cnt">(3)</span>
						
											</a>

					
				</li>
					</ul>
			</li>
</ul>
									<a href="https://sjh836.tistory.com/guestbook" class="link_guestbook">Guestbook</a>
								</div>
								<div class="wrap_etc">
									<div class="col_aside left_side">
										
												<!-- 공지사항 -->
												
													<div class="box_aside">
														<strong class="tit_aside">Notice</strong>
														<ul class="list_board">
															
														</ul>
													</div>
												
											
												<!-- 최근에 올라온 글 -->
												<div class="box_aside">
													<strong class="tit_aside">Recent Posts</strong>
													<ul class="list_board">
														
															<li><a href="https://sjh836.tistory.com/173" class="link_board">[이펙티브 자바3판] 7장 람..</a></li>
														

															<li><a href="https://sjh836.tistory.com/172" class="link_board">[이펙티브 자바3판] 9장 일..</a></li>
														

															<li><a href="https://sjh836.tistory.com/171" class="link_board">[이펙티브 자바3판] 5장 제..</a></li>
														

															<li><a href="https://sjh836.tistory.com/170" class="link_board">[이펙티브 자바3판] 4장 클..</a></li>
														
													</ul>
												</div>
											
												<!-- 최근에 달린 댓글 -->
												<div class="box_aside">
													<strong class="tit_aside">Recent Comments</strong>
													<ul class="list_board">
														
															<li><a href="https://sjh836.tistory.com/13#comment19256569" class="link_board">ㄱㅅ함니당</a></li>
														

															<li><a href="https://sjh836.tistory.com/131#comment19242323" class="link_board">감사합니다.!</a></li>
														

															<li><a href="https://sjh836.tistory.com/131#comment19225498" class="link_board">설명을 엄청 간단히 잘해놓으..</a></li>
														

															<li><a href="https://sjh836.tistory.com/131#comment19208894" class="link_board">좋은 자료 감사합니다.</a></li>
														
													</ul>
												</div>
											
												<!-- 링크 -->
												<div class="box_aside">
													<strong class="tit_aside">Link</strong>
													<ul class="list_board">
														
													</ul>
												</div>
											
									</div>


									<div class="col_aside right_side">
										
												<!-- 달력 -->
												<div class="box_aside box_calendar">
															<table class="tt-calendar" cellpadding="0" cellspacing="1" style="width: 100%; table-layout: fixed">
			<caption class="cal_month">
				<a href="https://sjh836.tistory.com/archive/201812" title="1개월 앞의 달력을 보여줍니다.">«</a>
				&nbsp;
				<a href="https://sjh836.tistory.com/archive/201901" title="현재 달의 달력을 보여줍니다.">2019/01</a>
				&nbsp;
				<a href="https://sjh836.tistory.com/archive/201902" title="1개월 뒤의 달력을 보여줍니다.">»</a>
			</caption>
			<thead>
			<tr>
				<th class="cal_week2">일</th>
				<th class="cal_week1">월</th>
				<th class="cal_week1">화</th>
				<th class="cal_week1">수</th>
				<th class="cal_week1">목</th>
				<th class="cal_week1">금</th>
				<th class="cal_week1">토</th>
			</tr>
			</thead>
			<tbody>
					<tr class="cal_week">
			<td class="cal_day1">&nbsp;</td>
			<td class="cal_day1">&nbsp;</td>
			<td class=" cal_day cal_day3">1</td>
			<td class=" cal_day cal_day3">2</td>
			<td class=" cal_day cal_day3">3</td>
			<td class=" cal_day cal_day3">4</td>
			<td class=" cal_day cal_day3">5</td>
		</tr>
		<tr class="cal_week">
			<td class=" cal_day cal_day_sunday cal_day3">6</td>
			<td class=" cal_day cal_day3">7</td>
			<td class=" cal_day cal_day3">8</td>
			<td class=" cal_day cal_day3">9</td>
			<td class=" cal_day cal_day3">10</td>
			<td class=" cal_day cal_day3">11</td>
			<td class=" cal_day cal_day3">12</td>
		</tr>
		<tr class="cal_week">
			<td class=" cal_day cal_day_sunday cal_day3">13</td>
			<td class=" cal_day cal_day3">14</td>
			<td class=" cal_day cal_day3">15</td>
			<td class=" cal_day cal_day3">16</td>
			<td class=" cal_day cal_day3">17</td>
			<td class=" cal_day cal_day3"><a class="cal_click" href="https://sjh836.tistory.com/archive/20190118">18</a></td>
			<td class=" cal_day cal_day3">19</td>
		</tr>
		<tr class="cal_week cal_current_week">
			<td class=" cal_day cal_day_sunday cal_day3">20</td>
			<td class=" cal_day cal_day3">21</td>
			<td class=" cal_day cal_day3">22</td>
			<td class=" cal_day cal_day4">23</td>
			<td class=" cal_day cal_day3">24</td>
			<td class=" cal_day cal_day3">25</td>
			<td class=" cal_day cal_day3">26</td>
		</tr>
		<tr class="cal_week">
			<td class=" cal_day cal_day_sunday cal_day3">27</td>
			<td class=" cal_day cal_day3">28</td>
			<td class=" cal_day cal_day3">29</td>
			<td class=" cal_day cal_day3">30</td>
			<td class=" cal_day cal_day3">31</td>
			<td class="cal_day2">&nbsp;</td>
			<td class="cal_day2">&nbsp;</td>
		</tr>
			</tbody>
		</table>
		
												</div>
											
												<!-- 태그 클라우드 -->
												<div class="box_aside box_tag">
													<strong class="tit_aside">Tags</strong>
													<ul class="list_tag">
														
															<li><a href="https://sjh836.tistory.com/tag/git" class="link_tag cloud4">git</a></li>
														
															<li><a href="https://sjh836.tistory.com/tag/%EB%8D%B0%EC%9D%B4%ED%84%B0%ED%86%B5%EC%8B%A0" class="link_tag cloud4">데이터통신</a></li>
														
															<li><a href="https://sjh836.tistory.com/tag/TCP" class="link_tag cloud4">TCP</a></li>
														
															<li><a href="https://sjh836.tistory.com/tag/spring" class="link_tag cloud3">spring</a></li>
														
															<li><a href="https://sjh836.tistory.com/tag/mybatis" class="link_tag cloud4">mybatis</a></li>
														
															<li><a href="https://sjh836.tistory.com/tag/VCS" class="link_tag cloud4">VCS</a></li>
														
															<li><a href="https://sjh836.tistory.com/tag/Linux" class="link_tag cloud4">Linux</a></li>
														
															<li><a href="https://sjh836.tistory.com/tag/libuv" class="link_tag cloud4">libuv</a></li>
														
															<li><a href="https://sjh836.tistory.com/tag/github" class="link_tag cloud4">github</a></li>
														
															<li><a href="https://sjh836.tistory.com/tag/Static" class="link_tag cloud4">Static</a></li>
														
															<li><a href="https://sjh836.tistory.com/tag/V8" class="link_tag cloud4">V8</a></li>
														
															<li><a href="https://sjh836.tistory.com/tag/HTTP" class="link_tag cloud4">HTTP</a></li>
														
															<li><a href="https://sjh836.tistory.com/tag/template" class="link_tag cloud4">template</a></li>
														
															<li><a href="https://sjh836.tistory.com/tag/ajax" class="link_tag cloud4">ajax</a></li>
														
															<li><a href="https://sjh836.tistory.com/tag/effective" class="link_tag cloud4">effective</a></li>
														
															<li><a href="https://sjh836.tistory.com/tag/javascript" class="link_tag cloud4">javascript</a></li>
														
															<li><a href="https://sjh836.tistory.com/tag/Express" class="link_tag cloud4">Express</a></li>
														
															<li><a href="https://sjh836.tistory.com/tag/SERVLET" class="link_tag cloud4">SERVLET</a></li>
														
															<li><a href="https://sjh836.tistory.com/tag/Java" class="link_tag cloud1">Java</a></li>
														
															<li><a href="https://sjh836.tistory.com/tag/json" class="link_tag cloud4">json</a></li>
														
															<li><a href="https://sjh836.tistory.com/tag/%EB%84%A4%ED%8A%B8%EC%9B%8C%ED%81%AC" class="link_tag cloud4">네트워크</a></li>
														
															<li><a href="https://sjh836.tistory.com/tag/Elk" class="link_tag cloud4">Elk</a></li>
														
															<li><a href="https://sjh836.tistory.com/tag/html" class="link_tag cloud4">html</a></li>
														
															<li><a href="https://sjh836.tistory.com/tag/socket" class="link_tag cloud4">socket</a></li>
														
															<li><a href="https://sjh836.tistory.com/tag/mongodb" class="link_tag cloud4">mongodb</a></li>
														
															<li><a href="https://sjh836.tistory.com/tag/network" class="link_tag cloud3">network</a></li>
														
															<li><a href="https://sjh836.tistory.com/tag/Heap" class="link_tag cloud4">Heap</a></li>
														
															<li><a href="https://sjh836.tistory.com/tag/r" class="link_tag cloud4">r</a></li>
														
															<li><a href="https://sjh836.tistory.com/tag/nodejs" class="link_tag cloud3">nodejs</a></li>
														
															<li><a href="https://sjh836.tistory.com/tag/Lombok" class="link_tag cloud4">Lombok</a></li>
														
													</ul>
													<a href="https://sjh836.tistory.com/tag" class="link_more">more</a>
												</div>
											
												<!-- 글 보관함 -->
												<div class="box_aside box_archive">
													<strong class="tit_aside">Archives</strong>
													<ul class="list_keep">
														
															<li><a href="https://sjh836.tistory.com/archive/201901" class="link_keep">2019/01</a> (1)</li>
														

															<li><a href="https://sjh836.tistory.com/archive/201812" class="link_keep">2018/12</a> (3)</li>
														

															<li><a href="https://sjh836.tistory.com/archive/201811" class="link_keep">2018/11</a> (2)</li>
														

															<li><a href="https://sjh836.tistory.com/archive/201808" class="link_keep">2018/08</a> (6)</li>
														
													</ul>
												</div>
											
												<!-- 방문자수 -->
												<div class="box_aside box_visitor">
													<dl class="list_visitor">
														<dt>Today</dt>
														<dd>617</dd>
													</dl>
													<dl class="list_total">
														<dt>Total</dt>
														<dd>166,326</dd>
													</dl>
												</div>
											
									</div>
								</div>
							</div>
						</div>
						<button type="button" class="ico_skin btn_close">닫기</button>

						<strong class="screen_out">관리 메뉴</strong>
						<ul class="list_control">
							<li><a href="https://sjh836.tistory.com/manage/entry/post" class="ico_skin link_write" title="글쓰기">글쓰기</a></li>
							<li><a href="https://sjh836.tistory.com/guestbook" class="ico_skin link_memo" title="방명록">방명록</a></li>
							<li><a href="https://sjh836.tistory.com/rss" class="ico_skin link_rss" title="RSS">RSS</a></li>
							<li><a href="https://sjh836.tistory.com/manage" class="ico_skin link_manage" title="관리">관리</a></li>
						</ul>
					</div>
				</div>

				<div id="mArticle" class="article_skin">

					

					<div class="index_title">
						<h2 class="tit_skin"><span class="txt_title">빨간색코딩</span></h2>
					</div>

					
						


						
							<h2 id="dkBody" class="screen_out">HTTP 구조 (https, request, response, 주요 상태코드) 본문</h2>
							<div class="area_title">
								<strong class="tit_category"><a href="https://sjh836.tistory.com/category/network">network</a></strong>
								<h3 class="tit_post">HTTP 구조 (https, request, response, 주요 상태코드)</h3>
								<span class="info_post">빨간색소년
                                <span class="txt_bar"></span>2017.07.10 21:30
								
							</span>
							</div>

							<div class="area_view">
								<div class="tt_article_useless_p_margin"><p><br></p>
<h2 style="BOX-SIZING: border-box; MARGIN-BOTTOM: 16px; FONT-FAMILY: -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, Roboto, Helvetica, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; MARGIN-TOP: 24px; BORDER-BOTTOM: rgb(238,238,238) 1px solid; COLOR: rgb(51,51,51); PADDING-BOTTOM: 0.3em; LINE-HEIGHT: 1.25">1. 특징</h2>
<ul style="BOX-SIZING: border-box; FONT-SIZE: 16px; MARGIN-BOTTOM: 16px; FONT-FAMILY: -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, Roboto, Helvetica, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; MARGIN-TOP: 0px; COLOR: rgb(51,51,51); PADDING-LEFT: 2em">
<li style="BOX-SIZING: border-box">인터넷상에서 데이터를 주고 받기 위한 서버/클라이언트 모델을 따르는 전송 프로토콜</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">애플리케이션 레벨의 프로토콜로 TCP/IP위에서 작동</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">클라이언트에서 요청(request)를 보내면 서버는 요청을 처리해서 응답(response)</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">80번 port 이용</li></ul>
<h3 style="BOX-SIZING: border-box; FONT-SIZE: 1.25em; MARGIN-BOTTOM: 16px; FONT-FAMILY: -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, Roboto, Helvetica, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; MARGIN-TOP: 24px; COLOR: rgb(51,51,51); LINE-HEIGHT: 1.25">비상태연결(Stateless, Connectless)</h3>
<p style="BOX-SIZING: border-box; FONT-SIZE: 16px; MARGIN-BOTTOM: 16px; FONT-FAMILY: -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, Roboto, Helvetica, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; COLOR: rgb(51,51,51)">서버에 연결하고 요청해서 응답을 받으면 연결을 끊어버린다.</p>
<ul style="BOX-SIZING: border-box; FONT-SIZE: 16px; MARGIN-BOTTOM: 16px; FONT-FAMILY: -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, Roboto, Helvetica, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; MARGIN-TOP: 0px; COLOR: rgb(51,51,51); PADDING-LEFT: 2em">
<li style="BOX-SIZING: border-box">장점: 접속유지 최소화, 불특정 다수를 대상으로 하는 서비스에 유리</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">단점: 연결을 끊어버리기 때문에, 클라이언트의 이전 상태를 알 수 없음, 따라서 로그인을 해도 정보유지 불가, 이를 해결하기 위해 쿠키 등등을 이용</li></ul>
<h3 style="BOX-SIZING: border-box; FONT-SIZE: 1.25em; MARGIN-BOTTOM: 16px; FONT-FAMILY: -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, Roboto, Helvetica, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; MARGIN-TOP: 24px; COLOR: rgb(51,51,51); LINE-HEIGHT: 1.25">Keep Alive</h3>
<p style="BOX-SIZING: border-box; FONT-SIZE: 16px; MARGIN-BOTTOM: 16px; FONT-FAMILY: -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, Roboto, Helvetica, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; COLOR: rgb(51,51,51)">HTTP 1.1 부터는 keep-alive 기능을 지원</p>
<p style="BOX-SIZING: border-box; FONT-SIZE: 16px; MARGIN-BOTTOM: 16px; FONT-FAMILY: -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, Roboto, Helvetica, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; COLOR: rgb(51,51,51)">HTTP는 하나의 연결에 하나의 요청을 하는 것을 기준으로 설계가 되어, 문서에 20여개의 파일이 있다면 계속 연결하고 다운하고 연결끊어야한다. TCP통신 과정에서 비용이 많이 소모함. 따라서 Keep Alive 기능 등장.</p>
<p style="BOX-SIZING: border-box; FONT-SIZE: 16px; MARGIN-BOTTOM: 16px; FONT-FAMILY: -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, Roboto, Helvetica, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; COLOR: rgb(51,51,51)">지정된 시간동안 연결을 끊지 않고 요청을 계속해서 보낼 수 있다.</p>
<h3 style="BOX-SIZING: border-box; FONT-SIZE: 1.25em; MARGIN-BOTTOM: 16px; FONT-FAMILY: -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, Roboto, Helvetica, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; MARGIN-TOP: 24px; COLOR: rgb(51,51,51); LINE-HEIGHT: 1.25">HTTPS</h3>
<p style="BOX-SIZING: border-box; FONT-SIZE: 16px; MARGIN-BOTTOM: 16px; FONT-FAMILY: -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, Roboto, Helvetica, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; COLOR: rgb(51,51,51)">SSL은 전자상거래에서의 데이터 보안을 위해서 개발한 통신 레이어다. SSL은 표현계층의 프로토콜로 응용 계층 아래에 있기 때문에, 어떤 응용 계층의 데이터라도 암호화해서 보낼 수 있다</p>
<p style="BOX-SIZING: border-box; FONT-SIZE: 16px; MARGIN-BOTTOM: 16px; FONT-FAMILY: -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, Roboto, Helvetica, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; COLOR: rgb(51,51,51)">&nbsp;</p>
<p style="BOX-SIZING: border-box; FONT-SIZE: 16px; MARGIN-BOTTOM: 16px; FONT-FAMILY: -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, Roboto, Helvetica, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; FLOAT: none; COLOR: rgb(51,51,51); TEXT-ALIGN: center; CLEAR: none"><span class="imageblock" style="display:inline-block;width:728px;;height:auto;max-width:100%"><span data-url="https://t1.daumcdn.net/cfile/tistory/216CF8395963739014?original" data-lightbox="lightbox"><img srcset="//img1.daumcdn.net/thumb/R1920x0/?fname=http%3A%2F%2Fcfile23.uf.tistory.com%2Fimage%2F216CF8395963739014DFE0 1920w, //img1.daumcdn.net/thumb/R960x0/?fname=http%3A%2F%2Fcfile23.uf.tistory.com%2Fimage%2F216CF8395963739014DFE0 960w, //img1.daumcdn.net/thumb/R720x0/?fname=http%3A%2F%2Fcfile23.uf.tistory.com%2Fimage%2F216CF8395963739014DFE0 720w, //img1.daumcdn.net/thumb/R640x0.q70/?fname=http%3A%2F%2Fcfile23.uf.tistory.com%2Fimage%2F216CF8395963739014DFE0 640w, //img1.daumcdn.net/thumb/R480x0.q70/?fname=http%3A%2F%2Fcfile23.uf.tistory.com%2Fimage%2F216CF8395963739014DFE0 480w" src="./HTTP 구조 (https, request, response, 주요 상태코드)_files/216CF8395963739014" style="cursor: pointer;max-width:100%;height:auto" width="728" height="477" filename="https.png" filemime="image/jpeg"></span></span></p>
<ul style="BOX-SIZING: border-box; FONT-SIZE: 16px; MARGIN-BOTTOM: 16px; FONT-FAMILY: -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, Roboto, Helvetica, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; MARGIN-TOP: 0px; COLOR: rgb(51,51,51); PADDING-LEFT: 2em">
<li style="BOX-SIZING: border-box">HTTPS의 기본 포트번호는 443</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">HTTP에 비해 많이 느림</li></ul>
<h2 style="BOX-SIZING: border-box; MARGIN-BOTTOM: 16px; FONT-FAMILY: -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, Roboto, Helvetica, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; MARGIN-TOP: 24px; BORDER-BOTTOM: rgb(238,238,238) 1px solid; COLOR: rgb(51,51,51); PADDING-BOTTOM: 0.3em; LINE-HEIGHT: 1.25">2. Request</h2>
<h3 style="BOX-SIZING: border-box; FONT-SIZE: 1.25em; MARGIN-BOTTOM: 16px; FONT-FAMILY: -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, Roboto, Helvetica, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; MARGIN-TOP: 24px; COLOR: rgb(51,51,51); LINE-HEIGHT: 1.25">메세지 구조</h3>
<ul style="BOX-SIZING: border-box; FONT-SIZE: 16px; MARGIN-BOTTOM: 16px; FONT-FAMILY: -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, Roboto, Helvetica, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; MARGIN-TOP: 0px; COLOR: rgb(51,51,51); PADDING-LEFT: 2em">
<li style="BOX-SIZING: border-box">요청 라인 : GET / HTTP/1.1
<ul style="BOX-SIZING: border-box; MARGIN-BOTTOM: 0px; MARGIN-TOP: 0px; PADDING-LEFT: 2em">
<li style="BOX-SIZING: border-box">요청 메소드 : GET, POST, PUT, DELETE</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">요청 URL</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">HTTP 버전</li></ul></li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">요청 헤더 : 키-값 방식으로 들어감
<ul style="BOX-SIZING: border-box; MARGIN-BOTTOM: 0px; MARGIN-TOP: 0px; PADDING-LEFT: 2em">
<li style="BOX-SIZING: border-box">Accept : 클라이언트가 받을 수 있는 컨텐츠</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">Cookie : 쿠키</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">Content-Type : 메세지 바디 종류</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">Content-Length : 메세지 바디 길이</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">If-Modified-Since : 특정 날짜 이후에 변경됐을 때만</li></ul></li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">요청 바디(엔티티)</li></ul>
<h3 style="BOX-SIZING: border-box; FONT-SIZE: 1.25em; MARGIN-BOTTOM: 16px; FONT-FAMILY: -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, Roboto, Helvetica, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; MARGIN-TOP: 24px; COLOR: rgb(51,51,51); LINE-HEIGHT: 1.25">Content-Type과 Body</h3>
<p style="BOX-SIZING: border-box; FONT-SIZE: 16px; MARGIN-BOTTOM: 16px; FONT-FAMILY: -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, Roboto, Helvetica, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; COLOR: rgb(51,51,51)">참조문서 :&nbsp;<a style="BOX-SIZING: border-box; COLOR: rgb(64,120,192); BACKGROUND-COLOR: transparent" href="https://www.w3.org/Protocols/rfc1341/4_Content-Type.html">https://www.w3.org/Protocols/rfc1341/4_Content-Type.html</a></p>
<ol style="BOX-SIZING: border-box; FONT-SIZE: 16px; MARGIN-BOTTOM: 16px; FONT-FAMILY: -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, Roboto, Helvetica, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; MARGIN-TOP: 0px; COLOR: rgb(51,51,51); PADDING-LEFT: 2em">
<li style="BOX-SIZING: border-box">form 형태 : URLEncoded 방식
<ul style="BOX-SIZING: border-box; MARGIN-BOTTOM: 0px; MARGIN-TOP: 0px; PADDING-LEFT: 2em">
<li style="BOX-SIZING: border-box">application/x-www-form-urlencoded</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">메세지 바디 : 쿼리 문자열</li></ul></li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">json 형태
<ul style="BOX-SIZING: border-box; MARGIN-BOTTOM: 0px; MARGIN-TOP: 0px; PADDING-LEFT: 2em">
<li style="BOX-SIZING: border-box">application/json</li></ul></li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">멀티파트 형태 : 이진파일 넘길 때 사용, 하나의 메세지 바디에 파트를 나눠서 작성
<ul style="BOX-SIZING: border-box; MARGIN-BOTTOM: 0px; MARGIN-TOP: 0px; PADDING-LEFT: 2em">
<li style="BOX-SIZING: border-box">boundary는 파트 구분자</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">multipart/form-data: boundary=frontier</li></ul></li></ol>
<h2 style="BOX-SIZING: border-box; MARGIN-BOTTOM: 16px; FONT-FAMILY: -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, Roboto, Helvetica, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; MARGIN-TOP: 24px; BORDER-BOTTOM: rgb(238,238,238) 1px solid; COLOR: rgb(51,51,51); PADDING-BOTTOM: 0.3em; LINE-HEIGHT: 1.25">3. Response</h2>
<h3 style="BOX-SIZING: border-box; FONT-SIZE: 1.25em; MARGIN-BOTTOM: 16px; FONT-FAMILY: -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, Roboto, Helvetica, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; MARGIN-TOP: 24px; COLOR: rgb(51,51,51); LINE-HEIGHT: 1.25">메세지 구조</h3>
<ul style="BOX-SIZING: border-box; FONT-SIZE: 16px; MARGIN-BOTTOM: 16px; FONT-FAMILY: -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, Roboto, Helvetica, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; MARGIN-TOP: 0px; COLOR: rgb(51,51,51); PADDING-LEFT: 2em">
<li style="BOX-SIZING: border-box">응답 라인
<ul style="BOX-SIZING: border-box; MARGIN-BOTTOM: 0px; MARGIN-TOP: 0px; PADDING-LEFT: 2em">
<li style="BOX-SIZING: border-box">버전</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">상태 코드</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">상태 메세지 : HTTP/1.1 200 OK</li></ul></li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">응답 헤더
<ul style="BOX-SIZING: border-box; MARGIN-BOTTOM: 0px; MARGIN-TOP: 0px; PADDING-LEFT: 2em">
<li style="BOX-SIZING: border-box">Content-Type : 바디 데이터의 타입</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">Content-Length : 바디 데이터 크기</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">Set-Cookie : 쿠키 설정</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">ETag : 엔티티 태그</li></ul></li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">응답 바디 : HTML, JSON, Octet Stream 등이 있다.</li></ul>
<h3 style="BOX-SIZING: border-box; FONT-SIZE: 1.25em; MARGIN-BOTTOM: 16px; FONT-FAMILY: -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, Roboto, Helvetica, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; MARGIN-TOP: 24px; COLOR: rgb(51,51,51); LINE-HEIGHT: 1.25">상태 코드</h3>
<ul style="BOX-SIZING: border-box; FONT-SIZE: 16px; MARGIN-BOTTOM: 16px; FONT-FAMILY: -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, Roboto, Helvetica, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; MARGIN-TOP: 0px; COLOR: rgb(51,51,51); PADDING-LEFT: 2em">
<li style="BOX-SIZING: border-box">1xx : 정보</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">2xx : 성공
<ul style="BOX-SIZING: border-box; MARGIN-BOTTOM: 0px; MARGIN-TOP: 0px; PADDING-LEFT: 2em">
<li style="BOX-SIZING: border-box">200 : OK. 요청 성공</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">201 : Created. 생성 요청 성공</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">202 : Accepted. 요청 수락(처리 보장X)</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">204 : 성공했으나 돌려줄게 없음</li></ul></li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">3xx : 리다이렉션
<ul style="BOX-SIZING: border-box; MARGIN-BOTTOM: 0px; MARGIN-TOP: 0px; PADDING-LEFT: 2em">
<li style="BOX-SIZING: border-box">300 : Multiple choices. 여러 리소스에 대한 요청 결과 목록</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">301,302,303 : Redirect. 리소스 위치가 변경된 상태</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">304 : Not Modified. 리소스가 수정되지 않았음</li></ul></li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">4xx : 클라이언트 오류
<ul style="BOX-SIZING: border-box; MARGIN-BOTTOM: 0px; MARGIN-TOP: 0px; PADDING-LEFT: 2em">
<li style="BOX-SIZING: border-box">400 : Bad Request. 요청 오류</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">401 : Unauthorized. 권한없음</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">403 : Forbidden. 요청 거부</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">404 : Not Found. 리소스가 없는 상태</li></ul></li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">5xx : 서버 오류
<ul style="BOX-SIZING: border-box; MARGIN-BOTTOM: 0px; MARGIN-TOP: 0px; PADDING-LEFT: 2em">
<li style="BOX-SIZING: border-box">500 : Internal Server Error. 서버가 요청을 처리 못함</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">501 : Not Implemented. 서버가 지원하지 않는 요청</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">503 : Service Unavailable. 과부하 등으로 당장 서비스가 불가능한 상태</li></ul></li></ul>
<h3 style="BOX-SIZING: border-box; FONT-SIZE: 1.25em; MARGIN-BOTTOM: 16px; FONT-FAMILY: -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, Roboto, Helvetica, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; MARGIN-TOP: 24px; COLOR: rgb(51,51,51); LINE-HEIGHT: 1.25">Content-Type과 Body</h3>
<p style="BOX-SIZING: border-box; FONT-SIZE: 16px; MARGIN-BOTTOM: 16px; FONT-FAMILY: -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, Roboto, Helvetica, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; COLOR: rgb(51,51,51)">주요 컨텐츠 타입은 아래와 같다.</p>
<ul style="BOX-SIZING: border-box; FONT-SIZE: 16px; MARGIN-BOTTOM: 0px !important; FONT-FAMILY: -apple-system, BlinkMacSystemFont, &quot;Segoe UI&quot;, Roboto, Helvetica, Arial, sans-serif, &quot;Apple Color Emoji&quot;, &quot;Segoe UI Emoji&quot;, &quot;Segoe UI Symbol&quot;; MARGIN-TOP: 0px; COLOR: rgb(51,51,51); PADDING-LEFT: 2em">
<li style="BOX-SIZING: border-box">text/plain, text/html</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">application/xml, application/json</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">image/png, image/jpg</li>
<li style="BOX-SIZING: border-box; MARGIN-TOP: 0.25em">audio/mp3, video/mp4</li></ul>
<p><br></p><div class="container_postbtn"><div class="postbtn_like"><div class="like_btn" data-uoc-svc="tistory" data-uoc-uid="2548253_81" data-uoc-sc="401" data-uoc-pcurl="https://sjh836.tistory.com/81" data-uoc-fetchurl="http://api.kakao.tistory.com/like/fetch?uid=2548253_81"><label class="uoc-icon"><span class="ico_postbtn ico_like"></span> <span class="txt_like uoc-text">공감</span><span class="txt_like uoc-count" style="display: none;"></span><input type="button" class="inp_btn uoc-button"></label></div><span class="ico_bar"></span><label data-thumbnail-url="https://t1.daumcdn.net/cfile/tistory/216CF8395963739014" data-title="HTTP 구조 (https, request, response, 주요 상태코드)" data-description="1. 특징 인터넷상에서 데이터를 주고 받기 위한 서버/클라이언트 모델을 따르는 전송 프로토콜 애플리케이션 레벨의 프로토콜로 TCP/IP위에서 작동 클라이언트에서 요청(request)를 보내면 서버는 요청을 처리해서.." data-profile-image="https://t1.daumcdn.net/cfile/tistory/215DB34E585E3EC136" data-profile-name="빨간색소년" data-pc-url="https://sjh836.tistory.com/81" data-blog-title="빨간색코딩"><span class="ico_postbtn ico_sns">sns</span><input type="button" class="inp_btn"></label><span class="ico_bar"></span><label data-entry-id="81"><span class="ico_postbtn ico_report">신고</span><input type="button" class="inp_btn"></label></div></div><div class="another_category another_category_color_gray">
<h4>'<a href="https://sjh836.tistory.com/category/network">network</a>' 카테고리의 다른 글</h4>
<table>
<tbody><tr>
<th>
<a href="https://sjh836.tistory.com/85?category=680971">데이터통신 17장 ATM망 연습문제 풀이</a>&nbsp;&nbsp;<span>(0)</span>
</th>
<td>
2017.07.11</td>
</tr>
<tr>
<th>
<a href="https://sjh836.tistory.com/81?category=680971" class="current">HTTP 구조 (https, request, response, 주요 상태코드)</a>&nbsp;&nbsp;<span>(0)</span>
</th>
<td>
2017.07.10</td>
</tr>
<tr>
<th>
<a href="https://sjh836.tistory.com/72?category=680971">데이터통신 15장 X.25 패킷 교환망 연습문제 풀이</a>&nbsp;&nbsp;<span>(0)</span>
</th>
<td>
2017.06.03</td>
</tr>
<tr>
<th>
<a href="https://sjh836.tistory.com/67?category=680971">데이터통신 14장 디지털 종합 정보 통신망 연습문제 풀이</a>&nbsp;&nbsp;<span>(0)</span>
</th>
<td>
2017.05.29</td>
</tr>
<tr>
<th>
<a href="https://sjh836.tistory.com/63?category=680971">데이터통신 13장 교환방식: 네트워크층 기능 연습문제 풀이</a>&nbsp;&nbsp;<span>(0)</span>
</th>
<td>
2017.05.24</td>
</tr>
<tr>
<th>
<a href="https://sjh836.tistory.com/61?category=680971">데이터통신 12장 근거리 통신망 연습문제 풀이</a>&nbsp;&nbsp;<span>(1)</span>
</th>
<td>
2017.05.20</td>
</tr>
</tbody></table></div></div>
							</div>
							<div class="area_etc">
								
									<dl class="list_tag">
										<dt>Tag</dt>
										<dd><a href="https://sjh836.tistory.com/tag/HTTP" rel="tag">HTTP</a>,
<a href="https://sjh836.tistory.com/tag/https" rel="tag">https</a>,
<a href="https://sjh836.tistory.com/tag/request" rel="tag">request</a>,
<a href="https://sjh836.tistory.com/tag/response" rel="tag">response</a></dd>
									</dl>
								
							</div>

							
								<div class="area_related">
									<strong class="tit_related">'network' Related Articles</strong>
									<ul class="list_related">
										
											<li class="thumb_type">
												<a href="https://sjh836.tistory.com/85?category=680971" class="link_related">
													
													<span class="thumb_related">
														<img src="./HTTP 구조 (https, request, response, 주요 상태코드)_files/saved_resource" class="img_related" alt="">
													</span>
													
													<span class="txt_related">데이터통신 17장 ATM망 연습문제 풀이</span>
													<span class="date_related">2017.07.11</span>
													<span class="frame_related"></span>
												</a>
											</li>
										
											<li class="thumb_type">
												<a href="https://sjh836.tistory.com/72?category=680971" class="link_related">
													
													<span class="thumb_related">
														<img src="./HTTP 구조 (https, request, response, 주요 상태코드)_files/saved_resource(1)" class="img_related" alt="">
													</span>
													
													<span class="txt_related">데이터통신 15장 X.25 패킷 교환망 연습문제 풀이</span>
													<span class="date_related">2017.06.03</span>
													<span class="frame_related"></span>
												</a>
											</li>
										
											<li class="thumb_type">
												<a href="https://sjh836.tistory.com/67?category=680971" class="link_related">
													
													<span class="thumb_related">
														<img src="./HTTP 구조 (https, request, response, 주요 상태코드)_files/saved_resource(2)" class="img_related" alt="">
													</span>
													
													<span class="txt_related">데이터통신 14장 디지털 종합 정보 통신망 연습문제 풀이</span>
													<span class="date_related">2017.05.29</span>
													<span class="frame_related"></span>
												</a>
											</li>
										
											<li class="thumb_type">
												<a href="https://sjh836.tistory.com/63?category=680971" class="link_related">
													
													<span class="thumb_related">
														<img src="./HTTP 구조 (https, request, response, 주요 상태코드)_files/saved_resource(3)" class="img_related" alt="">
													</span>
													
													<span class="txt_related">데이터통신 13장 교환방식: 네트워크층 기능 연습문제 풀이</span>
													<span class="date_related">2017.05.24</span>
													<span class="frame_related"></span>
												</a>
											</li>
										
									</ul>
									<a href="https://sjh836.tistory.com/category/network" class="link_more">more</a>
								</div>
							

							<div class="area_reply">
								<strong class="tit_reply" onclick="toggleLayerForEntry(&#39;81&#39;, &#39;comment&#39;); return false"><span id="commentCount81">0</span>  Comments</strong>
								<div id="entry81Comment" style="display:block">
									

									<form method="post" action="https://sjh836.tistory.com/comment/add/81" onsubmit="return false" style="margin: 0">
										<fieldset class="fld_reply">
											<legend class="screen_out">댓글쓰기 폼</legend>
											
												
													<div class="writer_info">
                                                    <span class="info_name">
                                                        <label for="name" class="lab_info screen_out">이름</label>
                                                        <span class="wrap_info">
                                                            <input type="text" name="name" id="name" class="inp_info" placeholder="Name" tabindex="1">
                                                        </span>
                                                    </span>
														<span class="info_pw ">
                                                        <label for="password" class="lab_info screen_out">비밀번호</label>
                                                        <span class="wrap_info">
                                                            <input type="password" name="password" id="password" class="inp_info" placeholder="Password" tabindex="2">
                                                        </span>
                                                    </span>
													</div>
												
												<div class="writer_check">
                                                <span class="check_secret ">
                                                    <input type="checkbox" name="secret" id="secret" class="inp_secret" tabindex="4">
                                                    <label for="secret" class="lab_secret">
                                                        <span class="ico_skin ico_check"></span>
                                                        Secret
                                                    </label>
                                                </span>
												</div>
											

											<div class="reply_write ">
												<label for="comment" class="lab_write screen_out">내용</label>
												<textarea name="comment" id="comment" class="tf_reply" placeholder="여러분의 소중한 댓글을 입력해주세요" tabindex="3"></textarea>
											</div>

											<div class="writer_btn">
												<button type="submit" class="btn_enter" onclick="addComment(this, 81); return false;" tabindex="5">Send</button>
											</div>
										</fieldset>
									</form>
								</div><script type="text/javascript">loadedComments[81]=true;findFragmentAndHighlight(81)</script>
							</div>


						
					

					

					

					

					

					

					
						<div class="area_paging">
    					<span class="inner_paging">
                            <a href="https://sjh836.tistory.com/82" class="btn_prev "><span class="ico_skin ico_prev"></span>Prev</a>
    						
    							<a href="https://sjh836.tistory.com/173" class="link_page"><span>1</span></a>
    						
    							<a class="link_page"><span>···</span></a>
    						
    							<a href="https://sjh836.tistory.com/85" class="link_page"><span>89</span></a>
    						
    							<a href="https://sjh836.tistory.com/84" class="link_page"><span>90</span></a>
    						
    							<a href="https://sjh836.tistory.com/83" class="link_page"><span>91</span></a>
    						
    							<a href="https://sjh836.tistory.com/82" class="link_page"><span>92</span></a>
    						
    							<a class="link_page"><span class="selected">93</span></a>
    						
    							<a href="https://sjh836.tistory.com/80" class="link_page"><span>94</span></a>
    						
    							<a href="https://sjh836.tistory.com/79" class="link_page"><span>95</span></a>
    						
    							<a href="https://sjh836.tistory.com/78" class="link_page"><span>96</span></a>
    						
    							<a href="https://sjh836.tistory.com/77" class="link_page"><span>97</span></a>
    						
    							<a class="link_page"><span>···</span></a>
    						
    							<a href="https://sjh836.tistory.com/2" class="link_page"><span>164</span></a>
    						
                            <a href="https://sjh836.tistory.com/80" class="btn_next ">Next<span class="ico_skin ico_next"></span></a>
    					</span>
						</div>
					
				</div>
			</div>
		</div>
		<hr class="hide">
		<div id="dkFoot" role="contentinfo" class="area_foot">
			<small class="info_copyright">
				Blog is powered by
				<a href="http://www.kakaocorp.com/" class="emph_t" target="_blank">kakao</a> / Designed by
				<a href="http://www.tistory.com/" class="emph_t" target="_blank">Tistory</a>
			</small>
		</div>
	</div>



<script src="./HTTP 구조 (https, request, response, 주요 상태코드)_files/script.js.다운로드"></script>
<script type="text/javascript" src="./HTTP 구조 (https, request, response, 주요 상태코드)_files/wcslog.js.다운로드"></script>
<script type="text/javascript">
if(!wcs_add) var wcs_add = {};
wcs_add["wa"] = "92bf6f6d3e1280";
wcs_do();
</script>
<script src="./HTTP 구조 (https, request, response, 주요 상태코드)_files/search_dragselection.min.js.다운로드"></script>
<script>
    (function($) {
        $("body").bind('copy', function (e) {

            var url = document.location.href,
                decodedUrl = decodeURI(url),
                selection = window.getSelection();


            if (typeof window.getSelection == "undefined") {//IE8 or earlier...
                event.preventDefault();

                var pagelink = '\n\n 출처: ' + decodedUrl,
                    copytext = selection + pagelink;

                if (window.clipboardData) {
                    window.clipboardData.setData('Text', copytext);
                }
                return;
            }
            var body_element = document.getElementsByTagName('body')[0];

            //if the selection is short let's not annoy our users
            if (("" + selection).length < 30) return;

            //create a div outside of the visible area
            var newdiv = document.createElement('div');
            newdiv.style.position = 'absolute';
            newdiv.style.left = '-99999px';
            body_element.appendChild(newdiv);
            newdiv.appendChild(selection.getRangeAt(0).cloneContents());

            //we need a <pre> tag workaround
            //otherwise the text inside "pre" loses all the line breaks!
            if (selection.getRangeAt(0).commonAncestorContainer.nodeName == "PRE") {
                newdiv.innerHTML = "<pre>" + newdiv.innerHTML + "</pre>";
            }

            newdiv.innerHTML += '<br /><br />출처: <a href="' + url + '">' + decodedUrl + '</a> [빨간색코딩]';

            selection.selectAllChildren(newdiv);
            window.setTimeout(function () {
                body_element.removeChild(newdiv);
            }, 200);

        });
    })(tjQuery);
</script><script src="./HTTP 구조 (https, request, response, 주요 상태코드)_files/lightbox.min.js.다운로드"></script><div id="lightboxOverlay" class="lightboxOverlay" style="width: 1903px; height: 4830px; display: block;"></div><div id="lightbox" class="lightbox" style="top: 650px; left: 0px;"><div class="lb-outerContainer" style="width: 744px; height: 490px;"><div class="lb-container"><img class="lb-image" src="./HTTP 구조 (https, request, response, 주요 상태코드)_files/https.png" style="width: 736px; height: 482px;"><div class="lb-nav" style=""><a class="lb-prev" href="https://sjh836.tistory.com/81" style="display: none;"></a><a class="lb-next" href="https://sjh836.tistory.com/81" style="display: none;"></a></div><div class="lb-loader" style="display: none;"><a class="lb-cancel"></a></div></div></div><div class="lb-dataContainer" style="width: 744px;"><div class="lb-data"><div class="lb-details"><span class="lb-caption" style="display: none;"></span><span class="lb-number" style="display: none;"></span></div><div class="lb-closeContainer"><a class="lb-close"></a></div></div></div></div>
	<script>
	    lightbox.option({
			"fadeDuration": 200,
		    "resizeDuration": 200,
		    "wrapAround": false,
			"albumLabel": "%1 / %2",
			"fitImagesInViewport":true ,
			"stopEvent": false
	    })
	</script><script type="text/javascript">
var _tiq = 'undefined' !== typeof _tiq ? _tiq : [];
_tiq.push(['__setConfig', {enableScroll:true, enableClick:true, enableButton:true}]);
_tiq.push(["__setParam", "svcdomain", "user.tistory.com"]);
(function(d) {
	var se = d.createElement('script'); se.type = 'text/javascript'; se.async = true;
	se.src = location.protocol + '//m2.daumcdn.net/tiara/js/td.min.js';
	var s = d.getElementsByTagName('head')[0]; s.appendChild(se);
})(document);
_tiq.push(['__setParam', 'param_ex', JSON.stringify({"userId":"3499469","blogId":"2548253","entryId":"81"})]);
_tiq.push(['__trackPageview']);
_tiq.push(['__content', 't_content', {
'c_id':'2548253_81', 
'c_title':'HTTP 구조 (https, request, response, 주요 상태코드)', 
'type':'article', 
'author':'', 
'author_id':'3499469', 
'cp':'빨간색코딩', 
'cp_id':'2548253', 
'regdata':'2017-07-10 21:30:38', 
'plink':'https://sjh836.tistory.com/81', 
'media':'pcweb', 
}]);
var addEvent = function (evt, fn) { window.addEventListener ? window.addEventListener(evt, fn, false) : window.attachEvent('on' + evt, fn); };
var removeEvent = function(evt, fn) { window.removeEventListener ? window.removeEventListener(evt, fn, false) : window.detachEvent('on' + evt, fn);};
var ua = navigator.userAgent.toLowerCase(); var isIOS = /iP[ao]d|iPhone/i.test(ua);
var contentExStat = function() {
		_tiq.push(['__content', 't_content_ex', {
			'data_type':'usage'
, 'meta': {
'c_id':'2548253_81', 
'c_title':'HTTP 구조 (https, request, response, 주요 상태코드)', 
'type':'article', 
'author':'', 
'author_id':'3499469', 
'cp':'빨간색코딩', 
'cp_id':'2548253', 
'regdata':'2017-07-10 21:30:38', 
'plink':'https://sjh836.tistory.com/81', 
'media':'pcweb', 
}
}]);
		removeEvent(isIOS ? 'pagehide' : 'beforeunload', contentExStat);
};
addEvent(isIOS ? 'pagehide' : 'beforeunload', contentExStat);
</script>
<script type="text/javascript">window.roosevelt_params_queue = window.roosevelt_params_queue || []; window.roosevelt_params_queue.push({channel_id: "dk", channel_label: 'tistory'});</script>
<script type="text/javascript" src="./HTTP 구조 (https, request, response, 주요 상태코드)_files/roosevelt_dk_bt.js.다운로드" async=""></script><script type="text/javascript">if(window.console!=undefined){setTimeout(console.log.bind(console,"%cTISTORY","font:8em Arial;color:#EC6521;font-weight:bold"),0);setTimeout(console.log.bind(console,"%c  나를 표현하는 블로그","font:2em sans-serif;color:#333;"),0);}</script><iframe style="position:absolute;width:1px;height:1px;left:-100px;top:-100px" src="./HTTP 구조 (https, request, response, 주요 상태코드)_files/api.html" id="editEntry"></iframe><div id="layer_sns" class="layer_sns">
        <div class="bg_layer"></div>
        <ul class="list_sns">
            <li><a class="ico_sns ico_fb" data-service="facebook">페이스북 공유하기</a></li>
            <li><a class="ico_sns ico_kt" data-service="kakaotalk">카카오톡 공유하기</a></li>
            <li><a class="ico_sns ico_ks" data-service="kakaostory">카카오스토리 공유하기</a></li>
            <li><a class="ico_sns ico_tw" data-service="twitter">트위터 공유하기</a></li>
        </ul>
        <button type="button" class="btn_close"><span class="ico_sns ico_close">sns공유하기 레이어 닫기</span></button>
    </div>


</body></html>
