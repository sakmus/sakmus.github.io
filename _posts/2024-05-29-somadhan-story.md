---
title: The Story Behind Somadhan
date: 2024-05-29 12:30:00 +0600
categories: [Programming, Backend, Python]
tags: [python, programming, backend, wolframalpha]
description: Reason behind building this web-app and the odds I faced from the beginning
image: 
    path: https://images2.imgbox.com/0c/36/CJvmTZEx_o.png
    alt: A screenshot of Somadhan web interface
---

## Introduction

As you may know, my Python Flask project [Somadhan](https://github.com/sakmus/somadhan/){:target="_blank"} uses the [Wolfram Alpha](https://wolframalhpa.com/){:target="_blank"} API to communicate with the server and solve complex problems within just a few seconds. But why? Why would someone use this third-party client to solve maths when you can always do it from the official site within your browser? Maybe more questions are wandering around this project, so I’ll try to answer them.

## Backstory

To put it simply, I was kind of frustrated about maths. I love solving math problems. But sometimes, you calculate for 3-4 pages and don’t know whether you messed up. On top of that, some academic books may have the answer for you to check, yet many don’t. Also, sometimes the answers in the books are wrong. To solve these numerous issues, I stumbled upon building an app that can answer almost any mathematical problem.

## Initial Program

After coming up with the idea, I had to find a way to build it and make it work. I used Wolfram Alpha API in the past for console-based simple assistants. I was a script kiddie back then and I can't call myself a programmer yet for my lack of knowledge. My target was to build this app as CLI since command-line applications are easier to build than graphical ones and can utilize more resources performing actual tasks rather than showing them. According to the plan, I built the command line app successfully. It was able to give text results within one or two seconds. The next task was a tough one, the task of building the GUI.

## Building the GUI

I have never built GUI applications before, so the process took more time, energy and complex turns than usual. As my target was mainly desktop devices, I started with [Tkinter](https://docs.python.org/3/library/tkinter.html){:target="_blank"} and [Custom Tkinter](https://pypi.org/project/customtkinter/){:target="_blank"}. The ‘Custom Tkinter’ package built on top of Tkinter helped me build the GUI with modern window and button designs. And the best part was that it had the same efficiency as the common-line version.

But to increase the scope of this app, I decided to convert it into a web application. For this type of small app, backend frameworks like [Django](https://pypi.org/project/Django/){:target="blank"} were overkill. To simply migrate to the web interface, I chose [Flask](https://pypi.org/project/Flask/){:target="blank"}. It took a very short amount of time to fully migrate. And now it’s standing in front of you in that version where it’s compatible with mobile phones.

## Problems Faced in Each Step

The development may seem simple and smooth to many of you, but it was a roller coaster ride for me. First, while building the command line version, the first problem was the font. Even after solving the issue by changing the default font of my terminal, it still seemed quite a hassle, and it was one question at a time. To cope with this single-user issue, I used the built-in [Socket](https://docs.python.org/3/library/socket.html){:target="_blank"} module to connect it with a local network and used another built-in module called [Threading](https://docs.python.org/3/library/threading.html){:target="_blank"}. Now, the program can handle multiple clients on multiple devices at once.

Reading mathematical expressions from the terminal in the monospace font is quite eye-straining. Thus, I upgraded it to the GUI version using ‘Tkinter’ and ‘Custom Tkinter’ modules. The code was blazing fast, but it came with some drawbacks. The program wasn't on the local network and was limited to a single client. It seemed to me more like a downgrade to the command line version. However, sacrificing a few more seconds, the web version solved all other problems. The server could run on the local network and was used by multiple clients simultaneously. Afterwards, I not only had one-line answers but also could show some basic plots. The plots too were sourced from Wolfram Alpha.

## Conclusion

The development journey and the project were fun. However, it is not scalable at the business or at the enterprise level to monetize it. Firstly, any user could visit [Wolfram Alpha](https://wolframalpha.com/){:target="_blank"} and get the same or even better results without any cost because it offers more flexibility in terms of mathematical input. Lastly and most importantly, this program has the potential for data theft. You may never know that these applications may steal and sell your data. I built this one out of frustration and to learn and explore new technologies and domains of this empire. However, the program is available as a [GitHub repository](https://github.com/sakmus/somadhan/). You may want to look at the code and criticize it. As the program is not profitable, I don’t expect anybody to contribute to the code. If you do contribute out of generosity, I’d appreciate that. The program has been published under the [GPL-3](https://www.gnu.org/licenses/gpl-3.0.en.html#license-text){:target="_blank"} License,  so do give credits if you share. It would motivate me. Happy coding!