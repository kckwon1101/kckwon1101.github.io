---
title: 동작 파라미터화(Behavior Parameterizaion)
author: Kichang Kwon
date: 2020-11-20 17:10:00 +0900
categories: [Java, ModernJava]
tags: [behavior parameterizaion]
pin: true
---


### TEST

```java
    @GetMapping(value = "/child/storybook")
    public LrngResponse selStorybookCpltList() {

        ChildModel child = authService.getChildAuthentication();
        LrngRequest request = new LrngRequest();
        request.setLrngMemSeqno(child.getLrngMemSeqno());

        Map<String, Object> result = lrngService.selStorybookCpltList(request);

        return new LrngResponse(result);
    }
```
