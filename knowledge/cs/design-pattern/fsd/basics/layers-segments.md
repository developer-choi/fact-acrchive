---
tags: [fsd, architecture, layers, responsibility]
---

# Questions
- [Could you explain the seven layers of FSD and the specific responsibility of each layer?](#could-you-explain-the-seven-layers-of-fsd-and-the-specific-responsibility-of-each-layer)
  - [What is the key difference between 'Entities' and 'Features' in FSD?](#what-is-the-key-difference-between-entities-and-features-in-fsd)
  - [[TODO] What is the key difference between 'App' and 'Pages' in FSD?](#todo-what-is-the-key-difference-between-app-and-pages-in-fsd)
- [What are segments in FSD, and what is the role of each one?](#what-are-segments-in-fsd-and-what-is-the-role-of-each-one)

---

# Answers

## Could you explain the seven layers of FSD and the specific responsibility of each layer?

### Keywords
FSD, Layers, Responsibility

### Official Answer
#### App
Everything that makes the app run — routing, entrypoints, global styles, providers.

#### Pages
Full pages or large parts of a page in nested routing.

#### Widgets
Large self-contained chunks of functionality or UI, usually delivering an entire use case.

#### Features
actions that bring business value to the user.

#### Entities
Business entities that the project works with, like user or product.

#### Shared
Reusable functionality, especially when it's detached from the specifics of the project/business, though not necessarily.

### Reference
- [Feature-Sliced Design Official Documentation](https://feature-sliced.design/docs/get-started/overview)

---

## What is the key difference between 'Entities' and 'Features' in FSD?
### Official Answer
An entity is a real-life concept that your app is working with. A feature is an interaction that provides real-life value to your app’s users, the thing people want to do with your entities.

> User Annotation
> - 엔티티는 명사, 개념, 데이터에 해당합니다. 따라서 데이터 타입, 타입을 가공하는 유틸리티, 데이터를 가져오는 GET API 호출 함수, 그리고 데이터를 단순히 보여주는 컴포넌트와 같은 코드들이 엔티티 레이어에 위치합니다.
> - 피처는 동사, 액션, 기능에 해당합니다. 따라서 실제 기능이 포함된 컴포넌트나 Hooks, 그리고 GET 이외의 API 호출 함수 등이 피처 레이어에 위치합니다.

### Reference
- [Feature-Sliced Design Official Documentation](https://feature-sliced.design/docs/get-started/overview)

---

## [TODO] What is the key difference between 'App' and 'Pages' in FSD?
### Keywords

### Official Answer

### Reference

---

## What are segments in FSD, and what is the role of each one?
### Official Answer
- **ui**: everything related to UI display: UI components, date formatters, styles, etc.
- **api**: backend interactions: request functions, data types, mappers, etc. / for code that handles rendering and appearance
- **model**: the data model: schemas, interfaces, stores, and business logic. / for storage and business logic
- **lib**: library code that other modules on this slice need.
- **config**: configuration files and feature flags. / for feature flags, environment variables and other forms of configuration