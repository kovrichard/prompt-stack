# prompt-stack

Full-Stack application from Prompts 📄➡️🌐


## Introduction

`PromptStack` is a full-stack application, without the code that implements it. Each file is in the place where it needs to be, but instead of code,
they contain prompts for various AI tools that you need to use to generate the implementation. The config files are already filled with the
required settings so you can focus on the part that truly matters: the implementation.

Since almost no code is written in PromptStack, every user will get a slightly different implementation because of the probabilistic nature of
AI tools.

## Motivation

`PromptStack` was created to show that anyone can build a full-stack web application with the right AI tools. During reading the prompts for the
different files, you will explore various well-known prompting techniques that make any developer's life easier.

## How to use the repo?

The repository contains a backend and a frontend. No config file must be changed, you only have to generate code, text, or images. Each file has a
correspondent `.prompt` file next to it. For example, to generate the implementation of `app.ts`, you have to look for the steps in `app.ts.prompt`.
The `.prompt` file will contain a prompt (or multiple prompts) and an explanation about what to do with the it. It will explain what tool you should
put the prompt into, and what to do with the result you received.

Here is an example `.prompt` file for `app.ts`:

```
Tool to use: GitHub Copilot
Task: Copy the content of Prompt into app.ts, then press Enter twice. When you receive a completion,
      press Tab to accept it. If you don't receive completions anymore, the this task is finished.
      Copy everything between the two --- marks.
Prompt:
---
// typescript
// basic express app with two routes
// the / returns 'Hello World!' in json 'message' property
// the /healthcheck returns 'OK' in json 'status' property
// types are used where possible
// app is default exported but not listening
---
```

## Quick Start

### Clone the repository

``` bash
git clone git@github.com:kovrichard/prompt-stack.git
```

or

``` bash
git clone https://github.com/kovrichard/prompt-stack.git
```

### Install dependencies

``` bash
pnpm i
```

or

``` bash
npm i
```

or

``` bash
yarn install
```

### Implement the code

Follow to instructions in the `.prompt` files and generate their implementation. Once you feel you are ready, go to the next step.

### Start the app

Backend:

``` bash
cd server
pnpm run dev
```

Frontend

``` bash
cd client
pnpm run dev
