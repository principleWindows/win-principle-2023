# 第1讲 Windows 操作系统概述

- https://news.microsoft.com/source/features/ai/microsoft-outlines-framework-for-building-ai-apps-and-copilots-expands-ai-plugin-ecosystem/
- https://powerbi.microsoft.com/en-us/what-is-business-intelligence/
- https://redmondmag.com/articles/2023/05/23/meet-fabric-the-ai-fication-of-microsoft-data--business.aspx
- https://visualstudiomagazine.com/articles/2023/05/23/build-2023-ai.aspx
- https://blogs.microsoft.com/blog/2023/05/23/microsoft-build-brings-ai-tools-to-the-forefront-for-developers/
- https://www.windowscentral.com/microsoft/here-are-the-biggest-announcements-coming-out-of-microsoft-build-2023
- https://www.windowscentral.com/microsoft/top-5-announcements-from-microsoft-build-2023-that-you-need-to-know
- https://blogs.windows.com/windowsdeveloper/2023/05/23/bringing-the-power-of-ai-to-windows-11-unlocking-a-new-era-of-productivity-for-customers-and-developers-with-windows-copilot-and-dev-home/

---

## <span id="index">目录</span>

- [1.1 Introduction](#introduction) \
- [1.2 Windows Programming](#windows-programming) \
	- [1.2.1 工具及开发流程]()
	- [1.2.2 编程语言]()
	- [1.2.3 应用程序类型]()
	- [1.2.4 函数指针与委托]()
	- [1.2.5 Codebase and git]()
- [1.3 MVVM and WPF](#mvvm-and-wpf) \
- [1.4 UWP, WinUI and App SDK](#uwp-winui-and-app-sdk) \
- [1.5 WebView2 and PWA](#webview2-and-pwa) \


OS ==> an AI personal assistant

The Copilot will be available in a taskbar for users. Once open, the Copilot will "stay consistent across your apps, programs and windows," said Chief Product Officer Panos Panay. It will be available for users in apps such as Word and Teams.

Every developer should be an AI developer ==>  On Windows platform, assisted by Windows CoPilot

![](pix_1/Copilot-stack-2.webp)
Microsoft outlined an AI development framework to help developers build their own copilot. Graphic courtesy of Microsoft.


## 1.2 Windows Programming


### Programming model

- [The Programming Model](https://learn.microsoft.com/en-us/windows/win32/rpc/the-programming-model)
- <https://www.igi-global.com/dictionary/towards-programming-model-ubiquitous-computing/34866>
- [Differences between programming model and programming paradigm?](https://cs.stackexchange.com/questions/49421/differences-between-programming-model-and-programming-paradigm)
- [What is a programming model?](https://softwareengineering.stackexchange.com/questions/365755/what-is-a-programming-model)
- [Coyote programming models](https://www.microsoft.com/en-us/research/blog/coyote-making-it-easier-for-developers-to-build-reliable-asynchronous-software/)

---

The programming model is what the instructions (the language) require to work correctly. Implementation 
of those instructions are the details that can change without changing the result of following those 
instructions.

For example, if my instructions are that you should relocate 3 feet north and 2 feet west you can implement 
those instructions by moving west first then north, north first then west, or by moving diagonally 
in a northwest direction. You can even stager about randomly until you happen be at the right spot 
and then stop. Any of those follow the instructions. The programming model here is the idea of relocating 
at a different spot. Is it not how you relocate at a different spot. "How" is implementation detail.

A programming language or an instruction set both abstract away implementation details that they do 
not care about. This leaves those who design compilers, interpreters, JVMs, and CPUs with room to make 
choices of how to implement while supporting this model. Those choices can make things more robust, 
efficient, maintainable, and extensible. Or they can fail to do so. But so long as they do what the 
instructions asked for they still maintain the programming model.

So long as the implementation supports the programming model you can trust that when it follows the 
instructions it will give you what it was supposed to give you.

Also understand that these can layer. You could have a movement model that exposes the idea of moving 
only north & south and east & west leaving no way to move diagonally. That detail won't be in the location 
model above but it will be down here in the movement model. What isn't in the movement model is if 
you walk, ride a bike, or swim to do these movements.

Whenever we model we chose things to care about at this level. Other things we abstract away and let 
something else deal with them.


#### What is the Programming Models in Cloud Computing?

- <https://elysiumacademy.org/cloud-computing-programming-characteristics/>

Usually, there are some certain strategies to recognize where cloud services will use and how it achieves for business goals. Particularly, to reach your goals in business are possible through infrastructure as a service and Platform as a Service, private and public cloud, testing and development, big data analytics course, file storage, disaster recovery, and backup of the cloud. Through the essential servers and computer programming of the cloud, it is efficient to access all the facilities offered by this computing technology. Additionally, cloud course development empowers the user to acquire their application for quick marketing. To mention that, there is no data loss due to hardware failures because of backups in the network. Also, it uses the organization’s saving, and remote servers.


