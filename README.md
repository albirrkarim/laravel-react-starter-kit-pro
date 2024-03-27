# Laravel React Starter Kit PRO

![Laravel React Starter Kit PRO Banner](/img/banner.webp)

Premium toolkit designed for full-stack web development, offering a streamlined approach to integrating Laravel with React. It includes updated dependencies, best practices, and security implementations, making it suitable for developers at any level looking for a reliable project foundation.

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

![Project Foundation](/img/foundation.png)

I will make solid laravel react starter kit with includes many amazing component.

## B. Development Aspect

### Philosophy

Make it simple, easy to learn and teach to your teams, real production case.

### Integration

Provide best practice to make the data APIs. 

- Routing name
- Well route grouping
- Handling Form Request (CRUD) from the frontend
- Traits
- Ready make email verification, forgot password. you just setting the SMTP (tutorial is included in the readme on private repo)
- We need more AI ... in this package has example of using open ai api and the elevenlabs (text-to-speech services) the laravel is act as forwarder to keeps the secret key is secure.


### Security

Provide some example for authentications and securing laravel.

- Using JWT (Json Web Token)
- Throthling (rate limiter)
- Fingerprint login
- Pin login

### Maintenance

I keep this package designed to be simple, less dependencies, designed for making common website. Always updated with current version. This starter kit is keeps to its latest version when at the end of the month. (monthly update)

**Front end main dependencies:**

- [React js](https://react.dev/)

  React offer reuseable component and good interactifity compares to other old js library like [jquery](https://jquery.com/). react has drawback when the programmer is new in react, they don't know about the react rerender and it can resulting a slow app, lag, or maybe memory leak. Again the experience is needed when deal with react.

- [Material UI](https://mui.com)

  Material ui is widely used, good foundation for frontend, offer very good best practice.

- [Tailwind CSS](https://tailwindcss.com)

  Tailwind offer good ui when you still thing the material ui is not your style.

- [Editor js](https://editorjs.io/)

  Sometimes we need to implement editor that can, do like CMS in wordpress. That can edit long article with good user experience. How can we achieve this in react and laravel? Many options is available like [CKeditor](https://ckeditor.com/) and other. i do research the [Editor js](https://editorjs.io/) is better user experience when we try to make long article content.

- [Apexcharts](https://apexcharts.com)

  Apexcharts is a good choice for displaying your charts.

- [Next js](https://nextjs.org) 

  The our basic stack is laravel and react (client-side rendering). Recently i have project that must do hard competition in SEO. The Server Side Rendering (SSR) is must be used.

  So i combine the next js(offer SSR capability), react js, laravel. also this is exist draw back. your hosting must support for node js hosting, make sure you check the hosting specification.

  We have starter kit with next js version


**Backend main dependencies:**

- [php-open-source-saver/jwt-auth](https://github.com/PHP-Open-Source-Saver/jwt-auth)

- [php-open-source-saver/jwt-auth](https://github.com/PHP-Open-Source-Saver/jwt-auth)


### Testing

The purpose of testing is to make sure all function work correctly time after time and feature after feature implemented.

![Automatic & Easy Way to Testing Laravel](/img/testing.png)

**Common Problem:**

The case is when you try to implement next feature (`X`) sometimes the existing feature (`Y`) is broken.

What you will do ? fix the `Y` feature, then checking manually all other features? Stop, don't manually check the functionality time overtime.

Making automatic testing for laravel is high labour cost. Making test code for backend is difficult when it comes with many posibilities of data modification, how you can make test case for that? its so hard.

In this package i decide to make testing based on the API output, Since, the frontend (react) and backend (laravel) is connected by API.

**Then how you can making test case?**

1. First make sure (now) all the feature is correct

2. Then, They can just doing many interactions click button, fill forms, etc, on app ui. and the test case is generated automatically.

    <details>
      <summary>Show generated test case</summary>

      <br/>

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
    </details>

<br/>

3. Then when we want to do testing using [jest library](https://jestjs.io/), My code will doing send request based on the test case. Just run the `npm run test` 

    ```js
    const res = // sent to server with information testcase.send

    expect(res).tobe(testcase.send.received);
    ```

    With that method and sequentially doing actions, so the test case will don't care about the data changes, in the database. but just give attention into the final output of the APIs.

4. The finall output of the APIs (response) with correct data and sequentially executed is representing your function inside laravel is working properly. Now the all features have been checked automatically and 100% working so the app ready to be deliver into production.

<br>
<br>

## C. Todo

- [ ] Make demo
- [ ] Make video tutorial

<br>
<br>

## D. Code

In the demo website you will see only the frontend and api mocking (just to simulate api call).

Once you buy you will get inside my [private repo Laravel React Starter Kit PRO](https://github.com/Web-XR-AI-lab/laravel-react-starter-kit-pro)

<br>
<br>

## E. Changelog

Changelog contains information about new amazing feature, fix bug, breaking changes information, and what you should do when the version is update.

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

We need funding to make this starter kit always maintained. No worry, i make the price is cheap $5 USD monthly. its just price of a coffee.

**This package will update the dependencies every?**

Monthly

**Just ask me what question you will ask**

Send me message via:

Discord: [albirrkarim](https://discord.com/channels/@me/884043164908929034)

<!-- <details>
  <summary></summary>

  <br/>

Yes it is, i

</details> -->

<br/>
