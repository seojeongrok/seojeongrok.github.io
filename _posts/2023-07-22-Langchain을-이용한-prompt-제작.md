---
title: Langchain을 이용한 prompt 제작
author: jeongrosk
date: 2023-07-22 14:27:00 +0800
categories: [Prompt, Langchain]
tags: [Prompt]
pin: true
---


## 좋은 Prompt의 조건
- **명확성(Clarity)**
    - Prompt는 명확하고 정확해야 한다. 
    - 불명확한 Prompt는 모델에게 혼란을 줄 수 있으며, 예상치 못한 결과를 초래할 수 있다.
    - LLM에게 무엇을 해야하는지 명확하게 설명해야 한다.
    - > Bad Example: "이야기를 써봐"
        {: .prompt-danger}
    - > Good Example: "과학 판타지 장르의 짧은 이야기를 써봐."
        {: .prompt-tip }

- **상세성(Detail)**
    - Prompt는 가능한 한 구체적이고 상세하게 요청되어야 한다. 
    - 모델에게 원하는 응답 유형을 명확하게 알려주는 프롬프트는 훨씬 더 유용한 결과를 가져올 수 있다.
    - **구체적이고 상세한 정보를 제공**해야 LLM에서 요청하는 업무에 대한 원하는 출력을 정확하게 이끌어낼 수 있다.
    - > Bad Example: "수학 문제를 풀어봐."
        {: .prompt-danger}
    - > Good Example: "다음의 2차 방정식을 풀어봐: 2x² - 3x - 5 = 0."
        {: .prompt-tip }

- **편향성(Bias)**
    - 좋은 Prompt는 중립적이어야 한다. 
    - 편향된 Prompt는 편향된 결과를 초래할 수 있습니다.
    - 선입견이 없어야 한다.
    - > Bad Example: "글로벌 온난화는 사기이다. 이에 대해 논해봐."
        {: .prompt-danger}
    - > Good Example: "글로벌 온난화에 대한 다양한 견해를 논해봐."
        {: .prompt-tip }

- **가독성(Readability)**
    - Prompt는 문법적으로 올바르고 가독성이 좋아야 한다. 
    - 문맥을 이해하기 어렵거나 복잡한 문장 구조를 가진 Prompt는 모델의 성능을 저하시킬 수 있다.
    - > Bad Example: "책 얘기 써서 미래 어떻게 될 지."
        {: .prompt-danger}
    - > Good Example: "미래의 사회를 상상하고 그에 대한 짧은 이야기를 써봐."
        {: .prompt-tip }

