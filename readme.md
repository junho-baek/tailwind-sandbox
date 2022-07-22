- [Tailwind Sandbox](#tailwind-sandbox)
- [tailwindcss-practice](#tailwindcss-practice)
- [section 1: Introduction](#section-1--introduction)
  - [1. Introduction](#1-introduction)
  - [2. Course Outline & Project](#2-course-outline---project)
  - [3. Project Links](#3-project-links)
  - [4. What is Tailwind CSS?](#4-what-is-tailwind-css-)
  - [5. Basic Environment Setup](#5-basic-environment-setup)
  - [6. Tailwind Sandbox Setup](#6-tailwind-sandbox-setup)
- [Section 2: Tailwind Fundamentals - Part 1](#section-2--tailwind-fundamentals---part-1)
  - [7. Utility-First Example](#7-utility-first-example)
  - [8. Working with Colors](#8-working-with-colors)
  - [9. Container & Spacing](#9-container---spacing)
  - [10. Typography](#10-typography)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>

# Tailwind Sandbox

This is part of my Tailwind From Scratch course. The sandbox contains around 20 different folders/files that focus on specific aspects/classes of Tailwind.

If you are taking the course, use the **"tailwind-sandbox-starter"** folder and work through the course with me. The **"tailwind-sandbox-done"** folder is obviously the finished code.

We are just using the Play CDN for this part of the course.

The main projects for the course will be in a different repo.

# tailwindcss-practice

# section 1: Introduction

## 1. Introduction

> 클래스 명으로 스타일을 추가하는 테일윈드 씨에스에스를 배워볼 것이다.

## 2. Course Outline & Project

> [https://tailwindfromscratch.com/#projects] 여기에서 이 강의의 프로젝트들을 프리뷰할 수 있다.

## 3. Project Links

Project Links
Course Links

Code & Demos:

Main Website With Project Demos - https://tailwindfromscratch.com

Code For Sandbox - https://github.com/bradtraversy/tailwind-sandbox

Code For All Projects - https://github.com/bradtraversy/tailwind-course-projects

Code For Simple Tailwind Starter - https://github.com/bradtraversy/simple-tailwind-starter

Documentation:

https://tailwindcss.com

Course Credit:

Traversy Media - https://traversymedia.com

Csaba Kissi Twitter - https://twitter.com/csaba_kissi

Frontend Mentor Website - https://frontendmentor.io

## 4. What is Tailwind CSS?

> 유틸리티 위주의 로우레벨 css 프레임워크이다.

> 미리 디자인된 컴포넌트가 있는 것은 아니다.

> 모든 사이트마다 유니크함을 지킬 수 있다. 유연성 때문

> 커스터마이징을 직접적으로 할 수 있다.

> css를 좀 아는 사람들한테 유리하다.

> html 에 너무 많은 class가 들어갈 수 있다.

> 미디어의 크기에 따른 크기조절이라든지, 호버시에 변경점이라든지 다 클래스로 이미 만들어져있다.

## 5. Basic Environment Setup

> vsc, node 등 이런저런 세팅 영상
> 나는 코드샌드박스를 씀

## 6. Tailwind Sandbox Setup

https://github.com/bradtraversy/tailwind-sandbox

https://pyppkx.csb.app/tailwind-sandbox-done/index.html

# Section 2: Tailwind Fundamentals - Part 1

## 7. Utility-First Example

> "flex items-center p-6 max-w-sm mx-auto bg-white rounded-xl shadow-xl space-x-4 mt-12"

- flex 박스
- justify items center
- padding 6
- max width small
- mx ; margin x축
- space x ; 안쪽 x값.. 왼쪽 기준인듯

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <script src="https://cdn.tailwindcss.com"></script>
    <title>Utility First Fundamentals</title>
    <style>
      body {
        margin-top: 200px !important;
      }
      .alert {
        display: flex;
        max-width: 24rem;
        margin: 0 auto;
        padding: 1.5rem;
        border-radius: 0.5rem;
        background-color: #fff;
        box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
      }
      .alert-logo-wrap {
        flex-shrink: 0;
      }
      .alert-logo {
        height: 3rem;
        width: 3rem;
      }
      .alert-body {
        margin-left: 1.5rem;
        padding-top: 0.25rem;
      }
      .alert-title {
        color: #1a202c;
        font-size: 1.25rem;
        line-height: 1.25;
        font-weight: 500;
      }
      .alert-message {
        color: #718096;
        font-size: 1rem;
        line-height: 1.5;
      }
    </style>
  </head>
  <body>
    <!-- HTML/CSS Version -->
    <div class="alert">
      <div class="alert-logo-wrap">
        <img class="alert-logo" src="../assets/img/warning.svg" alt="alert" />
      </div>
      <div class="alert-body">
        <h4 class="alert-title">Are You Sure?</h4>
        <p class="alert-message">You are about to delete a post</p>
      </div>
    </div>

    <!-- Tailwind Version -->
    <!-- 크기 구분 sm md lg xlg -->
    <div
      class="flex items-center p-6 max-w-sm mx-auto bg-white rounded-xl shadow-xl space-x-4 mt-12"
    >
      <img src="../assets/img/warning.svg" alt="" class="w-12 h-12" />
      <div>
        <div class="text-xl font-medium text-black">
          Are You Sure?
        </div>
        <p class="text-slate-500">You are about to delete a post</p>
      </div>
    </div>
  </body>
</html>
```

## 8. Working with Colors

> 컬러 속성 클래스에 대해 알아보자

```html
<body>
  <!-- Default colors -->
  <!-- white, black, red, green, blue, orange, yellow, purple, lime, emerald, teal, cyan, indigo, violet, fuchsia, pink, rose, sky, gray, slate, zinc, neutral, stone, amber,  -->

  <!-- Text Colors -->
  <!-- 검정과 화이트는 shade 옵션 -200 이런거 줄 수 없다. -->
  <p class="text-black">Tailwind is awesome</p>
  <p class="text-white">Tailwind is awesome</p>
  <!-- 일반적인 색상은 shade를 꼭 줘야한다. 50에서 900까지 줄 수 있다. -->
  <p class="text-red-50">Tailwind is awesome</p>
  <p class="text-red-900">Tailwind is awesome</p>
  <p class="text-green-500">Tailwind is awesome</p>
  <p class="text-emerald-500">Tailwind is awesome</p>
  <p class="text-zinc-300">Tailwind is awesome</p>
  <p class="text-slate-800">Tailwind is awesome</p>
  <!-- Background Colors -->
  <p class="bg-red-50">Tailwind is awesome</p>
  <p class="bg-red-900">Tailwind is awesome</p>
  <p class="bg-green-500">Tailwind is awesome</p>
  <p class="bg-emerald-500">Tailwind is awesome</p>
  <p class="bg-zinc-300">Tailwind is awesome</p>
  <p class="bg-slate-800 text-white">Tailwind is awesome</p>
  <!-- Text Underline -->
  <p class="underline decoration-zinc-300">Tailwind is awesome</p>
  <p class="underline decoration-red-300">Tailwind is awesome</p>
  <p class="underline decoration-blue-300">Tailwind is awesome</p>
  <!-- Border Colors -->
  <input type="text" class="border border-blue-300" />
  <input type="text" class="border border-orange-300" />
  <input type="text" class="border border-green-300" />
  <!-- Divide Colors -->
  <div class="divide-y divide-blue-300">
    <div>냐냐 1</div>
    <div>냐냐 2</div>
    <div>냐냐 3</div>
    <div>냐냐 4</div>
    <div>냐냐 5</div>
  </div>
  <!-- Outline Colors -->
  <button class="outline outline-red-500">Hello</button>
  <button class="outline outline-blue-500">Hello</button>
  <button class="outline outline-green-500">Hello</button>
  <!-- Box Shadow Colors (Opacity defaults to 100, but you can set it)-->
  <button class="shadow-lg bg-cyan-500 shadow-cyan-500">subscribe</button>
  <button
    class="shadow-lg bg-red-300 shadow-red-500 underline decoration-zinc-300 text-emerald-500"
  >
    subscribe
  </button>
  <!-- 분수꼴은 opacity를 나타낸다. 100에 가까울 수록 불투명도가 높아진다. -->
  <button class="shadow-lg bg-cyan-500 shadow-blue-500/50">subscribe</button>
  <button class="shadow-lg bg-cyan-500 shadow-blue-500/90">subscribe</button>
  <!-- Accent Colors -->
  <input type="checkbox" class="accent-purple-500" checked />
  <input type="checkbox" class="accent-blue-500" checked />
  <!-- Arbitrary Colors -->
  <div class="bg-[#427fab]">Hello</div>
  <div class="bg-[rgba(255,0,0,0.2)]">Hello</div>
  <div class="bg-[skyblue]">Hello</div>
</body>
```

## 9. Container & Spacing

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <script src="https://cdn.tailwindcss.com"></script>
    <title>Container & Spacing</title>
  </head>
  <body>
    <!-- Container -->
    <!-- break 포인트가 생긴다 -->
    <div class="container mx-auto">
      <article>
        <h3>Article One</h3>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit.
          Exercitationem laboriosam libero molestiae recusandae accusantium
          voluptates? Expedita dignissimos amet eveniet dolore nobis odio a
          sunt, maiores quasi. Modi amet quos dolores!
        </p>
      </article>

      <!-- Margin -->
      <div class="bg-red-100 m-2">Hello world</div>
      <div class="bg-red-100 ml-4">Hello world</div>
      <div class="bg-red-100 mr-4">Hello world</div>
      <div class="bg-red-100 mt-4">Hello world</div>
      <div class="bg-red-100 mb-4">Hello world</div>
      <!-- 이건 별로 추천하지 않음. 차라리 콘피그 설정 파일을 바꾸는걸 추천한다 -->
      <div class="bg-red-100 mt-[20px]">Hello world</div>
      <!-- Padding -->
      <div class="bg-red-100 p-2">Hello world</div>
      <div class="bg-red-100 pl-4">Hello world</div>
      <div class="bg-red-100 pr-4">Hello world</div>
      <div class="bg-red-100 pt-4">Hello world</div>
      <div class="bg-red-100 pb-4">Hello world</div>

      <div class="bg-red-100 pt-[20px]">Hello world</div>
      <!-- Space Between X -->
      <div class="flex mt-24 space-x-4">
        <div>Item 1</div>
        <div>Item 2</div>
        <div>Item 3</div>
        <div>Item 4</div>
        <div>Item 5</div>
        <div>Item 6</div>
        <div>Item 7</div>
      </div>
      <!-- Space Between Y -->
      <div class="flex flex-col mt-24 space-y-4">
        <div>Item 1</div>
        <div>Item 2</div>
        <div>Item 3</div>
        <div>Item 4</div>
        <div>Item 5</div>
        <div>Item 6</div>
        <div>Item 7</div>
      </div>
    </div>
  </body>
</html>

<!-- 브릭 포인트란 컨테이너의 레이아웃 옵션이 바뀌는 넓이를 뜻한다. -->
<!-- Breakpoinsts for Container 
    container	None	width: 100%;
    sm (640px)	    max-width: 640px;
    md (768px)	    max-width: 768px;
    lg (1024px)	    max-width: 1024px;
    xl (1280px)	    max-width: 1280px;
    2xl (1536px)	  max-width: 1536px; 
-->

<!-- Margin Values
      m-0	margin: 0px;
      mx-0	margin-left: 0px;
      margin-right: 0px;
      my-0	margin-top: 0px;
      margin-bottom: 0px;
      mt-0	margin-top: 0px;
      mr-0	margin-right: 0px;
      mb-0	margin-bottom: 0px;
      ml-0	margin-left: 0px;
      m-px	margin: 1px;
      mx-px	margin-left: 1px;
      margin-right: 1px;
      my-px	margin-top: 1px;
      margin-bottom: 1px;
      mt-px	margin-top: 1px;
      mr-px	margin-right: 1px;
      mb-px	margin-bottom: 1px;
      ml-px	margin-left: 1px;
      m-0.5	margin: 0.125rem; /* 2px */
      mx-0.5	margin-left: 0.125rem; /* 2px */
      margin-right: 0.125rem; /* 2px */
      my-0.5	margin-top: 0.125rem; /* 2px */
      margin-bottom: 0.125rem; /* 2px */
      mt-0.5	margin-top: 0.125rem; /* 2px */
      mr-0.5	margin-right: 0.125rem; /* 2px */
      mb-0.5	margin-bottom: 0.125rem; /* 2px */
      ml-0.5	margin-left: 0.125rem; /* 2px */
      m-1	margin: 0.25rem; /* 4px */
      mx-1	margin-left: 0.25rem; /* 4px */
      margin-right: 0.25rem; /* 4px */
      my-1	margin-top: 0.25rem; /* 4px */
      margin-bottom: 0.25rem; /* 4px */
      mt-1	margin-top: 0.25rem; /* 4px */
      mr-1	margin-right: 0.25rem; /* 4px */
      mb-1	margin-bottom: 0.25rem; /* 4px */
      ml-1	margin-left: 0.25rem; /* 4px */
      m-1.5	margin: 0.375rem; /* 6px */
      mx-1.5	margin-left: 0.375rem; /* 6px */
      margin-right: 0.375rem; /* 6px */
      my-1.5	margin-top: 0.375rem; /* 6px */
      margin-bottom: 0.375rem; /* 6px */
      mt-1.5	margin-top: 0.375rem; /* 6px */
      mr-1.5	margin-right: 0.375rem; /* 6px */
      mb-1.5	margin-bottom: 0.375rem; /* 6px */
      ml-1.5	margin-left: 0.375rem; /* 6px */
      m-2	margin: 0.5rem; /* 8px */
      mx-2	margin-left: 0.5rem; /* 8px */
      margin-right: 0.5rem; /* 8px */
      my-2	margin-top: 0.5rem; /* 8px */
      margin-bottom: 0.5rem; /* 8px */
      mt-2	margin-top: 0.5rem; /* 8px */
      mr-2	margin-right: 0.5rem; /* 8px */
      mb-2	margin-bottom: 0.5rem; /* 8px */
      ml-2	margin-left: 0.5rem; /* 8px */
      m-2.5	margin: 0.625rem; /* 10px */
      mx-2.5	margin-left: 0.625rem; /* 10px */
      margin-right: 0.625rem; /* 10px */
      my-2.5	margin-top: 0.625rem; /* 10px */
      margin-bottom: 0.625rem; /* 10px */
      mt-2.5	margin-top: 0.625rem; /* 10px */
      mr-2.5	margin-right: 0.625rem; /* 10px */
      mb-2.5	margin-bottom: 0.625rem; /* 10px */
      ml-2.5	margin-left: 0.625rem; /* 10px */
      m-3	margin: 0.75rem; /* 12px */
      mx-3	margin-left: 0.75rem; /* 12px */
      margin-right: 0.75rem; /* 12px */
      my-3	margin-top: 0.75rem; /* 12px */
      margin-bottom: 0.75rem; /* 12px */
      mt-3	margin-top: 0.75rem; /* 12px */
      mr-3	margin-right: 0.75rem; /* 12px */
      mb-3	margin-bottom: 0.75rem; /* 12px */
      ml-3	margin-left: 0.75rem; /* 12px */
      m-3.5	margin: 0.875rem; /* 14px */
      mx-3.5	margin-left: 0.875rem; /* 14px */
      margin-right: 0.875rem; /* 14px */
      my-3.5	margin-top: 0.875rem; /* 14px */
      margin-bottom: 0.875rem; /* 14px */
      mt-3.5	margin-top: 0.875rem; /* 14px */
      mr-3.5	margin-right: 0.875rem; /* 14px */
      mb-3.5	margin-bottom: 0.875rem; /* 14px */
      ml-3.5	margin-left: 0.875rem; /* 14px */
      m-4	margin: 1rem; /* 16px */
      mx-4	margin-left: 1rem; /* 16px */
      margin-right: 1rem; /* 16px */
      my-4	margin-top: 1rem; /* 16px */
      margin-bottom: 1rem; /* 16px */
      mt-4	margin-top: 1rem; /* 16px */
      mr-4	margin-right: 1rem; /* 16px */
      mb-4	margin-bottom: 1rem; /* 16px */
      ml-4	margin-left: 1rem; /* 16px */
      m-5	margin: 1.25rem; /* 20px */
      mx-5	margin-left: 1.25rem; /* 20px */
      margin-right: 1.25rem; /* 20px */
      my-5	margin-top: 1.25rem; /* 20px */
      margin-bottom: 1.25rem; /* 20px */
      mt-5	margin-top: 1.25rem; /* 20px */
      mr-5	margin-right: 1.25rem; /* 20px */
      mb-5	margin-bottom: 1.25rem; /* 20px */
      ml-5	margin-left: 1.25rem; /* 20px */
      m-6	margin: 1.5rem; /* 24px */
      mx-6	margin-left: 1.5rem; /* 24px */
      margin-right: 1.5rem; /* 24px */
      my-6	margin-top: 1.5rem; /* 24px */
      margin-bottom: 1.5rem; /* 24px */
      mt-6	margin-top: 1.5rem; /* 24px */
      mr-6	margin-right: 1.5rem; /* 24px */
      mb-6	margin-bottom: 1.5rem; /* 24px */
      ml-6	margin-left: 1.5rem; /* 24px */
      m-7	margin: 1.75rem; /* 28px */
      mx-7	margin-left: 1.75rem; /* 28px */
      margin-right: 1.75rem; /* 28px */
      my-7	margin-top: 1.75rem; /* 28px */
      margin-bottom: 1.75rem; /* 28px */
      mt-7	margin-top: 1.75rem; /* 28px */
      mr-7	margin-right: 1.75rem; /* 28px */
      mb-7	margin-bottom: 1.75rem; /* 28px */
      ml-7	margin-left: 1.75rem; /* 28px */
      m-8	margin: 2rem; /* 32px */
      mx-8	margin-left: 2rem; /* 32px */
      margin-right: 2rem; /* 32px */
      my-8	margin-top: 2rem; /* 32px */
      margin-bottom: 2rem; /* 32px */
      mt-8	margin-top: 2rem; /* 32px */
      mr-8	margin-right: 2rem; /* 32px */
      mb-8	margin-bottom: 2rem; /* 32px */
      ml-8	margin-left: 2rem; /* 32px */
      m-9	margin: 2.25rem; /* 36px */
      mx-9	margin-left: 2.25rem; /* 36px */
      margin-right: 2.25rem; /* 36px */
      my-9	margin-top: 2.25rem; /* 36px */
      margin-bottom: 2.25rem; /* 36px */
      mt-9	margin-top: 2.25rem; /* 36px */
      mr-9	margin-right: 2.25rem; /* 36px */
      mb-9	margin-bottom: 2.25rem; /* 36px */
      ml-9	margin-left: 2.25rem; /* 36px */
      m-10	margin: 2.5rem; /* 40px */
      mx-10	margin-left: 2.5rem; /* 40px */
      margin-right: 2.5rem; /* 40px */
      my-10	margin-top: 2.5rem; /* 40px */
      margin-bottom: 2.5rem; /* 40px */
      mt-10	margin-top: 2.5rem; /* 40px */
      mr-10	margin-right: 2.5rem; /* 40px */
      mb-10	margin-bottom: 2.5rem; /* 40px */
      ml-10	margin-left: 2.5rem; /* 40px */
      m-11	margin: 2.75rem; /* 44px */
      mx-11	margin-left: 2.75rem; /* 44px */
      margin-right: 2.75rem; /* 44px */
      my-11	margin-top: 2.75rem; /* 44px */
      margin-bottom: 2.75rem; /* 44px */
      mt-11	margin-top: 2.75rem; /* 44px */
      mr-11	margin-right: 2.75rem; /* 44px */
      mb-11	margin-bottom: 2.75rem; /* 44px */
      ml-11	margin-left: 2.75rem; /* 44px */
      m-12	margin: 3rem; /* 48px */
      mx-12	margin-left: 3rem; /* 48px */
      margin-right: 3rem; /* 48px */
      my-12	margin-top: 3rem; /* 48px */
      margin-bottom: 3rem; /* 48px */
      mt-12	margin-top: 3rem; /* 48px */
      mr-12	margin-right: 3rem; /* 48px */
      mb-12	margin-bottom: 3rem; /* 48px */
      ml-12	margin-left: 3rem; /* 48px */
      m-14	margin: 3.5rem; /* 56px */
      mx-14	margin-left: 3.5rem; /* 56px */
      margin-right: 3.5rem; /* 56px */
      my-14	margin-top: 3.5rem; /* 56px */
      margin-bottom: 3.5rem; /* 56px */
      mt-14	margin-top: 3.5rem; /* 56px */
      mr-14	margin-right: 3.5rem; /* 56px */
      mb-14	margin-bottom: 3.5rem; /* 56px */
      ml-14	margin-left: 3.5rem; /* 56px */
      m-16	margin: 4rem; /* 64px */
      mx-16	margin-left: 4rem; /* 64px */
      margin-right: 4rem; /* 64px */
      my-16	margin-top: 4rem; /* 64px */
      margin-bottom: 4rem; /* 64px */
      mt-16	margin-top: 4rem; /* 64px */
      mr-16	margin-right: 4rem; /* 64px */
      mb-16	margin-bottom: 4rem; /* 64px */
      ml-16	margin-left: 4rem; /* 64px */
      m-20	margin: 5rem; /* 80px */
      mx-20	margin-left: 5rem; /* 80px */
      margin-right: 5rem; /* 80px */
      my-20	margin-top: 5rem; /* 80px */
      margin-bottom: 5rem; /* 80px */
      mt-20	margin-top: 5rem; /* 80px */
      mr-20	margin-right: 5rem; /* 80px */
      mb-20	margin-bottom: 5rem; /* 80px */
      ml-20	margin-left: 5rem; /* 80px */
      m-24	margin: 6rem; /* 96px */
      mx-24	margin-left: 6rem; /* 96px */
      margin-right: 6rem; /* 96px */
      my-24	margin-top: 6rem; /* 96px */
      margin-bottom: 6rem; /* 96px */
      mt-24	margin-top: 6rem; /* 96px */
      mr-24	margin-right: 6rem; /* 96px */
      mb-24	margin-bottom: 6rem; /* 96px */
      ml-24	margin-left: 6rem; /* 96px */
      m-28	margin: 7rem; /* 112px */
      mx-28	margin-left: 7rem; /* 112px */
      margin-right: 7rem; /* 112px */
      my-28	margin-top: 7rem; /* 112px */
      margin-bottom: 7rem; /* 112px */
      mt-28	margin-top: 7rem; /* 112px */
      mr-28	margin-right: 7rem; /* 112px */
      mb-28	margin-bottom: 7rem; /* 112px */
      ml-28	margin-left: 7rem; /* 112px */
      m-32	margin: 8rem; /* 128px */
      mx-32	margin-left: 8rem; /* 128px */
      margin-right: 8rem; /* 128px */
      my-32	margin-top: 8rem; /* 128px */
      margin-bottom: 8rem; /* 128px */
      mt-32	margin-top: 8rem; /* 128px */
      mr-32	margin-right: 8rem; /* 128px */
      mb-32	margin-bottom: 8rem; /* 128px */
      ml-32	margin-left: 8rem; /* 128px */
      m-36	margin: 9rem; /* 144px */
      mx-36	margin-left: 9rem; /* 144px */
      margin-right: 9rem; /* 144px */
      my-36	margin-top: 9rem; /* 144px */
      margin-bottom: 9rem; /* 144px */
      mt-36	margin-top: 9rem; /* 144px */
      mr-36	margin-right: 9rem; /* 144px */
      mb-36	margin-bottom: 9rem; /* 144px */
      ml-36	margin-left: 9rem; /* 144px */
      m-40	margin: 10rem; /* 160px */
      mx-40	margin-left: 10rem; /* 160px */
      margin-right: 10rem; /* 160px */
      my-40	margin-top: 10rem; /* 160px */
      margin-bottom: 10rem; /* 160px */
      mt-40	margin-top: 10rem; /* 160px */
      mr-40	margin-right: 10rem; /* 160px */
      mb-40	margin-bottom: 10rem; /* 160px */
      ml-40	margin-left: 10rem; /* 160px */
      m-44	margin: 11rem; /* 176px */
      mx-44	margin-left: 11rem; /* 176px */
      margin-right: 11rem; /* 176px */
      my-44	margin-top: 11rem; /* 176px */
      margin-bottom: 11rem; /* 176px */
      mt-44	margin-top: 11rem; /* 176px */
      mr-44	margin-right: 11rem; /* 176px */
      mb-44	margin-bottom: 11rem; /* 176px */
      ml-44	margin-left: 11rem; /* 176px */
      m-48	margin: 12rem; /* 192px */
      mx-48	margin-left: 12rem; /* 192px */
      margin-right: 12rem; /* 192px */
      my-48	margin-top: 12rem; /* 192px */
      margin-bottom: 12rem; /* 192px */
      mt-48	margin-top: 12rem; /* 192px */
      mr-48	margin-right: 12rem; /* 192px */
      mb-48	margin-bottom: 12rem; /* 192px */
      ml-48	margin-left: 12rem; /* 192px */
      m-52	margin: 13rem; /* 208px */
      mx-52	margin-left: 13rem; /* 208px */
      margin-right: 13rem; /* 208px */
      my-52	margin-top: 13rem; /* 208px */
      margin-bottom: 13rem; /* 208px */
      mt-52	margin-top: 13rem; /* 208px */
      mr-52	margin-right: 13rem; /* 208px */
      mb-52	margin-bottom: 13rem; /* 208px */
      ml-52	margin-left: 13rem; /* 208px */
      m-56	margin: 14rem; /* 224px */
      mx-56	margin-left: 14rem; /* 224px */
      margin-right: 14rem; /* 224px */
      my-56	margin-top: 14rem; /* 224px */
      margin-bottom: 14rem; /* 224px */
      mt-56	margin-top: 14rem; /* 224px */
      mr-56	margin-right: 14rem; /* 224px */
      mb-56	margin-bottom: 14rem; /* 224px */
      ml-56	margin-left: 14rem; /* 224px */
      m-60	margin: 15rem; /* 240px */
      mx-60	margin-left: 15rem; /* 240px */
      margin-right: 15rem; /* 240px */
      my-60	margin-top: 15rem; /* 240px */
      margin-bottom: 15rem; /* 240px */
      mt-60	margin-top: 15rem; /* 240px */
      mr-60	margin-right: 15rem; /* 240px */
      mb-60	margin-bottom: 15rem; /* 240px */
      ml-60	margin-left: 15rem; /* 240px */
      m-64	margin: 16rem; /* 256px */
      mx-64	margin-left: 16rem; /* 256px */
      margin-right: 16rem; /* 256px */
      my-64	margin-top: 16rem; /* 256px */
      margin-bottom: 16rem; /* 256px */
      mt-64	margin-top: 16rem; /* 256px */
      mr-64	margin-right: 16rem; /* 256px */
      mb-64	margin-bottom: 16rem; /* 256px */
      ml-64	margin-left: 16rem; /* 256px */
      m-72	margin: 18rem; /* 288px */
      mx-72	margin-left: 18rem; /* 288px */
      margin-right: 18rem; /* 288px */
      my-72	margin-top: 18rem; /* 288px */
      margin-bottom: 18rem; /* 288px */
      mt-72	margin-top: 18rem; /* 288px */
      mr-72	margin-right: 18rem; /* 288px */
      mb-72	margin-bottom: 18rem; /* 288px */
      ml-72	margin-left: 18rem; /* 288px */
      m-80	margin: 20rem; /* 320px */
      mx-80	margin-left: 20rem; /* 320px */
      margin-right: 20rem; /* 320px */
      my-80	margin-top: 20rem; /* 320px */
      margin-bottom: 20rem; /* 320px */
      mt-80	margin-top: 20rem; /* 320px */
      mr-80	margin-right: 20rem; /* 320px */
      mb-80	margin-bottom: 20rem; /* 320px */
      ml-80	margin-left: 20rem; /* 320px */
      m-96	margin: 24rem; /* 384px */
      mx-96	margin-left: 24rem; /* 384px */
      margin-right: 24rem; /* 384px */
      my-96	margin-top: 24rem; /* 384px */
      margin-bottom: 24rem; /* 384px */
      mt-96	margin-top: 24rem; /* 384px */
      mr-96	margin-right: 24rem; /* 384px */
      mb-96	margin-bottom: 24rem; /* 384px */
      ml-96	margin-left: 24rem; /* 384px */
      m-auto	margin: auto;
      mx-auto	margin-left: auto;
      margin-right: auto;
      my-auto	margin-top: auto;
      margin-bottom: auto;
      mt-auto	margin-top: auto;
      mr-auto	margin-right: auto;
      mb-auto	margin-bottom: auto;
      ml-auto	margin-left: auto; 
    -->

<!-- Padding Values
      p-0	padding: 0px;
      px-0	padding-left: 0px;
      padding-right: 0px;
      py-0	padding-top: 0px;
      padding-bottom: 0px;
      pt-0	padding-top: 0px;
      pr-0	padding-right: 0px;
      pb-0	padding-bottom: 0px;
      pl-0	padding-left: 0px;
      p-px	padding: 1px;
      px-px	padding-left: 1px;
      padding-right: 1px;
      py-px	padding-top: 1px;
      padding-bottom: 1px;
      pt-px	padding-top: 1px;
      pr-px	padding-right: 1px;
      pb-px	padding-bottom: 1px;
      pl-px	padding-left: 1px;
      p-0.5	padding: 0.125rem; /* 2px */
      px-0.5	padding-left: 0.125rem; /* 2px */
      padding-right: 0.125rem; /* 2px */
      py-0.5	padding-top: 0.125rem; /* 2px */
      padding-bottom: 0.125rem; /* 2px */
      pt-0.5	padding-top: 0.125rem; /* 2px */
      pr-0.5	padding-right: 0.125rem; /* 2px */
      pb-0.5	padding-bottom: 0.125rem; /* 2px */
      pl-0.5	padding-left: 0.125rem; /* 2px */
      p-1	padding: 0.25rem; /* 4px */
      px-1	padding-left: 0.25rem; /* 4px */
      padding-right: 0.25rem; /* 4px */
      py-1	padding-top: 0.25rem; /* 4px */
      padding-bottom: 0.25rem; /* 4px */
      pt-1	padding-top: 0.25rem; /* 4px */
      pr-1	padding-right: 0.25rem; /* 4px */
      pb-1	padding-bottom: 0.25rem; /* 4px */
      pl-1	padding-left: 0.25rem; /* 4px */
      p-1.5	padding: 0.375rem; /* 6px */
      px-1.5	padding-left: 0.375rem; /* 6px */
      padding-right: 0.375rem; /* 6px */
      py-1.5	padding-top: 0.375rem; /* 6px */
      padding-bottom: 0.375rem; /* 6px */
      pt-1.5	padding-top: 0.375rem; /* 6px */
      pr-1.5	padding-right: 0.375rem; /* 6px */
      pb-1.5	padding-bottom: 0.375rem; /* 6px */
      pl-1.5	padding-left: 0.375rem; /* 6px */
      p-2	padding: 0.5rem; /* 8px */
      px-2	padding-left: 0.5rem; /* 8px */
      padding-right: 0.5rem; /* 8px */
      py-2	padding-top: 0.5rem; /* 8px */
      padding-bottom: 0.5rem; /* 8px */
      pt-2	padding-top: 0.5rem; /* 8px */
      pr-2	padding-right: 0.5rem; /* 8px */
      pb-2	padding-bottom: 0.5rem; /* 8px */
      pl-2	padding-left: 0.5rem; /* 8px */
      p-2.5	padding: 0.625rem; /* 10px */
      px-2.5	padding-left: 0.625rem; /* 10px */
      padding-right: 0.625rem; /* 10px */
      py-2.5	padding-top: 0.625rem; /* 10px */
      padding-bottom: 0.625rem; /* 10px */
      pt-2.5	padding-top: 0.625rem; /* 10px */
      pr-2.5	padding-right: 0.625rem; /* 10px */
      pb-2.5	padding-bottom: 0.625rem; /* 10px */
      pl-2.5	padding-left: 0.625rem; /* 10px */
      p-3	padding: 0.75rem; /* 12px */
      px-3	padding-left: 0.75rem; /* 12px */
      padding-right: 0.75rem; /* 12px */
      py-3	padding-top: 0.75rem; /* 12px */
      padding-bottom: 0.75rem; /* 12px */
      pt-3	padding-top: 0.75rem; /* 12px */
      pr-3	padding-right: 0.75rem; /* 12px */
      pb-3	padding-bottom: 0.75rem; /* 12px */
      pl-3	padding-left: 0.75rem; /* 12px */
      p-3.5	padding: 0.875rem; /* 14px */
      px-3.5	padding-left: 0.875rem; /* 14px */
      padding-right: 0.875rem; /* 14px */
      py-3.5	padding-top: 0.875rem; /* 14px */
      padding-bottom: 0.875rem; /* 14px */
      pt-3.5	padding-top: 0.875rem; /* 14px */
      pr-3.5	padding-right: 0.875rem; /* 14px */
      pb-3.5	padding-bottom: 0.875rem; /* 14px */
      pl-3.5	padding-left: 0.875rem; /* 14px */
      p-4	padding: 1rem; /* 16px */
      px-4	padding-left: 1rem; /* 16px */
      padding-right: 1rem; /* 16px */
      py-4	padding-top: 1rem; /* 16px */
      padding-bottom: 1rem; /* 16px */
      pt-4	padding-top: 1rem; /* 16px */
      pr-4	padding-right: 1rem; /* 16px */
      pb-4	padding-bottom: 1rem; /* 16px */
      pl-4	padding-left: 1rem; /* 16px */
      p-5	padding: 1.25rem; /* 20px */
      px-5	padding-left: 1.25rem; /* 20px */
      padding-right: 1.25rem; /* 20px */
      py-5	padding-top: 1.25rem; /* 20px */
      padding-bottom: 1.25rem; /* 20px */
      pt-5	padding-top: 1.25rem; /* 20px */
      pr-5	padding-right: 1.25rem; /* 20px */
      pb-5	padding-bottom: 1.25rem; /* 20px */
      pl-5	padding-left: 1.25rem; /* 20px */
      p-6	padding: 1.5rem; /* 24px */
      px-6	padding-left: 1.5rem; /* 24px */
      padding-right: 1.5rem; /* 24px */
      py-6	padding-top: 1.5rem; /* 24px */
      padding-bottom: 1.5rem; /* 24px */
      pt-6	padding-top: 1.5rem; /* 24px */
      pr-6	padding-right: 1.5rem; /* 24px */
      pb-6	padding-bottom: 1.5rem; /* 24px */
      pl-6	padding-left: 1.5rem; /* 24px */
      p-7	padding: 1.75rem; /* 28px */
      px-7	padding-left: 1.75rem; /* 28px */
      padding-right: 1.75rem; /* 28px */
      py-7	padding-top: 1.75rem; /* 28px */
      padding-bottom: 1.75rem; /* 28px */
      pt-7	padding-top: 1.75rem; /* 28px */
      pr-7	padding-right: 1.75rem; /* 28px */
      pb-7	padding-bottom: 1.75rem; /* 28px */
      pl-7	padding-left: 1.75rem; /* 28px */
      p-8	padding: 2rem; /* 32px */
      px-8	padding-left: 2rem; /* 32px */
      padding-right: 2rem; /* 32px */
      py-8	padding-top: 2rem; /* 32px */
      padding-bottom: 2rem; /* 32px */
      pt-8	padding-top: 2rem; /* 32px */
      pr-8	padding-right: 2rem; /* 32px */
      pb-8	padding-bottom: 2rem; /* 32px */
      pl-8	padding-left: 2rem; /* 32px */
      p-9	padding: 2.25rem; /* 36px */
      px-9	padding-left: 2.25rem; /* 36px */
      padding-right: 2.25rem; /* 36px */
      py-9	padding-top: 2.25rem; /* 36px */
      padding-bottom: 2.25rem; /* 36px */
      pt-9	padding-top: 2.25rem; /* 36px */
      pr-9	padding-right: 2.25rem; /* 36px */
      pb-9	padding-bottom: 2.25rem; /* 36px */
      pl-9	padding-left: 2.25rem; /* 36px */
      p-10	padding: 2.5rem; /* 40px */
      px-10	padding-left: 2.5rem; /* 40px */
      padding-right: 2.5rem; /* 40px */
      py-10	padding-top: 2.5rem; /* 40px */
      padding-bottom: 2.5rem; /* 40px */
      pt-10	padding-top: 2.5rem; /* 40px */
      pr-10	padding-right: 2.5rem; /* 40px */
      pb-10	padding-bottom: 2.5rem; /* 40px */
      pl-10	padding-left: 2.5rem; /* 40px */
      p-11	padding: 2.75rem; /* 44px */
      px-11	padding-left: 2.75rem; /* 44px */
      padding-right: 2.75rem; /* 44px */
      py-11	padding-top: 2.75rem; /* 44px */
      padding-bottom: 2.75rem; /* 44px */
      pt-11	padding-top: 2.75rem; /* 44px */
      pr-11	padding-right: 2.75rem; /* 44px */
      pb-11	padding-bottom: 2.75rem; /* 44px */
      pl-11	padding-left: 2.75rem; /* 44px */
      p-12	padding: 3rem; /* 48px */
      px-12	padding-left: 3rem; /* 48px */
      padding-right: 3rem; /* 48px */
      py-12	padding-top: 3rem; /* 48px */
      padding-bottom: 3rem; /* 48px */
      pt-12	padding-top: 3rem; /* 48px */
      pr-12	padding-right: 3rem; /* 48px */
      pb-12	padding-bottom: 3rem; /* 48px */
      pl-12	padding-left: 3rem; /* 48px */
      p-14	padding: 3.5rem; /* 56px */
      px-14	padding-left: 3.5rem; /* 56px */
      padding-right: 3.5rem; /* 56px */
      py-14	padding-top: 3.5rem; /* 56px */
      padding-bottom: 3.5rem; /* 56px */
      pt-14	padding-top: 3.5rem; /* 56px */
      pr-14	padding-right: 3.5rem; /* 56px */
      pb-14	padding-bottom: 3.5rem; /* 56px */
      pl-14	padding-left: 3.5rem; /* 56px */
      p-16	padding: 4rem; /* 64px */
      px-16	padding-left: 4rem; /* 64px */
      padding-right: 4rem; /* 64px */
      py-16	padding-top: 4rem; /* 64px */
      padding-bottom: 4rem; /* 64px */
      pt-16	padding-top: 4rem; /* 64px */
      pr-16	padding-right: 4rem; /* 64px */
      pb-16	padding-bottom: 4rem; /* 64px */
      pl-16	padding-left: 4rem; /* 64px */
      p-20	padding: 5rem; /* 80px */
      px-20	padding-left: 5rem; /* 80px */
      padding-right: 5rem; /* 80px */
      py-20	padding-top: 5rem; /* 80px */
      padding-bottom: 5rem; /* 80px */
      pt-20	padding-top: 5rem; /* 80px */
      pr-20	padding-right: 5rem; /* 80px */
      pb-20	padding-bottom: 5rem; /* 80px */
      pl-20	padding-left: 5rem; /* 80px */
      p-24	padding: 6rem; /* 96px */
      px-24	padding-left: 6rem; /* 96px */
      padding-right: 6rem; /* 96px */
      py-24	padding-top: 6rem; /* 96px */
      padding-bottom: 6rem; /* 96px */
      pt-24	padding-top: 6rem; /* 96px */
      pr-24	padding-right: 6rem; /* 96px */
      pb-24	padding-bottom: 6rem; /* 96px */
      pl-24	padding-left: 6rem; /* 96px */
      p-28	padding: 7rem; /* 112px */
      px-28	padding-left: 7rem; /* 112px */
      padding-right: 7rem; /* 112px */
      py-28	padding-top: 7rem; /* 112px */
      padding-bottom: 7rem; /* 112px */
      pt-28	padding-top: 7rem; /* 112px */
      pr-28	padding-right: 7rem; /* 112px */
      pb-28	padding-bottom: 7rem; /* 112px */
      pl-28	padding-left: 7rem; /* 112px */
      p-32	padding: 8rem; /* 128px */
      px-32	padding-left: 8rem; /* 128px */
      padding-right: 8rem; /* 128px */
      py-32	padding-top: 8rem; /* 128px */
      padding-bottom: 8rem; /* 128px */
      pt-32	padding-top: 8rem; /* 128px */
      pr-32	padding-right: 8rem; /* 128px */
      pb-32	padding-bottom: 8rem; /* 128px */
      pl-32	padding-left: 8rem; /* 128px */
      p-36	padding: 9rem; /* 144px */
      px-36	padding-left: 9rem; /* 144px */
      padding-right: 9rem; /* 144px */
      py-36	padding-top: 9rem; /* 144px */
      padding-bottom: 9rem; /* 144px */
      pt-36	padding-top: 9rem; /* 144px */
      pr-36	padding-right: 9rem; /* 144px */
      pb-36	padding-bottom: 9rem; /* 144px */
      pl-36	padding-left: 9rem; /* 144px */
      p-40	padding: 10rem; /* 160px */
      px-40	padding-left: 10rem; /* 160px */
      padding-right: 10rem; /* 160px */
      py-40	padding-top: 10rem; /* 160px */
      padding-bottom: 10rem; /* 160px */
      pt-40	padding-top: 10rem; /* 160px */
      pr-40	padding-right: 10rem; /* 160px */
      pb-40	padding-bottom: 10rem; /* 160px */
      pl-40	padding-left: 10rem; /* 160px */
      p-44	padding: 11rem; /* 176px */
      px-44	padding-left: 11rem; /* 176px */
      padding-right: 11rem; /* 176px */
      py-44	padding-top: 11rem; /* 176px */
      padding-bottom: 11rem; /* 176px */
      pt-44	padding-top: 11rem; /* 176px */
      pr-44	padding-right: 11rem; /* 176px */
      pb-44	padding-bottom: 11rem; /* 176px */
      pl-44	padding-left: 11rem; /* 176px */
      p-48	padding: 12rem; /* 192px */
      px-48	padding-left: 12rem; /* 192px */
      padding-right: 12rem; /* 192px */
      py-48	padding-top: 12rem; /* 192px */
      padding-bottom: 12rem; /* 192px */
      pt-48	padding-top: 12rem; /* 192px */
      pr-48	padding-right: 12rem; /* 192px */
      pb-48	padding-bottom: 12rem; /* 192px */
      pl-48	padding-left: 12rem; /* 192px */
      p-52	padding: 13rem; /* 208px */
      px-52	padding-left: 13rem; /* 208px */
      padding-right: 13rem; /* 208px */
      py-52	padding-top: 13rem; /* 208px */
      padding-bottom: 13rem; /* 208px */
      pt-52	padding-top: 13rem; /* 208px */
      pr-52	padding-right: 13rem; /* 208px */
      pb-52	padding-bottom: 13rem; /* 208px */
      pl-52	padding-left: 13rem; /* 208px */
      p-56	padding: 14rem; /* 224px */
      px-56	padding-left: 14rem; /* 224px */
      padding-right: 14rem; /* 224px */
      py-56	padding-top: 14rem; /* 224px */
      padding-bottom: 14rem; /* 224px */
      pt-56	padding-top: 14rem; /* 224px */
      pr-56	padding-right: 14rem; /* 224px */
      pb-56	padding-bottom: 14rem; /* 224px */
      pl-56	padding-left: 14rem; /* 224px */
      p-60	padding: 15rem; /* 240px */
      px-60	padding-left: 15rem; /* 240px */
      padding-right: 15rem; /* 240px */
      py-60	padding-top: 15rem; /* 240px */
      padding-bottom: 15rem; /* 240px */
      pt-60	padding-top: 15rem; /* 240px */
      pr-60	padding-right: 15rem; /* 240px */
      pb-60	padding-bottom: 15rem; /* 240px */
      pl-60	padding-left: 15rem; /* 240px */
      p-64	padding: 16rem; /* 256px */
      px-64	padding-left: 16rem; /* 256px */
      padding-right: 16rem; /* 256px */
      py-64	padding-top: 16rem; /* 256px */
      padding-bottom: 16rem; /* 256px */
      pt-64	padding-top: 16rem; /* 256px */
      pr-64	padding-right: 16rem; /* 256px */
      pb-64	padding-bottom: 16rem; /* 256px */
      pl-64	padding-left: 16rem; /* 256px */
      p-72	padding: 18rem; /* 288px */
      px-72	padding-left: 18rem; /* 288px */
      padding-right: 18rem; /* 288px */
      py-72	padding-top: 18rem; /* 288px */
      padding-bottom: 18rem; /* 288px */
      pt-72	padding-top: 18rem; /* 288px */
      pr-72	padding-right: 18rem; /* 288px */
      pb-72	padding-bottom: 18rem; /* 288px */
      pl-72	padding-left: 18rem; /* 288px */
      p-80	padding: 20rem; /* 320px */
      px-80	padding-left: 20rem; /* 320px */
      padding-right: 20rem; /* 320px */
      py-80	padding-top: 20rem; /* 320px */
      padding-bottom: 20rem; /* 320px */
      pt-80	padding-top: 20rem; /* 320px */
      pr-80	padding-right: 20rem; /* 320px */
      pb-80	padding-bottom: 20rem; /* 320px */
      pl-80	padding-left: 20rem; /* 320px */
      p-96	padding: 24rem; /* 384px */
      px-96	padding-left: 24rem; /* 384px */
      padding-right: 24rem; /* 384px */
      py-96	padding-top: 24rem; /* 384px */
      padding-bottom: 24rem; /* 384px */
      pt-96	padding-top: 24rem; /* 384px */
      pr-96	padding-right: 24rem; /* 384px */
      pb-96	padding-bottom: 24rem; /* 384px */
      pl-96	padding-left: 24rem; /* 384px */
    -->

<!-- Space Between X/Y
      space-x-0 > * + *	margin-left: 0px;
      space-y-0 > * + *	margin-top: 0px;
      space-x-0.5 > * + *	margin-left: 0.125rem; /* 2px */
      space-y-0.5 > * + *	margin-top: 0.125rem; /* 2px */
      space-x-1 > * + *	margin-left: 0.25rem; /* 4px */
      space-y-1 > * + *	margin-top: 0.25rem; /* 4px */
      space-x-1.5 > * + *	margin-left: 0.375rem; /* 6px */
      space-y-1.5 > * + *	margin-top: 0.375rem; /* 6px */
      space-x-2 > * + *	margin-left: 0.5rem; /* 8px */
      space-y-2 > * + *	margin-top: 0.5rem; /* 8px */
      space-x-2.5 > * + *	margin-left: 0.625rem; /* 10px */
      space-y-2.5 > * + *	margin-top: 0.625rem; /* 10px */
      space-x-3 > * + *	margin-left: 0.75rem; /* 12px */
      space-y-3 > * + *	margin-top: 0.75rem; /* 12px */
      space-x-3.5 > * + *	margin-left: 0.875rem; /* 14px */
      space-y-3.5 > * + *	margin-top: 0.875rem; /* 14px */
      space-x-4 > * + *	margin-left: 1rem; /* 16px */
      space-y-4 > * + *	margin-top: 1rem; /* 16px */
      space-x-5 > * + *	margin-left: 1.25rem; /* 20px */
      space-y-5 > * + *	margin-top: 1.25rem; /* 20px */
      space-x-6 > * + *	margin-left: 1.5rem; /* 24px */
      space-y-6 > * + *	margin-top: 1.5rem; /* 24px */
      space-x-7 > * + *	margin-left: 1.75rem; /* 28px */
      space-y-7 > * + *	margin-top: 1.75rem; /* 28px */
      space-x-8 > * + *	margin-left: 2rem; /* 32px */
      space-y-8 > * + *	margin-top: 2rem; /* 32px */
      space-x-9 > * + *	margin-left: 2.25rem; /* 36px */
      space-y-9 > * + *	margin-top: 2.25rem; /* 36px */
      space-x-10 > * + *	margin-left: 2.5rem; /* 40px */
      space-y-10 > * + *	margin-top: 2.5rem; /* 40px */
      space-x-11 > * + *	margin-left: 2.75rem; /* 44px */
      space-y-11 > * + *	margin-top: 2.75rem; /* 44px */
      space-x-12 > * + *	margin-left: 3rem; /* 48px */
      space-y-12 > * + *	margin-top: 3rem; /* 48px */
      space-x-14 > * + *	margin-left: 3.5rem; /* 56px */
      space-y-14 > * + *	margin-top: 3.5rem; /* 56px */
      space-x-16 > * + *	margin-left: 4rem; /* 64px */
      space-y-16 > * + *	margin-top: 4rem; /* 64px */
      space-x-20 > * + *	margin-left: 5rem; /* 80px */
      space-y-20 > * + *	margin-top: 5rem; /* 80px */
      space-x-24 > * + *	margin-left: 6rem; /* 96px */
      space-y-24 > * + *	margin-top: 6rem; /* 96px */
      space-x-28 > * + *	margin-left: 7rem; /* 112px */
      space-y-28 > * + *	margin-top: 7rem; /* 112px */
      space-x-32 > * + *	margin-left: 8rem; /* 128px */
      space-y-32 > * + *	margin-top: 8rem; /* 128px */
      space-x-36 > * + *	margin-left: 9rem; /* 144px */
      space-y-36 > * + *	margin-top: 9rem; /* 144px */
      space-x-40 > * + *	margin-left: 10rem; /* 160px */
      space-y-40 > * + *	margin-top: 10rem; /* 160px */
      space-x-44 > * + *	margin-left: 11rem; /* 176px */
      space-y-44 > * + *	margin-top: 11rem; /* 176px */
      space-x-48 > * + *	margin-left: 12rem; /* 192px */
      space-y-48 > * + *	margin-top: 12rem; /* 192px */
      space-x-52 > * + *	margin-left: 13rem; /* 208px */
      space-y-52 > * + *	margin-top: 13rem; /* 208px */
      space-x-56 > * + *	margin-left: 14rem; /* 224px */
      space-y-56 > * + *	margin-top: 14rem; /* 224px */
      space-x-60 > * + *	margin-left: 15rem; /* 240px */
      space-y-60 > * + *	margin-top: 15rem; /* 240px */
      space-x-64 > * + *	margin-left: 16rem; /* 256px */
      space-y-64 > * + *	margin-top: 16rem; /* 256px */
      space-x-72 > * + *	margin-left: 18rem; /* 288px */
      space-y-72 > * + *	margin-top: 18rem; /* 288px */
      space-x-80 > * + *	margin-left: 20rem; /* 320px */
      space-y-80 > * + *	margin-top: 20rem; /* 320px */
      space-x-96 > * + *	margin-left: 24rem; /* 384px */
      space-y-96 > * + *	margin-top: 24rem; /* 384px */
      space-x-px > * + *	margin-left: 1px;
      space-y-px > * + *	margin-top: 1px;
      space-y-reverse > * + *	--tw-space-y-reverse: 1;
      space-x-reverse > * + *	--tw-space-x-reverse: 1;
    -->
```

## 10. Typography

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <script src="https://cdn.tailwindcss.com"></script>
    <title>Typography</title>
    <!-- 이런 식으로 폰트를 설정할 수 있음 -->
    <!-- <script>
    tailwind.config = {
      theme: {
        fontFamily:{
          
        }
      }
    }
      </script> -->
  </head>
  <body class="pb-12">
    <!-- Font Family -->
    <div class="font-sans">안녕하세요 Tailwind is awesome</div>
    <div class="font-serif">안녕하세요 Tailwind is awesome</div>
    <div class="font-mono">안녕하세요 Tailwind is awesome</div>
    <!-- Font Size -->
    <div class="text-xs">안녕하세요 Tailwind is awesome</div>
    <div class="text-sm">안녕하세요 Tailwind is awesome</div>
    <div class="text-base">안녕하세요 Tailwind is awesome</div>
    <div class="text-lg">안녕하세요 Tailwind is awesome</div>
    <div class="text-xl">안녕하세요 Tailwind is awesome</div>
    <div class="text-2xl">안녕하세요 Tailwind is awesome</div>
    <div class="text-3xl">안녕하세요 Tailwind is awesome</div>
    <div class="text-9xl">안녕하세요 Tailwind is awesome</div>
    <!-- Font Weight -->
    <div class="font-light">안녕하세요 Tailwind is awesome</div>
    <div class="font-normal">안녕하세요 Tailwind is awesome</div>
    <div class="font-medium">안녕하세요 Tailwind is awesome</div>
    <div class="font-semibold">안녕하세요 Tailwind is awesome</div>
    <div class="font-bold">안녕하세요 Tailwind is awesome</div>
    <!-- Letter Spacing -->
    <div class="tracking-tight">안녕하세요 Tailwind is awesome</div>
    <div class="tracking-normal">안녕하세요 Tailwind is awesome</div>
    <div class="tracking-wide">안녕하세요 Tailwind is awesome</div>
    <!-- Text Alignment -->
    <div class="text-left">안녕하세요 Tailwind is awesome</div>
    <div class="text-center">안녕하세요 Tailwind is awesome</div>
    <div class="text-right">안녕하세요 Tailwind is awesome</div>
    <!-- Text Decoration -->
    <div class="underline decoration-4 decoration-blue-400">
      안녕하세요 Tailwind is awesome
    </div>
    <!-- Decoration Style -->
    <div class="underline decoration-double decoration-4 decoration-blue-400">
      안녕하세요 Tailwind is awesome
    </div>
    <div class="underline decoration-dotted decoration-4 decoration-blue-400">
      안녕하세요 Tailwind is awesome
    </div>
    <div class="underline decoration-dashed decoration-4 decoration-blue-400">
      안녕하세요 Tailwind is awesome
    </div>
    <div
      class="underline decoration-wavy decoration-4 mb-4 decoration-blue-400"
    >
      안녕하세요 Tailwind is awesome
    </div>

    <!-- Decoration Offset -->
    <div
      class="underline decoration-double decoration-4 decoration-blue-400 underline-offset-8"
    >
      안녕하세요 Tailwind is awesome
    </div>

    <!-- Text Transform -->
    <p class="normal-case">안녕하세요 Tailwind is awesome</p>
    <p class="uppercase">안녕하세요 Tailwind is awesome</p>
    <p class="lowercase">안녕하세요 Tailwind is awesome</p>
    <p class="capitalize">안녕하세요 Tailwind is awesome</p>
  </body>
</html>

<!-- Font Family
  font-sans	
  font-family: ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, "Noto Sans", sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji";

  font-serif	
  font-family: ui-serif, Georgia, Cambria, "Times New Roman", Times, serif;
  
  font-mono	
  font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;

-->

<!-- 
  Font Size
  text-xs	    font-size: 0.75rem; /* 12px */
  text-sm	    font-size: 0.875rem; /* 14px */
  text-base	  font-size: 1rem; /* 16px */
  text-lg	    font-size: 1.125rem; /* 18px */
  text-xl	    font-size: 1.25rem; /* 20px */
  text-2xl	  font-size: 1.5rem; /* 24px */
  text-3xl	  font-size: 1.875rem; /* 30px */
  text-4xl	  font-size: 2.25rem; /* 36px */
  text-5xl	  font-size: 3rem; /* 48px */
  text-6xl	  font-size: 3.75rem; /* 60px */
  text-7xl	  font-size: 4.5rem; /* 72px */
  text-8xl	  font-size: 6rem; /* 96px */
  text-9xl	  font-size: 8rem; /* 128px */ 
-->

<!-- Font Weight
  font-thin	      font-weight: 100;
  font-extralight	font-weight: 200;
  font-light	    font-weight: 300;
  font-normal	    font-weight: 400;
  font-medium	    font-weight: 500;
  font-semibold	  font-weight: 600;
  font-bold	      font-weight: 700;
  font-extrabold	font-weight: 800;
  font-black	    font-weight: 900;
-->

<!-- Letter Spacing
  tracking-tighter	letter-spacing: -0.05em;
  tracking-tight	  letter-spacing: -0.025em;
  tracking-normal	  letter-spacing: 0em;
  tracking-wide	    letter-spacing: 0.025em;
  tracking-wider	  letter-spacing: 0.05em;
  tracking-widest	  letter-spacing: 0.1em;
-->

<!-- Text Alignment
  text-left	    text-align: left;
  text-center	  text-align: center;
  text-right	  text-align: right;
  text-justify	text-align: justify;
 -->

<!-- Text Decoration
  decoration-auto	      text-decoration-thickness: auto;
  decoration-from-font	text-decoration-thickness: from-font;
  decoration-0	        text-decoration-thickness: 0px;
  decoration-1	        text-decoration-thickness: 1px;
  decoration-2	        text-decoration-thickness: 2px;
  decoration-4	        text-decoration-thickness: 4px;
  decoration-8	        text-decoration-thickness: 8px;
-->

<!-- Text Transform
  uppercase	  text-transform: uppercase;
  lowercase	  text-transform: lowercase;
  capitalize	text-transform: capitalize;
  normal-case	text-transform: none;
-->
```

## 11. Width & Height

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <script src="https://cdn.tailwindcss.com"></script>
    <title>Sizing</title>
  </head>
  <body>
    <!-- Width -->
    <div class="bg-black text-white w-4">hello</div>
    <div class="bg-black text-white w-48">hello</div>
    <div class="bg-black text-white w-96">hello</div>
    <!-- Percentages -->
    <div class="bg-green-800 text-white w-1/4">hello</div>
    <div class="bg-green-800 text-white w-1/3">hello</div>
    <div class="bg-green-800 text-white w-1/2">hello</div>
    <!-- Width of the viewport -->
    <div class="bg-blue-500 text-white w-screen">hello</div>
    <!-- 100% of container -->
    <div class="bg-blue-300 text-white w-full">hello</div>
    <!-- min/max content -->

    <!-- Arbitrary width -->
    <div class="bg-blue-700 text-white w-[300px]">hello</div>
    <!-- Max Width -->
    <div class="bg-gray-500 max-w-sm mx-auto overflow-hidden">
      <span class="text-xs">
        hellohellohellohellohellohello hellohellohellohellohellohello
        hellohellohellohello
        hellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohello</span
      >
    </div>

    <!-- Height (Most of the same options as widths) -->
    <div class="flex items-end">
      <div class="bg-orange-500 w-20 h-24">Hello</div>
      <div class="bg-orange-500 w-20 h-32">Hello</div>
      <div class="bg-orange-500 w-20 h-40">Hello</div>
      <div class="bg-orange-500 w-20 h-48">Hello</div>
      <div class="bg-orange-500 w-20 h-64">Hello</div>
      <div class="bg-orange-500 w-20 h-96">Hello</div>
    </div>
    <!-- Min Height -->

    <!-- Max Height -->

    <!-- Full screen height -->
    <div class="bg-blue-300 w-20 h-screen">Hello</div>
  </body>
</html>

<!-- 
  Width Sizes
    w-0	    width: 0px;
    w-px	  width: 1px;
    w-0.5	  width: 0.125rem; /* 2px */
    w-1	    width: 0.25rem; /* 4px */
    w-1.5	  width: 0.375rem; /* 6px */
    w-2	    width: 0.5rem; /* 8px */
    w-2.5	  width: 0.625rem; /* 10px */
    w-3	    width: 0.75rem; /* 12px */
    w-3.5	  width: 0.875rem; /* 14px */
    w-4	    width: 1rem; /* 16px */
    w-5   	width: 1.25rem; /* 20px */
    w-6	    width: 1.5rem; /* 24px */
    w-7	    width: 1.75rem; /* 28px */
    w-8	    width: 2rem; /* 32px */
    w-9	    width: 2.25rem; /* 36px */
    w-10	  width: 2.5rem; /* 40px */
    w-11	  width: 2.75rem; /* 44px */
    w-12	  width: 3rem; /* 48px */
    w-14	  width: 3.5rem; /* 56px */
    w-16	  width: 4rem; /* 64px */
    w-20	  width: 5rem; /* 80px */
    w-24	  width: 6rem; /* 96px */
    w-28	  width: 7rem; /* 112px */
    w-32	  width: 8rem; /* 128px */
    w-36	  width: 9rem; /* 144px */
    w-40	  width: 10rem; /* 160px */
    w-44	  width: 11rem; /* 176px */
    w-48	  width: 12rem; /* 192px */
    w-52	  width: 13rem; /* 208px */
    w-56	  width: 14rem; /* 224px */
    w-60	  width: 15rem; /* 240px */
    w-64	  width: 16rem; /* 256px */
    w-72	  width: 18rem; /* 288px */
    w-80	  width: 20rem; /* 320px */
    w-96	  width: 24rem; /* 384px */
    w-auto	width: auto;
    w-1/2	  width: 50%;
    w-1/3	  width: 33.333333%;
    w-2/3	  width: 66.666667%;
    w-1/4	  width: 25%;
    w-2/4	  width: 50%;
    w-3/4	  width: 75%;
    w-1/5	  width: 20%;
    w-2/5	  width: 40%;
    w-3/5	  width: 60%;
    w-4/5	  width: 80%;
    w-1/6	  width: 16.666667%;
    w-2/6	  width: 33.333333%;
    w-3/6	  width: 50%;
    w-4/6	  width: 66.666667%;
    w-5/6	  width: 83.333333%;
    w-1/12	width: 8.333333%;
    w-2/12	width: 16.666667%;
    w-3/12	width: 25%;
    w-4/12	width: 33.333333%;
    w-5/12	width: 41.666667%;
    w-6/12	width: 50%;
    w-7/12	width: 58.333333%;
    w-8/12	width: 66.666667%;
    w-9/12	width: 75%;
    w-10/12	width: 83.333333%;
    w-11/12	width: 91.666667%;
    w-full	width: 100%;
    w-screen  width: 100vw;
    w-min	  width: min-content;
    w-max	  width: max-content;
    w-fit	  width: fit-content; -->

<!-- 
    Min Width Sizes
    min-w-0	      min-width: 0px;
    min-w-full	  min-width: 100%;
    min-w-min	    min-width: min-content;
    min-w-max	    min-width: max-content;
    min-w-fit	    min-width: fit-content;
    -->

<!-- 
    Max Width Sizes
    max-w-0	      max-width: 0rem; /* 0px */
    max-w-none	  max-width: none;
    max-w-xs	    max-width: 20rem; /* 320px */
    max-w-sm	    max-width: 24rem; /* 384px */
    max-w-md	    max-width: 28rem; /* 448px */
    max-w-lg	    max-width: 32rem; /* 512px */
    max-w-xl	    max-width: 36rem; /* 576px */
    max-w-2xl	    max-width: 42rem; /* 672px */
    max-w-3xl	    max-width: 48rem; /* 768px */
    max-w-4xl	    max-width: 56rem; /* 896px */
    max-w-5xl	    max-width: 64rem; /* 1024px */
    max-w-6xl	    max-width: 72rem; /* 1152px */
    max-w-7xl	    max-width: 80rem; /* 1280px */
    max-w-full	  max-width: 100%;
    max-w-min	    max-width: min-content;
    max-w-max	    max-width: max-content;
    max-w-fit	    max-width: fit-content;
    max-w-prose	  max-width: 65ch;
    max-w-screen-sm	max-width: 640px;
    max-w-screen-md	max-width: 768px;
    max-w-screen-lg	max-width: 1024px;
    max-w-screen-xl	max-width: 1280px;
    max-w-screen-2xl	max-width: 1536px;
  -->

<!-- 
    Height Sizes
    h-0	        height: 0px;
    h-px	      height: 1px;
    h-0.5	      height: 0.125rem; /* 2px */
    h-1	        height: 0.25rem; /* 4px */
    h-1.5	      height: 0.375rem; /* 6px */
    h-2	        height: 0.5rem; /* 8px */
    h-2.5	      height: 0.625rem; /* 10px */
    h-3	        height: 0.75rem; /* 12px */
    h-3.5	      height: 0.875rem; /* 14px */
    h-4	        height: 1rem; /* 16px */
    h-5	        height: 1.25rem; /* 20px */
    h-6	        height: 1.5rem; /* 24px */
    h-7	        height: 1.75rem; /* 28px */
    h-8	        height: 2rem; /* 32px */
    h-9	        height: 2.25rem; /* 36px */
    h-10	      height: 2.5rem; /* 40px */
    h-11	      height: 2.75rem; /* 44px */
    h-12	      height: 3rem; /* 48px */
    h-14	      height: 3.5rem; /* 56px */
    h-16	      height: 4rem; /* 64px */
    h-20	      height: 5rem; /* 80px */
    h-24	      height: 6rem; /* 96px */
    h-28	      height: 7rem; /* 112px */
    h-32	      height: 8rem; /* 128px */
    h-36	      height: 9rem; /* 144px */
    h-40	      height: 10rem; /* 160px */
    h-44	      height: 11rem; /* 176px */
    h-48	      height: 12rem; /* 192px */
    h-52	      height: 13rem; /* 208px */
    h-56	      height: 14rem; /* 224px */
    h-60	      height: 15rem; /* 240px */
    h-64	      height: 16rem; /* 256px */
    h-72	      height: 18rem; /* 288px */
    h-80	      height: 20rem; /* 320px */
    h-96	      height: 24rem; /* 384px */
    h-auto	    height: auto;
    h-1/2	      height: 50%;
    h-1/3	      height: 33.333333%;
    h-2/3	      height: 66.666667%;
    h-1/4	      height: 25%;
    h-2/4	      height: 50%;
    h-3/4	      height: 75%;
    h-1/5	      height: 20%;
    h-2/5	      height: 40%;
    h-3/5	      height: 60%;
    h-4/5	      height: 80%;
    h-1/6	      height: 16.666667%;
    h-2/6	      height: 33.333333%;
    h-3/6	      height: 50%;
    h-4/6	      height: 66.666667%;
    h-5/6	      height: 83.333333%;
    h-full	    height: 100%;
    h-screen	  height: 100vh;
    h-min	      height: min-content;
    h-max	      height: max-content;
    h-fit	      height: fit-content;
   -->

<!-- 
  Min Height Sizes
    min-h-0	        min-height: 0px;
    min-h-full	    min-height: 100%;
    min-h-screen	  min-height: 100vh;
    min-h-min	      min-height: min-content;
    min-h-max	      min-height: max-content;
    min-h-fit	      min-height: fit-content;
 -->

<!-- 
   Max Height Sizes
    max-h-0         max-height: 0px;
    max-h-px	      max-height: 1px;
    max-h-0.5	      max-height: 0.125rem; /* 2px */
    max-h-1	        max-height: 0.25rem; /* 4px */
    max-h-1.5	      max-height: 0.375rem; /* 6px */
    max-h-2	        max-height: 0.5rem; /* 8px */
    max-h-2.5	      max-height: 0.625rem; /* 10px */
    max-h-3	        max-height: 0.75rem; /* 12px */
    max-h-3.5	      max-height: 0.875rem; /* 14px */
    max-h-4	        max-height: 1rem; /* 16px */
    max-h-5	        max-height: 1.25rem; /* 20px */
    max-h-6	        max-height: 1.5rem; /* 24px */
    max-h-7	        max-height: 1.75rem; /* 28px */
    max-h-8	        max-height: 2rem; /* 32px */
    max-h-9	        max-height: 2.25rem; /* 36px */
    max-h-10	      max-height: 2.5rem; /* 40px */
    max-h-11	      max-height: 2.75rem; /* 44px */
    max-h-12	      max-height: 3rem; /* 48px */
    max-h-14	      max-height: 3.5rem; /* 56px */
    max-h-16	      max-height: 4rem; /* 64px */
    max-h-20	      max-height: 5rem; /* 80px */
    max-h-24	      max-height: 6rem; /* 96px */
    max-h-28	      max-height: 7rem; /* 112px */
    max-h-32	      max-height: 8rem; /* 128px */
    max-h-36	      max-height: 9rem; /* 144px */
    max-h-40	      max-height: 10rem; /* 160px */
    max-h-44	      max-height: 11rem; /* 176px */
    max-h-48	      max-height: 12rem; /* 192px */
    max-h-52	      max-height: 13rem; /* 208px */
    max-h-56	      max-height: 14rem; /* 224px */
    max-h-60	      max-height: 15rem; /* 240px */
    max-h-64	      max-height: 16rem; /* 256px */
    max-h-72	      max-height: 18rem; /* 288px */
    max-h-80	      max-height: 20rem; /* 320px */
    max-h-96	      max-height: 24rem; /* 384px */
    max-h-full	    max-height: 100%;
    max-h-screen	  max-height: 100vh;
    max-h-min	      max-height: min-content;
    max-h-max	      max-height: max-content;
    max-h-fit	      max-height: fit-content;
  -->
```

## 12.layout&position

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <script src="https://cdn.tailwindcss.com"></script>
    <title>TailwindCSS</title>
  </head>
  <body>
    <!-- Positioning -->
    <div class="relative h-12 w-1/2 bg-red-200">
      <p>Parent Element</p>
      <div class="absolute bottom-0 right-0 bg-red-500">
        <p>Asolute Child</p>
      </div>
    </div>
    <!-- Top left corner -->
    <div class="relative h-32 w-32 bg-yellow-100">
      <div class="absolute left-0 top-0 h-16 w-16 bg-yellow-300"></div>
    </div>
    <!-- Top right corner -->
    <div class="relative h-32 w-32 bg-yellow-100">
      <div class="absolute right-0 top-0 h-16 w-16 bg-yellow-300"></div>
    </div>
    <!-- Bottom left corner -->
    <div class="relative h-32 w-32 bg-yellow-100">
      <div class="absolute left-0 bottom-0 h-16 w-16 bg-yellow-300"></div>
    </div>
    <!-- Bottom right corner -->
    <div class="relative h-32 w-32 bg-yellow-100">
      <div class="absolute left-1/4 bottom-0 h-16 w-16 bg-yellow-300"></div>
    </div>
    <!-- Span top edge -->
    <div class="relative h-32 w-32 bg-yellow-100">
      <div class="absolute inset-x-0 top-0 h-16 bg-yellow-300"></div>
    </div>
    <!-- Span left edge -->
    <div class="relative h-32 w-32 bg-yellow-100">
      <div class="absolute inset-y-0 left-0 w-16 bg-yellow-300"></div>
    </div>
    <!-- Span right edge -->
    <div class="relative h-32 w-32 bg-yellow-100">
      <div class="absolute inset-y-0 right-0 w-16 bg-yellow-300"></div>
    </div>
    <!-- Span bottom edge -->
    <div class="relative h-32 w-32 bg-yellow-100">
      <div class="absolute inset-x-0 bottom-0 h-16 bg-yellow-300"></div>
    </div>
    <!-- Display Classes -->
    <div>
      Lorem ipsum, <span class="inline font-bold">this is inline</span> dolor
      sit amet consectetur adipisicing elit. Labore error a qui
      perspiciatis,<span class="inline-block font-bold">
        this is inline block</span
      >
      ipsum velit? Repellendus accusamus, veniam facere animi ullam inventore
      <span class="block font-bold">this is block</span> voluptatibus voluptatum
      aliquid qui? Optio, illum vitae? Excepturi aspernatur aliquid vitae
      tempora ipsum ullam
      <span class="hidden font-bold">this is hidden</span> corporis culpa
      numquam aliquam deserunt ut perspiciatis ducimus odio odit soluta qui nisi
      accusantium eos quod sint, quam modi harum! Alias rerum sint amet?
    </div>
    <!-- Z-Index -->
    <div class="relative h-36">
      <div class="absolute left-10 w-24 h-24 bg-blue-300 z-40">1</div>
      <div class="absolute left-20 w-24 h-24 bg-blue-400">2</div>
      <div class="absolute left-40 w-24 h-24 bg-blue-500 z-30">3</div>
      <div class="absolute left-60 w-24 h-24 bg-blue-600">4</div>
      <div class="absolute left-80 w-24 h-24 bg-blue-700">5</div>
    </div>
    <!-- Floats -->
    <div class="w-1/2">
      <img
        class="h-48 w-48 float-right m-4"
        src="../assets/img/img1.jpg"
        alt=""
      />
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati
        molestias, dolore veniam id fuga similique adipisci iste iusto
        reprehenderit mollitia quos harum, sequi ullam repudiandae debitis eaque
        doloremque! Velit a qui error. Ipsam quaerat expedita quidem esse omnis
        iusto natus!
      </p>
    </div>
  </body>
</html>

<!-- Position Classes
      static	    position: static;
      fixed	      position: fixed;
      absolute	  position: absolute;
      relative	  position: relative;
      sticky	    position: sticky;
    -->

<!-- Display Classes
      block	            display: block;
      inline-block	    display: inline-block;
      inline	          display: inline;
      flex	            display: flex;
      inline-flex	      display: inline-flex;
      table	            display: table;
      grid	            display: grid;
      inline-grid	      display: inline-grid;
      contents	        display: contents;
      list-item	        display: list-item;
      hidden	          display: none;
    -->

<!-- Z-Index
      z-0	    z-index: 0;
      z-10	  z-index: 10;
      z-20	  z-index: 20;
      z-30	  z-index: 30;
      z-40	  z-index: 40;
      z-50	  z-index: 50;
      z-auto	z-index: auto;
    -->

<!-- Float
      float-right	  float: right;
      float-left	  float: left;
      float-none	  float: none;
    -->
```
