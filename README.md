# Vue 3 Composition API examples

## Project setup

```

yarn install

```

## Docker setup

Build the container

```
docker-compose build
```

Run the container (Add -d flag to launch without the logs)

```
docker-compose up
```

Stop the container

```
docker-compose down
```

## Project explanation

Vue 3's function-based API was proposed in an RFC in May 2019, and it was divisive. I wanted to better understand the benefits and so I created this repository for the purposes of better appreciating some of the changes that will be coming down the line.

## The project

The project is divided into a series of little apps that demonstrate how to achieve some of the basic Vue 2.x outcomes with Vue 3.0's API.

The Todo list was forked from a handy Codepen made by [@sharon-the-encoder](https://codepen.io/sharon-the-encoder) (@CodeFa on Github) - which sped up my intial work!

# What I've learned:

## Grouping your data together makes sense:

We all love Vue's very clean, consistent `data`, `methods`, `computed` structure. But it doesn't always make sense. Forcing types of actions or data together means that your method which mutates a data property might be at the top and bottom of the file. Vue 3 means we can group relevant actions and data them together.

## Hooks are smarter mixins

Mixins are helpful, no doubt - but they're dumb helpers. Hooks allow us to use smarter imports with explicit logic origin. If you have a file with several mixins, the origin of the data/methods/computed etc that are you now have access to is not immediately obvious. Hooks have us import what we need to use from them, and so we can clearly track our data's origin.

Hooks can also communicate with each other, something that mixins couldn't do.

<br /><br />

[![Netlify Status](https://api.netlify.com/api/v1/badges/62004b38-9301-419d-b28f-c5bbc5bd26d0/deploy-status)](https://app.netlify.com/sites/todoapps-vue3/deploys)

[Demo](https://todoapps-vue3.netlify.app/todo)