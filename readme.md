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
