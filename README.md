# Yandex Search Scraper

[![Promo](https://media.brightdata.com/2025/08/SERP-API-50-off-GitHub-banner_1389_166.png)](https://brightdata.co.kr/products/serp-api/yandex-search)

이 리포지토리는 Yandex Search Engine Results Pages(SERP)에서 데이터를 추출하기 위한 신뢰할 수 있는 두 가지 솔루션을 제공합니다:

- **무료 Yandex Scraper:** 소규모로 Yandex 검색 결과를 スクレイピング하기 위한 기본 도구입니다
- **엔터프라이즈급 Yandex SERP API:** 대용량, 실시간 데이터 추출을 위한 확장 가능하고 프로덕션 준비가 된 솔루션입니다([Bright Data's SERP Scraper API](https://brightdata.co.kr/products/serp-api)의 일부입니다)

## Table of Contents
- [Free Yandex SERP Scraper](#free-yandex-serp-scraper)
  - [Setup Requirements](#setup-requirements)
  - [Quick Start Guide](#quick-start-guide)
  - [Sample Output](#sample-output)
  - [Limitations](#limitations)
- [Yandex SERP Scraper API](#yandex-serp-scraper-api)
  - [Key Benefits](#key-benefits)
  - [Getting Started](#getting-started)
- [Implementation Methods](#implementation-methods)
  - [Direct API Access](#direct-api-access)
  - [Native Proxy-Based Access](#native-proxy-based-access)
- [Yandex Search Query Parameters](#yandex-search-query-parameters)
  - [Localization](#localization)
  - [Pagination](#pagination)
  - [Time Range](#time-range)
  - [Device Targeting](#device-targeting)
- [Practical Example](#practical-example)
- [Support & Resources](#support--resources)

## Free Yandex SERP Scraper

무료 스크레이퍼는 소규모로 Yandex SERP 데이터를 수집할 수 있는 간단한 방법을 제공합니다. 개인 프로젝트, 연구 또는 테스트 목적을 위해 제한된 데이터가 필요한 개발자에게 적합합니다.

<img width="800" alt="free-yandex-serp-scraper" src="https://github.com/luminati-io/yandex-api/blob/main/images/428371413-775c71f6-10cf-4a2d-91b8-6f137db5b171.png" />

### Setup Requirements

- [Python 3.9+](https://www.python.org/downloads/)
- 필수 패키지:
    - 브라우저 자동화를 위한 `playwright`
    - HTML 파싱을 위한 `BeautifulSoup`

```bash
pip install playwright beautifulsoup4
playwright install
```

> **Webスクレイピング이 처음이신가요?** [Beginner's Guide to Web Scraping with Python](https://brightdata.co.kr/blog/how-tos/web-scraping-with-python)을 확인해 보시기 바랍니다.
>

### Quick Start Guide

1. [yandex-search-results-scraper.py](https://github.com/luminati-io/yandex-api/blob/main/yandex-serp-scraper/yandex-serp-scraper.py)를 여십시오
2. 검색어 및 페이지 수 변수를 사용자 지정하십시오:

```python
PAGES_PER_TERM = {
    "ergonomic office chair": 2,
}
```

3. 스크립트를 실행하십시오

### Sample Output
<img width="800" alt="yandex-scraper-output" src="https://github.com/luminati-io/yandex-api/blob/main/images/428371812-dbd6f456-af64-4a4a-8735-f26876ae5fa8.png" />


### Limitations
Yandex를 スクレイピング할 때 가장 큰 과제 중 하나는 공격적인 CAPTCHA 보호입니다:

<img width="800" alt="yandex-captcha-challenge" src="https://github.com/luminati-io/yandex-api/blob/main/images/428371880-309e645f-c043-4231-aeb2-c3417e91b15e.png" />


Yandex는 자동화된 데이터 추출을 방지하기 위해 엄격하고 지속적으로 진화하는 アンチボット 시스템을 사용합니다. CAPTCHA가 자주 트리거되면 빠르게 IP 차단으로 이어질 수 있어, 안정적이고 장시간 실행되는 스크레이퍼를 유지하기가 어렵습니다.

무료 스크레이퍼는 기본 작업을 처리하지만, 다음과 같은 중요한 제한 사항이 있습니다:

- IP 차단 위험이 높습니다
- リクエスト 볼륨이 제한됩니다
- CAPTCHA 중단이 지속적으로 발생합니다
- 프로덕션 환경에 적합하지 않습니다

확장 가능하고 안정적인 솔루션을 원하신다면, 아래에 설명된 Bright Data의 전용 API를 고려해 보시기 바랍니다. 👇


## Yandex SERP Scraper API

[Yandex Search API](https://brightdata.co.kr/products/serp-api/yandex-search)는 Bright Data의 [SERP Scraping API](https://brightdata.co.kr/products/serp-api) 제품군의 일부입니다. 업계 선도적인 [プロキシ 인프라](https://brightdata.co.kr/proxy-types)를 활용하여 단 한 번의 API 호출로 실시간 Yandex 검색 결과를 제공합니다.

### Key Benefits

- **Global Accuracy**: 전 세계 특정 지역에 맞춘 결과를 얻을 수 있습니다
- **Pay-Per-Success**: 성공한 リクエスト에 대해서만 비용을 지불합니다
- **Real-Time Data**: 최신 검색 결과를 몇 초 내로 액세스할 수 있습니다
- **Unlimited Scalability**: 대용량 スクレイピング을 손쉽게 처리합니다
- **Cost-Efficient**: 비용이 많이 드는 인프라 필요성을 제거합니다
- **Reliable Performance**: 내장된 차단 방지 기술을 제공합니다
- **24/7 Expert Support**: 필요 시 언제든지 기술 지원을 받을 수 있습니다

 📌 Try Before You Buy: SERP API Live Demo에서 무료로 테스트해 보시기 바랍니다
 
 <img width="800" alt="bright-data-serp-api-playground" src="https://github.com/luminati-io/yandex-api/blob/main/images/428391143-c089343e-50a8-4961-8d11-d312982480df.png" />


### Getting Started

1. [Bright Data account를 생성](https://brightdata.co.kr/)하십시오(신규 사용자는 $5 크레딧을 받습니다)
2. [API key](https://docs.brightdata.com/general/account/api-token)를 생성하십시오
3. [단계별 가이드](https://github.com/luminati-io/yandex-api/blob/main/setup-serp-api-guide.md)를 따라 SERP API를 구성하십시오


## Implementation Methods

### Direct API Access

API를 사용하는 가장 간단한 방법은 Bright Data의 API エンドポイント로 직접 リクエスト를 보내는 것입니다.

**cURL Example:**

```bash
curl https://api.brightdata.com/request \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer API_TOKEN" \
  -d '{
        "zone": "ZONE_NAME",
        "url": "https://www.yandex.com/search/?text=apple+watch+series+10+review&lr=95&lang=en",
        "format": "raw"
      }'
```

**Python Example:**

```python
import requests
import json

url = "https://api.brightdata.com/request"

headers = {"Content-Type": "application/json", "Authorization": "Bearer API_TOKEN"}

payload = {
    "zone": "ZONE_NAME",
    "url": "https://www.yandex.com/search/?text=apple+watch+series+10+review&lr=95&lang=en",
    "format": "raw",
}

response = requests.post(url, headers=headers, json=payload)

with open("yandex-scraper-api-result.html", "w", encoding="utf-8") as file:
    file.write(response.text)

print("Response saved!")
```

### Native Proxy-Based Access

이 대체 방법은 검색 결과에 직접 액세스하기 위해 プロキシ 라우팅을 사용합니다.

**cURL Example:**

```bash
curl -i \
  --proxy brd.superproxy.io:33335 \
  --proxy-user brd-customer-<CUSTOMER_ID>-zone-<ZONE_NAME>:<ZONE_PASSWORD> \
  -k \
  "https://www.yandex.com/search/?text=apple+watch+series+10+review&lr=95&lang=en"
```

**Python Example:**

```python
import requests
import urllib3

urllib3.disable_warnings(urllib3.exceptions.InsecureRequestWarning)

host = "brd.superproxy.io"
port = 33335
username = "brd-customer-<customer_id>-zone-<zone_name>"
password = "<zone_password>"
proxy_url = f"http://{username}:{password}@{host}:{port}"

proxies = {"http": proxy_url, "https": proxy_url}

url = "https://www.yandex.com/search/?text=apple+watch+series+10+review&lr=95&lang=en"
response = requests.get(url, proxies=proxies, verify=False)

with open("yandex-scraper-api-result.html", "w", encoding="utf-8") as file:
    file.write(response.text)

print("Response saved!")
```

> **Note:** 네이티브 プロキシ 접근 방식을 사용할 때에는, 프로덕션 사용을 위해 Bright Data의 SSL 인증서를 설치하는 것을 권장합니다. 자세한 내용은 [SSL Certificate Guide](https://docs.brightdata.com/general/account/ssl-certificate)에서 확인하십시오.
> 

👉 [full HTML output](https://github.com/luminati-io/yandex-api/blob/main/yandex-scraper-api-output/yandex-scraper-api-result.html)을 확인해 보시기 바랍니다

*`lr` 및 `lang`과 같은 쿼리 パラメータ는 다음 섹션에서 설명합니다.*


## Yandex Search Query Parameters

### Localization

#### Region (`lr`)

이 パラメータ는 검색 결과에 대해 타겟팅할 지리적 지역 또는 국가를 정의합니다.

| Region | Code |
| --- | --- |
| Moscow | 1 |
| Saint-Petersburg | 2 |
| USA | 84 |
| Canada | 95 |
| China | 134 |

예시 - "best wireless earbuds"가 USA에서 어떻게 랭크되는지 확인하십시오:

```bash
curl --proxy brd.superproxy.io:33335 \
     --proxy-user brd-customer-<id>-zone-<zone>:<password> \
     "https://www.yandex.com/search/?text=best+wireless+earbuds&lr=84"
```

#### Language (`lang`)

두 글자 언어 코드를 사용하여 언어 선호도를 설정합니다:

- `lang=en` - 영어
- `lang=es` - 스페인어
- `lang=fr` - 프랑스어

예시 - 스페인어로 스포츠 뉴스를 가져옵니다:

```bash
https://www.yandex.com/search/?text=local+sports+news&lang=es
```

### Pagination

#### Page Number (`p`)

표시할 결과 페이지를 제어합니다:

- `p=0` - 첫 번째 페이지(기본값)
- `p=1` - 두 번째 페이지
- `p=4` - 다섯 번째 페이지

각 Yandex SERP 페이지는 일반적으로 10개의 결과를 반환합니다.

예시 - "nike running shoes"에 대해 3페이지(결과 21-30)를 スクレイピング하십시오:

```bash
https://www.yandex.com/search/?text=nike+running+shoes&p=2
```

### Time Range

#### Time Period (`within`)

결과를 특정 기간으로 제한합니다:

- `within=77` - 지난 24시간의 결과
- `within=1` - 지난 2주간의 결과
- `within=[%pm]` - 지난 한 달의 결과

예시 - 지난 24시간의 "iPhone 15 review" 결과를 가져옵니다:

```bash
https://www.yandex.com/search/?text=iphone+15+review&within=77
```

### Device Targeting

#### Device Type (`brd_mobile`)

시뮬레이션할 디바이스 유형을 지정합니다:

- `brd_mobile=0` 또는 생략 - 랜덤 데스크톱 user-agent
- `brd_mobile=1` - 랜덤 모바일 user-agent
- `brd_mobile=ios` 또는 `brd_mobile=iphone` - iPhone user-agent
- `brd_mobile=ipad` 또는 `brd_mobile=ios_tablet` - iPad user-agent
- `brd_mobile=android` - Android 폰 user-agent
- `brd_mobile=android_tablet` - Android 태블릿 user-agent

예시 - 반응형 웹사이트 테스트를 검색하는 iPhone을 시뮬레이션합니다:

```bash
https://www.yandex.com/search/?text=responsive+website+testing&brd_mobile=ios
```

#### Browser Type (`brd_browser`)

시뮬레이션할 브라우저를 정의합니다:

- 기본값(생략) - 랜덤 브라우저
- `brd_browser=chrome` - Google Chrome
- `brd_browser=safari` - Safari
- `brd_browser=firefox` - Mozilla Firefox

예시 - Python 튜토리얼을 검색하는 Safari 브라우저를 시뮬레이션합니다:

```bash
https://www.yandex.com/search/?text=how+to+learn+python&brd_browser=safari
```

> **Note:** `brd_browser=firefox`와 `brd_mobile=1`은 호환되지 않으므로 함께 사용하지 마십시오.
> 

## **Practical Example**

포괄적인 타겟팅을 위해 여러 パラメータ를 결합할 수 있습니다:

```bash
https://www.yandex.com/search/?text=organic+skincare+products
&lr=95
&lang=en
&p=2
&within=1
&brd_mobile=ios
&brd_browser=safari
```

이 검색은 다음을 수행합니다:

- 캐나다 사용자 타겟팅(`lr=95`)
- 영어 결과 표시(`lang=en`)
- 두 번째 페이지 표시(`p=2`)
- 지난 2주로 제한(`within=1`)
- iPhone 사용자 시뮬레이션(`brd_mobile=ios`)
- Safari 브라우저 사용(`brd_browser=safari`)

iOS 모바일 사용자가 보는 관점에서 캐나다 시장의 최근 유기농 제품 트렌드를 조사하려는 스킨케어 회사에 적합합니다.


## Support & Resources

- **Documentation:** [SERP API Documentation](https://docs.brightdata.com/scraping-automation/serp-api/)
- **Related APIs:**
    - [SERP API](https://github.com/luminati-io/serp-api)
    - [Google Search API](https://github.com/luminati-io/google-search-api)
    - [Google News Scraper](https://github.com/luminati-io/Google-News-Scraper)
    - [Google Trends API](https://github.com/luminati-io/google-trends-api)
    - [Google Reviews API](https://github.com/luminati-io/google-reviews-api)
    - [Google Hotels API](https://github.com/luminati-io/google-hotels-api)
    - [Google Flights API](https://github.com/luminati-io/google-flights-api)
    - [Web Unlocker API](https://github.com/luminati-io/web-unlocker-api)
- **Use Cases:**
    - [SEO & SERP Tracking](https://brightdata.co.kr/use-cases/serp-tracking)
    - [Travel Industry Data](https://brightdata.co.kr/use-cases/travel)
- **Additional Reading:** [Best SERP APIs](https://brightdata.co.kr/blog/web-data/best-serp-apis)
- **Contact Support:** [support@brightdata.com](mailto:support@brightdata.com)