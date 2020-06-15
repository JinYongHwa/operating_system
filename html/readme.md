## index.html
``` html
<html>
<head>
	<meta charset='utf-8'>
	<title>진용화님의 프로필</title>
	<style>
		.container{
			width:800px;
			max-width:100%;
			margin:10px auto;
			padding-top:20px;
			padding-bottom:20px;
			border-top:5px solid #00ab44;
			border-bottom:5px solid #00ab44;

		}
		.profile{
			width:150px;
			height:150px;
			object-fit:cover;
			display:inline-block;
		}
		.name-container{
			display:inline-block;
		}
		.header{
			font-size:25px;
			font-weight:bold;
		}
		.sub-header{
			font-size:16px;
			color:#00ab44;
		}
		.address,.mobile,.email{
			font-size:14px;
			color:#555;
		}

		.tab-container{
			margin-top:20px;
		}
		.tab-container .tab-item{
			border-radius:4px;
			padding:5px 10px;
			display:inline-block;
			text-decoration:none;
			color:#555;

		}
		.tab-container .tab-item.active{
			color:#00ab44;
			font-weight:bold;

		}

		.section{
			margin-top:20px;
		}
		.section .section-header{
			font-size:20px;
			color: #00ab44;
			font-weight:bold;
			margin-bottom:10px;
		}
		.section .body{
			font-size:16px;
			font-weight:bold;
		}
		.section .sub-body{
			font-size:14px;
			margin-bottom:10px;
		}
	</style>
</head>
<body>
	<div class="container">
		<img src="/profile.jpg" class="profile">
		<div class="name-container">
				<div class="header">
					진용화
				</div>
				<div class="sub-header">
					명지전문대 정보통신과
				</div>
				<div class="address">
					서울시 노원구 월계동
				</div>
				<div class="mobile">
				010-2973-0833
				</div>
				<div class="email">
					yhjin@hhsoft.co.kr
				</div>
		</div>
		<div class="tab-container">
			<a class="tab-item active" href="/">
				프로필
			</a>
			<a class="tab-item" href="introduce.html">
				자기소개서
			</a>
		</div>


		<div class="section">
			<div class="section-header">기술</div>
			<div class="body">Ubuntu,Java,html,Css</div>
		</div>
		<div class="section">
			<div class="section-header">경력</div>
			<div class="body">명지전문대</div>
			<div class="sub-body">2019~ 현재</div>

			<div class="body">연합인포맥스</div>
			<div class="sub-body">2011년 ~ 2016년</div>
		</div>

		<div class="section">
			<div class="section-header">학력</div>
			<div class="body">명지전문대</div>
			<div class="sub-body">2019~ 현재</div>
		</div>

		<div class="section">
			<div class="section-header">수상내역</div>
			<div class="body">2016년 대한민국 컨텐츠 공모대전 최우수상</div>

		</div>
	</div>



</body>
</html>

```

## intorudce.html
``` html
<html>
<head>
	<meta charset='utf-8'>
	<title>진용화님의 프로필</title>
	<style>
		.container{
			width:800px;
			max-width:100%;
			margin:10px auto;
			padding-top:20px;
			padding-bottom:20px;
			border-top:5px solid #00ab44;
			border-bottom:5px solid #00ab44;

		}
		.profile{
			width:150px;
			height:150px;
			object-fit:cover;
			display:inline-block;
		}
		.name-container{
			display:inline-block;
		}
		.header{
			font-size:25px;
			font-weight:bold;
		}
		.sub-header{
			font-size:16px;
			color:#00ab44;
		}
		.address,.mobile,.email{
			font-size:14px;
			color:#555;
		}

		.tab-container{
			margin-top:20px;
		}
		.tab-container .tab-item{
			border-radius:4px;
			padding:5px 10px;
			display:inline-block;
			text-decoration:none;
			color:#555;

		}
		.tab-container .tab-item.active{
			color:#00ab44;
			font-weight:bold;

		}

		.section{
			margin-top:20px;
		}
		.section .section-header{
			font-size:20px;
			color: #00ab44;
			font-weight:bold;
			margin-bottom:10px;
		}
		.section .body{
			font-size:16px;
			font-weight:bold;
			white-space:pre-line;
			line-height:25px;
		}
		.section .sub-body{
			font-size:14px;
			margin-bottom:10px;
		}
	</style>
</head>
<body>
	<div class="container">
		<img src="/profile.jpg" class="profile">
		<div class="name-container">
				<div class="header">
					진용화
				</div>
				<div class="sub-header">
					명지전문대 정보통신과
				</div>
				<div class="address">
					서울시 노원구 월계동
				</div>
				<div class="mobile">
				010-2973-0833
				</div>
				<div class="email">
					yhjin@hhsoft.co.kr
				</div>
		</div>
		<div class="tab-container">
			<a class="tab-item " href="/">
				프로필
			</a>
			<a class="tab-item active" href="introduce.html">
				자기소개서
			</a>
		</div>


		<div class="section">
			<div class="section-header">자기소개</div>
			<div class="body">여행 동호회 운영진으로 활동하며 의사결정 시 다양한 측면을 이해하고 고려해야 한다는 것을 알게 되었습니다. 제가 맡은 역할은 정해진 예산 내에서 여행 코스를 소화할 수 있도록 일정을 조정하거나 비용 절감 방안을 찾는 것이었습니다. 한 달에 두 번씩 운영진이 모여서 회의를 진행하며 서로 다른 의견을 절충하고 해결안을 찾는 과정을 반복했습니다. 여행지 선정과 코스를 완성하기 위해 활용한 자료는 관광청 자료 및 지역 홍보 사이트, 기존 여행사 상품 안내서 등 구할 수 있는 자료를 최대한 활용하여 비교했습니다.
지난해 기획했던 여행 중에 의사결정이 어려웠던 적이 있습니다.

회원들의 부담을 줄이고 참여도를 높이기 위해 회비는 10만 원 이하로 정했고 그 안에서 1박 2일의 국내 여행 코스를 완성해야 했습니다.

서울을 기준으로 거리가 멀어지면 교통비만 10만 원 가까이 들게 되는 점을 고려하여 강원도 내에서 여행지를 선정하기로 했습니다. 그밖에 숙박비, 식비, 관광지 입장료를 고려하여 최종적으로 강릉으로 결정했습니다. 목장이 있는 대관령이나 설악산 등반을 할 수 있는 속초 등 다른 대안이 있었습니다. 그러나 저렴한 입장료로 즐길 수 있는 강릉 선교장, 음료도 마시고 해변 풍경도 볼 수 있는 카페 거리 등 가성비 좋은 여행 코스를 기획할 수 있는 강릉으로 정했습니다. 4월 초순이었기에 벚꽃 개화 시기와 맞추어서 경포대 벚꽃길을 코스에 추가하여 비용 절감을 할 수 있었습니다.


저는 동호회 운영진 활동을 통해 회비를 운용하는 방법과 의사결정 과정에서 서로 다른 생각을 조율하는 방법을 배웠습니다. 비용 절감뿐만 아니라 계절과 날씨의 특성, 구성원의 취향, 여행지 특성 등 다양한 상황을 고려하는 방법과 모든 사람을 만족하게 할 수는 없지만 한정된 자원 내에서 최대한 합리적으로 결정하고 수행하는 방식을 알게 되었습니다. 개인적인 흥미로 시작한 동호회 활동이었지만 자원 활용과 원활한 의사소통 능력을 길러주었기에 저에게는 의미 있는 활동이었다고 생각합니다.</div>
		</div>

	</div>



</body>
</html>

```
