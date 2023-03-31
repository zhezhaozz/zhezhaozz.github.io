---
layout: page
title: GitHub Tutorial
description: Collaborative development using Git and GitHub
img: /assets/img/github-mark.png
importance: 3
category: Tutorial
---

This is a tutorial about collaborative development using Git and GitHub I made for my lab and the Academia Cafe community.

**Zoom Link:** TBD

**Time:** TBD

**Contact Info:** [zzhaozhe@umich.edu](mailto:john@example.com)

### Disclaimer
1. In this tutorial I will demonstrate codes in MacOS. Windows machine uses a different command-line interface, which I'm not familiar with. For windows users, I strongly recommend learning how to use the comman prompt before taking this tutorial.
2. This tutorial is only a simple demo of the current practice I'm using for projects. Not everything listed here is considered the best practice.

### Prerequisites
I will assume that you have installed `Git` on your operation systems. If not, please refer to this [link](https://www.atlassian.com/git/tutorials/install-git) for installation instruction. After the installation, go to [https://github.com/](https://github.com/) and register an account.

Once you acquired a GitHub account, you need to configure your account credential on your MacOS machine. Open the terminal application and type the following command. Remember to replace `your-github-user-name` and `your-account-email`.

{% raw %}
```zsh
$ git config --global user.name "your-github-user-name"
$ git config --global user.email your-account-email
```
{% endraw %}

Once you have done the above steps, type

{% raw %}
```zsh
$ git config --list
```
{% endraw %}

to make sure that your information has been correctly set up.

### Tutorial Material

This tutorial will follow along the instruction on this [repository](https://github.com/zhezhaozz/git_tutorial). This repository was inspired and modified from the git tutorial created by [romankouz](https://github.com/romankouz/git_tutorial).