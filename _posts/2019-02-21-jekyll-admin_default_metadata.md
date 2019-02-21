---
title: 지킬 포스트에 기본 메타데이터 적용하기
layout: post
keywords: jekyll, jekyll-admin
---

포스트를 쉽게 올리기 위해 지킬의 `jekyll-admin` 플러그인을 사용하던 중 매번 메타데이터를 입력해 줘야 하는 것이 불편하여, 기본 값을 적용하는 방법을 찾아보았다.

## 설정 전
이미 `layout`의 값을 `post`로 설정해야 되는 것을 알고 있는 상황임에도 매번 아래와 같이 메타데이터를 입력해 줘야 한다.

![기본 메타데이터 설정 전](/before_jekyll_admin.png)

## 설정 후
아래와 같이 `_config.yml`에 `defaults` 설정을 추가하면 된다.
```
defaults:
  -
    scope:
      path: ""
      type: "posts"
    values:
      layout: "post"
```

이제는 `keywords` 등 별도로 필요한 메타데이터만 편집을 하면 된다. :)