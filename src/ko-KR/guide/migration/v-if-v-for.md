---
title: v-if와 v-for의 우선순위
badges:
- breaking
---

# {{ $frontmatter.title }} <migrationbadges badges="$frontmatter.badges"></migrationbadges>

## 개요

- **BREAKING**: 동일한 엘리먼트에 `v-if`와 `v-for`를 함께 사용할 때, `v-if`가 더 높은 우선순위를 갖습니다.

## 서론

Vue.js에서 가장 일반적으로 사용되는 두 가지 디렉티브는 `v-if`와 `v-for`입니다. 따라서 개발자 여러분이 두 디렉티브를 함께 사용하고자 하는 시기가 온 것은 놀랄 일이 아닙니다. 권장하는 방법은 아니지만, 필요한 경우가 있을 수 있기에, 두 디렉티브를 함께 사용할 때 어떻게 동작하는지에 대한 지침을 제공하고자 합니다.

## 2.x 구문

2.x에서는 동일한 엘리먼트에 `v-if`와 `v-for`를 함께 사용할 때, `v-for`가 더 높은 우선순위를 갖습니다.

## 3.x 구문

3.x에서는 `v-if`가 항상 `v-for` 보다 더 높은 우선순위를 갖습니다.

## 마이그레이션 방법

구문이 모호해지기 때문에 동일한 엘리먼트에 두 디렉티브를 함께 사용하지 않는 것이 좋습니다.

작업 수행을 위한 한 가지 방법은 두 디렉티브를 템플릿 수준에서 관리하는 대신, 표시할 엘리먼트 목록을 필터링하는 computed 속성을 만드는 것입니다.
