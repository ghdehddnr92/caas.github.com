---
title: System Entity
tags: [entity, basic]
keywords: Basic Conversation
summary: Dialogflow에서 기본적으로 제공해주는 시스템 Entity에 대해 소개합니다.
sidebar: chatbot_doc_sidebar
permalink: entity_system.html
folder: groupChatbot
previous: {
    title: Entity 만들기, 
    url: entity_custom.html
}
next: {
    title: API 이해하기,
    url: api_basic.html
}
---

## 시스템 Entity

**시스템 Entity**는 Chatbot(챗봇)에서 기본적으로 제공하는 Entity를 의미하며 최종 사용자 표현에서 일반적인 유형을 추출할 수 있도록 설정할 수 있습니다. <br/>
예를 들어 @sys.color 유형을 사용하여 '빨간색' 또는 '파란색'과 같은 값을 추출할 수 있습니다. <span style="color:#2c3238;"><i class="fa fa-external-link-square" aria-hidden="true" style="margin:0px 5px"></i>[시스템 Entity 참조](https://cloud.google.com/dialogflow/docs/entities-system)</span>에서 시스템 항목의 전체 목록을 확인할 수 있습니다.<br/>

시스템 Entity에서 제공하는 값은 대부분의 애플리케이션에서 제대로 작동합니다. 하지만 애플리케이션에서 시스템 Entity 값을 추가해야 할 수 있습니다. 예를 들어 @sys.color 값 목록에 '파란색-녹색'을 추가하려 할 수 있습니다. 일부 시스템 Entity은 이러한 용도로 확장 가능합니다.<br/>

그리고 시스템 Entity는 사용자 정의 Entity와 달리 사용자가 직접 생성/수정할 수 없으며, Intent 상세 화면에서 Parameter 설정을 통해 사용할 수 있습니다.<br/>
<!-- Intent 만들기에서 entity 매칭해주는 부분 -->

Chatbot에서 제공하는 주요 시스템 Entity는 다음과 같습니다.<br/>
- [날짜 Entity : sys.date]
- [시간 Entity : sys.time]
- [숫자 Entity : sys.number]
- [이름 Entity : sys.person]
- [언어 Entity : sys.language]
- [일반 Entity : sys.any, sys.color, sys.url]
<br/><br/>

### 시스템 Entity 예시 - 날짜 Entity

| Entity | 대표어 | 
|--------|-------|
| sys.date | 오늘, 내일, 모레, 어제, 그제, 3일 전, 3일 후 등 |

**날짜 Entity**는 날짜를 가리키는 단어를 구분합니다. 일, 월, 년에 대해 각각의 시스템 Entity를 제공합니다. <br/>

Intent에 날짜 Entity 타입의 Parameter를 추가하고 날짜 지칭 단어가 들어가는 문장을 입력하면 단어가 숫자값으로 변환되어 들어오는 것을 확인할 수 있습니다. '오늘', '당월', '올해'를 0으로 잡고 기준으로 부터 떨어진 날짜수를 계산하여 반환하게 됩니다.  