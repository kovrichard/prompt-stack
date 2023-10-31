# prompt-stack

Full-Stack application from Prompts 📄➡️🌐


## Introduction

`PromptStack` is a full-stack application without the code that implements it. Each file is in the place where it needs to be, but instead of code,
they contain prompts for various AI tools that you need to use to generate the implementation. The config files are already filled with the
required settings, so you can focus on the part that truly matters: the implementation.

Since almost no code is written in `PromptStack`, every user will get a slightly different implementation because of the probabilistic nature of
AI tools.

The following AI tools are used in the repository:
- [ChatGPT](https://chat.openai.com/) with a Plus subscription
- [GitHub Copilot](https://github.com/features/copilot)
- [Midjourney](https://www.midjourney.com/home)

> [!NOTE]
> Feel free to try other language models, coding assistants, and image generators when using the repository. However, we tested every prompt with only
> the three tools above, so we cannot guarantee the same success rate when someone uses alternatives.

## Motivation

`PromptStack` was created to show that anyone can build a full-stack web application with the right AI tools. While reading the prompts for the
different files, you will explore well-known prompting techniques that make any developer's life easier. As you progress through the files, you
will get a good understanding of how modern full-stack developers can use AI in their daily work.

## How to use the repo?

The repository contains a backend and a frontend. No config file must be changed. You only have to generate code, text, or images. Each file has a
correspondent `.prompt` file next to it. For example, to generate the implementation of `app.ts`, you have to look for the steps in `app.ts.prompt`.
The `.prompt` file will contain a prompt (or multiple prompts) and an explanation about what to do with it. It will explain what tool you should put
the prompt into, and what to do with the result you received.

Here is an example `.prompt` file for `app.ts`:

```
Tool to use: GitHub Copilot
Task: Copy the content of Prompt into app.ts, then press Enter twice. When you receive a completion,
      press Tab to accept it. If you don't receive completions anymore, then this task is finished.
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

> [!IMPORTANT]
> Here's a pro tip: To get the most out of this repository, don't just blindly follow the instructions and copy-paste everything into the files. Read
> the prompts first thoroughly, think about why they will work, try to guess what the tools will generate, and finally, let them generate the thing.

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

Backend:

``` bash
cd server
pnpm i
```

Frontend:

``` bash
cd client
pnpm i
```

> [!NOTE]
> By default, the application uses `pnpm`. You can use other package managers, but then you also have to care about the correspondent lock files.

### Implement the code

Follow the instructions in the `.prompt` files and generate their implementation. Once you feel you are ready, go to the next step.

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
```

### Tests

`PromptStack` contains test files, but they are also empty. Tests also have their `.prompt` files next to them, so if you are interested, you can
generate test cases and run them with the following commands.

Backend:

``` bash
cd server
pnpm test
```

Frontend

``` bash
cd client
pnpm test
```
