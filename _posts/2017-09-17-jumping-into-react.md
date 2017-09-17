---
layout: post
title: "Jumping Into React.js"
author: "Steven"
---

This past week I started a web developer internship and it’s been great so far. What I have already noticed from the first week is the need to be constantly researching and continuing learning new technologies.

Before starting this internship I had an interest in wanting to learn React.js, so when my mentor asked which JavaScript framework we should use for a new task, I jumped at the opportunity to learn/use React.

Having some previous knowledge of Angular I felt fairly confident in learning it, however there are some differences and realized I should do a quick tutorial. So below in this post, I will be typing out notes while doing the tutorial on the [React.js](https://facebook.github.io/react/tutorial/tutorial.html) website.

### Getting Started

This has to be the easiest part of using React, all you need to do is follow a couple simple steps to get it running on your machine.

Install [Node.js](https://nodejs.org/en/) if you don’t have it yet. Then to install and get React running enter this code into your terminal.

<br>
{% highlight js %}
npm install -g create-react-app
create-react-app my-app

cd my-app
npm start
{% endhighlight %}
<br>

### Notes on React

_React is a declarative, efficient, and flexible JavaScript library for building user interfaces._

React is made up of many parts, one of the main parts are the components. _Components tell React what you want to render -then React will efficiently update and render just the right components when your data changes._

A component takes in parameters, called `props`, and returns a hierarchy of views to display via the `render` method.

The `render` method returns a description of what you want to render, and then React takes that description and renders it to the screen. Most developers use a special syntax called JSX which makes it easier to write these structures. The `<div />` syntax is transformed at build time to `React.createElement(‘div’)`.

You can put any JavaScript expression within braces inside JSX. Each React element is a real JavaScript object that you can store in a variable or pass around your program.

When a component no longer keeps its own state; it receives its value from its parent component and informs its parent when it’s clicked. Components like this are called _Controlled Components_.

_There are generally two ways for changing data. The first method is to mutate the data by directly changing the values of a variable. The second method is to replace the data with a new copy of the object that also includes desired changes._
<br>
<br>

_For example:_

**Data change with mutation**<br>
{% highlight js%}
var player = {score: 1, name: 'Jeff'};
player.score = 2;
// Now player is {score: 2, name: 'Jeff'}
{% endhighlight %}

**Data Change without mutation**<br>
{% highlight js%}
var player = {score: 1, name: 'Jeff'};

var newPlayer = Object.assign({}, player, {score: 2});
// Now player is unchanged, but newPlayer is {score: 2, name: 'Jeff'}

// Or if you are using object spread syntax proposal, you can write:
// var newPlayer = {...player, score: 2};
{% endhighlight %}
<br>
<br>

The end result is the same but by not mutating (or changing the underlying data) directly we now have an added benefit that can help us increase component and overall application performance.

React supports a simpler syntax called _functional components_. These are components that only consist of a `render` method. Rather than defining a class extending  `React.Component`, simply write a function that takes props and returns what should be rendered.

_For Example:_
{% highlight js %}
function Square(props) {
  return (
    <button className="square" onClick={props.onClick}>
      {props.value}
    </button>
  );
}
{% endhighlight %}
<br>

<hr>
<br>

As I said the purpose of this post was to just show some of the notes I took through out this tutorial. After finishing it I definitely feel like I’ve learned some of the basics of React. But there is still so much more to continue learning and I look forward to all the capabilities this JavaScript library has.

I hope you enjoyed and maybe learned something from this post. Feel free to share and definitely go check out the React docs and the tutorial to learn more.

You can view my repo for the tutorial [Reat.js Tutorial Repo](https://github.com/stevenmillsii/react-tutorial).
