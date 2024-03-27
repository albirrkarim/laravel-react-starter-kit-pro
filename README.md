# Laravel React Starter Kit PRO

![Laravel React Starter Kit PRO Banner](/img/banner.webp)

## Docs for v1.0.0

**Table Of Contents**

- [A. Introduction](#a-introduction)
- [B. Development Aspect](#b-development-aspect)
- [C. Todo](#c-todo)
- [D. Example Code](#d-code)
- [E. Changelog](#e-changelog)
- [F. Disclaimer & Warranty](#f-disclaimer--warranty)
- [G. FAQ](#g-faq)

## A. Introduction

### Problem

Long time ago, i was new in field of full stack developer. My tech stack is [laravel](https://laravel.com) and [react js](https://react.dev), i know little bit of laravel and react. I don't know the best practice, and functions that react and laravel already have to do some logic. The steps i use to learn something: learn few -> just do it -> improve (best practice etc)

**How about reading the documentation?**

The laravel and react, have a lot of features and helper functions. and ofcourse they make a lot documentations. The problem is we have to read **a lot** of the documentation so we understand the best practice.

### Solutions

#### Many ways you can do

1. The first solution is use chat gpt, copy the code you have made and ask chat gpt to modify it into best practice. this method you will be open and close chat gpt offer time. (it wasting time)

2. Using Template and Boilerplate. I also use paid template. (ensuring they maintain the dependencies update). How about boilerplate? many boilerplate is just opensource repo. that is not well maintenance. outdated dependencies, outdated integration method. etc ...

#### Finally

![Overview](/img/overview.png)

So i made this starter kit to ensure the the dependencies is maintained, integration is seamless, also the security, everthing just work, documented, and have system overview.

Maybe you are project manager that also want this thing, so you can easily explain to your team about your project and the tech stack do you use using our overview.

#### Conclusion

I will make solid laravel react starter kit with includes many amazing component.

## B. Development Aspect

### Philosophy

Make it simple, easy to learn and teach to your teams, real production case.

### Integration

What you will do if you want to implement some integration into other platform?

find the documentation.

### Security

- Provide some example for to securing laravel,
- Using JWT(Json Web Token)

### Maintenance

I keep this package designed to be simple, less dependencies, designed for making common website.

### Testing

The purpose of testing is to make sure all function work correctly time after time and feature after feature implemented.

![Automatic & Easy Way to Testing Laravel](/img/testing.png)

**Common Problem:**

The case is when you try to implement next feature (`X`) sometimes the existing feature (`Y`) is broken.

What you will do ? fix the `Y` feature, then checking manually all other features? Stop, don't manually check the functionality time overtime.

Making automatic testing for laravel is high labour cost. Making test code for backend is difficult when it comes with many posibilities of data modification, how you can make test case for that? its so hard.

The test case is something like this.

```
some value -> function -> expect to be
```

In this package i decide to make testing based on the API output, Since, the frontend (react) and backend (laravel) is connected by API.

**Then how you can making test case?**

First make sure now is the function is correct.

Then, They can just doing many interactions click button, fill forms, etc, on app ui. and the test case is generated automatically.

```js
[
  {// Action 1
    send: {
      url:"/api/v1/some_service?q=data that some button send to laravel api service",
      method:"GET",
    }
    received: "data that frontend received from laravel api service"
  },
  {// Action 2
    send: {
      url:"/api/v1/form",
      method:"POST",
      data:"data that some form send to laravel api service"
    }
    received:"data that frontend received from laravel api service"
  },
  // Other user interactions.
]
```

Then when we want to do testing using [jest library](https://jestjs.io/), my code will doing send request based on the test case

```js

const res = sent to server with information testcase.send

expect(res).tobe(testcase.send.received);
```

With that method and sequentially doing actions, so the test case will don't care about the data changes, in the database. but just give attention into the final output of the APIs.

The finall output of the APIs with correct sequentially actions is represent your function inside laravel is working properly.

<br>
<br>

## C. Todo

- [ ] Make demo.

<br>
<br>

## D. Code

In the demo website you will see only the frontend and api mocking (just to simulate api call).

Once you buy you will get inside my [private repo Laravel React Starter Kit PRO](https://github.com/Web-XR-AI-lab/laravel-react-starter-kit-pro)

<br>
<br>

## E. Changelog

Changelog contains information about new feature, improve accuracy, fix bug, and what you should do when the version is update.

See [CHANGELOG.md](CHANGELOG.md)

<br>
<br>

## F. Disclaimer & Warranty

There's no refund, just cancel your subscription in github sponsors menu.

I love feedback from my customers. You can write on the issue tab so when i have time i can try to solve that and deliver for the next update.

<br>
<br>

## G. FAQ

**Why it's expensive? Why it's not opensource package?**

We need funding to make this starter kit always maintained. No worry, i make the price is cheap $3 USD monthly. its just price of a coffee.

**This package will update the dependencies every?**

Monthly

**Just ask me what question you will ask**

<!-- <details>
  <summary></summary>

  <br/>

Yes it is, i

</details> -->

<br/>
