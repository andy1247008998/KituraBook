# 欢迎来到Kitura！

## 什么是Kitura?

[Kitura](http://www.kitura.io) 是一个用[Swift编程语言](https://swift.org)编写的轻量级Web开发框架. 它是由IBM公司在2016年初开发，然后作为开源软件以[Apache 2.0 许可证](https://tldrlegal.com/license/apache-license-2.0-%28apache-2.0%29#summary) (Swift语言也采用此许可证)发布的。

尽管Kitura已经得到“深蓝”公司的持续重视和推动，Kitura至今还没有在全球范围内火起来。也许世界上已经不需要另一个Web框架了。即使你已经决定使用Swift来开发你的服务器端应用，Kitura仍然有其他竞争对手如Vapor和Perfect。此外，虽然Kitura的文档看起来到处都有，文档质量和覆盖面却参差不齐。

## 为什么用Kitura?

* 因为Swift是一个极好的编程语言。苹果在2014年发布它来取代古老的Objective-C。Swift具备现代、友好、流畅、有趣的特点。
* 因为Kitura背后的IBM公司，大概是除了苹果之外，最积极采用和推进Swift的企业。IBM自己的[云平台](https://www.ibm.com/cloud/)专门为Swift应用提供支持，并且在它自家的企业级Linux和Unix操作系统如PowerLINUX和z/OS提供支持。IBM在可预见的未来将会持续支持Swift和Kitura的发展。
* 因为Swift是一种编译型语言，使用Kitura的Web应用通常会比那些脚本语言如PHP、Python、Perl、Ruby跑得更快。

## 为什么不用Kitura?

* 因为Kitura和Swift总的来说还是太年轻，你可能遇到需要的库没有对应的Swift版本。即使你可能不介意自己写代码来集成C或者C++库，那也需要大量的工作。
* Kitura is a very low-level framework, along the lines of Laravel or Ruby on Rails, so while it’s very quick to implement something like a REST interface that provides JSON responses for consumption by, say, a client app on iOS, building something like a blog will take considerably more work than it would using a more full-featured web framework or content management system like WordPress, Drupal, or Alfresco. That being said, building full-featured web sites with Kitura is certainly possible, as later examples in this book will show.
* Because compiling Swift code is currently not widely supported outside of macOS, Ubuntu Linux, and the IBM operating systems mentioned above. Most notably, Windows support is missing, and I sincerely hope there are some people from Apple and/or Microsoft and/or IBM working on that. There are *unofficial* ports of Swift to Windows and other Linux flavors, as well as FreeBSD, but your mileage may vary on the effectiveness of these systems.

## What You Should Know

This book makes some assumptions about what you already know about software development and the workings of the web. Please review the list below. If anything in the list is unfamiliar to you, I suggest you bone up on those things before diving deep into this book.

* **Software development with Swift.** Though this book will periodically teach or review certain aspects of Swift which may be unexpected or unusual for those not strongly familiar with it, it is not intended as a thorough introduction to Swift programming. At the least, you should have read Apple’s *The Swift Programming Language* book, though I’ll accept just reading the “A Swift Tour” section of the book if you’re already familiar with contemporary object-oriented programming languages such as C# or Java. You should already have Swift installed on your development machine and know how to build and run a basic command-line application. You do *not* need to be an experienced iOS or macOS developer; in fact, if you are, there’s actually probably a few things you will need to *unlearn* to become an effective Kitura developer. See the [CLI Swift for Cocoa developers](appendices/a-savvy-devs.md) appendix for more information if this applies to you.
* **General knowledge about HTTP.** The Hypertext Transfer Protocol is how web clients and web servers talk to each other. You should know about the different parts of a URL. You should know the meaning and usage of common HTTP status codes like 200 OK and 404 Not Found, as well as common client and server HTTP headers.
* **HTML.** The Hypertext Markup Language is how a simple text file can be interpreted by a web browser as a functional web page. You should know common HTML tags and page structure. Earlier chapters in this book will not deal with server responses in HTML, but later ones will.
* **SQL and associated concepts.** Structured Query Language is used by relational database systems such as PostgreSQL, MySQL, SQLite, or Microsoft SQL Server to read and manipulate data. You should understand common database structures such as tables, rows, and columns.
* **Swift Package Manager.** This is the modern way to add “packages” of additional code to your project. As I expect a major part of the audience of this book will be Cocoa developers who are familiar with using CocoaPods or Carthage for this purpose, this book includes an [appendix chapter introducing SPM](appendices/b-spm.md). Additionally, you should understand the concept of semantic versioning; the appendix will cover this as well.
* **Git.** You should have Git installed on your development server, as this is how Swift Package Manager will fetch packages. Ideally, you have some experience with using Git yourself and basic concepts of version control systems. If you wish to use a different version control system for your sites, that’s fine, but the chapter in this book on creating middleware will involve creating a new Swift Package Manager package, which requires experience with Git.


## Other Learning Resources

If you don’t like this book or just want a few more long-form tutorials for Kitura, here are some to consider.

* [*Server-Side Swift*](https://www.hackingwithswift.com/store/server-side-swift) is another e-book that covers Swift; this one is by Paul “twostraws” Hudson, who has written several books on Swift development. At US$40, Hudson’s book is certainly more pricey than this one, but in both cases you probably get what you paid for… I haven’t read *Server-Side Swift* myself, but I’ve read one of Hudson’s other books and found it to be pretty high-quality stuff.

* David Okun, Developer Advocate at IBM, has posted two entry-level articles at RayWenderlich.com: [Kitura Tutorial: Getting Started with Server Side Swift](https://www.raywenderlich.com/180721/kitura-tutorial-getting-started-with-server-side-swift), which covers basic REST responses and CouchDB database integration (the latter of which is not covered in this book), and [Kitura Stencil Tutorial: How to make Websites with Swift](https://www.raywenderlich.com/181130/kitura-stencil-tutorial-how-to-make-websites-with-swift), which covers templating with the Stencil templating engine.

* Like blogs? I suggest adding the [Swift@IBM Blog](https://developer.ibm.com/swift/blogs/) to your feed reader of choice. Its updates are sporadic, but often content-rich.

* If you like to learn with video, LinkedIn Learning (formerly Lynda.com) has released a video series entitled [Learning Server-Side Swift Using IBM Kitura](https://www.linkedin.com/learning/learning-server-side-swift-using-ibm-kitura). You can watch the first couple videos in the series without needing an account. LinkedIn Learning/Lynda.com subscriptions can be pricey, but both offer you free one-month trial subscriptions.

## Getting Help

You are not alone. As you go along, if you get stumped by something, don’t hesitate to reach out for help and clarification.

The Swift@IBM team site has a [public Slack instance](http://swift-at-ibm-slack.mybluemix.net/). (Slack is a feature-rich yet resource-intensive chat application targeted towards teams and workgroups.) There are several channels including #kitura specifically for Kitura discussion and #general which is good for general discussion about Swift development and other topics in the ecosystem. You can find me there under the username “nocturnal.” Feel free to reach out to me if you’re having any trouble with something in this book.

If Slack’s not your thing, you can also join the [Freenode IRC network](https://freenode.net). It doesn’t have any Kitura-specific channels currently (unfortunately), but it does have the #swift-lang channel which is great for general Swift discussion; there’s lots of smart people there. There may be other Swift-related channels in the IRC universe, but I like the Freenode network because its focus on open-source software means that if you need help with any other open-source (and some not-so-open-source) software you use throughout the day, you can probably find a channel related to it on Freenode. If you’re a Cocoa developer, the #iphonedev and/or #macdev channels may also be of interest; #iphonedev-chat is a fun channel for off-topic banter with others in the community. On Freenode, you can find me using the “_Nocturnal” alias. Again, feel free to reach out and say hi!

The [official Swift forums](https://forums.swift.org/) have a [Kitura category](https://forums.swift.org/c/related-projects/kitura). As I write this, the category is still fairly new and hasn’t seen much activity; also, I find the forum system that they are using to be quite confusing and borderline unusable. Nonetheless, forums are often a better place to ask long-form questions than the chat-based systems listed above.

Finally, don’t forget about the GitHub issue queues on most projects hosted there. They’re generally intended for reporting bugs and such, but you’re generally welcome to ask for help with usage there too.

## Notably Absent Topics

There are some topics that this book does not currently cover, but perhaps should. (Perhaps it will in future revisions.) I list them here so that you may peruse these topics on your own, should you so desire, as well as explain why I omitted them.

### `kitura create`

[`kitura create`](http://www.kitura.io/en/starter/generator.html) is an optional CLI tool which can be used in place of `swift package init` to start a new Kitura project. It can automatically add the Kitura dependency to your project as well as insert boilerplate code into your project based on your answers to some questions it asks you.

I ultimately decided not to cover this tool in this book because it is written in Node.js, and that's a rather large dependency to install for those that don't already have it (why the authors of this tool chose to write something in JavaScript when they could have chosen Swift itself is beyond me); also, I feel that it is very important to learn how to do “by hand” the things that this tool does for you, such as defining router paths.

### Swift-Kuery-ORM

Kuery is a package for integrating with SQL-based database management systems. The [chapter on Kuery](5-kuery.md) and following chapters use Kuery as a rather thin interface between the application and the underlying SQL engine - just a step up from writing direct SQL queries, really. [Swift-Kuery-ORM](https://github.com/IBM-Swift/Swift-Kuery-ORM) abstracts things further by basically letting you save and load objects themselves directly to and from the database, at least from the perspective of your app - of course things are still ending up as SQL queries at the very bottom, but manually breaking objects down into insert or update queries or building them back up from the result of select queries is handled for you.

I didn't cover Swift-Kuery-ORM as I personally am more familiar with using databases without ORM tools. However, as using an ORM is quite common in some ecosystems, I can appreciate that some experienced web developers may be more comfortable using them than not. Thus, I may add coverage of Swift-Kuery-ORM in the future, once I improve my own familiarity with it.

### Automated Testing

Automated testing is an important concept in ensuring software quality and avoiding bugs and functionality regressions as software evolves. Kitura and its related packages have rather good automated tests, and I encourage anyone building a “production-ready” project in Kitura also implement automated testing - especially if that project is intended to be a package used by others.

However, automated testing is a rather broad and complex topic, and for Kitura projects it can be doubly complex since the test has to both run the server part of it as well as the client part, ensuring the server is returning the appropriate responses. I ultimately decided that this all was just too complex to cover competently in what is intended to be an introductory-level, wide-but-shallow Kitura tutorial. But perhaps my mind will be changed in the future.

### Deploying

Okay, so you’ve written a great Kitura web app, and it runs fine on your local machine; now how do you get that up and running on the public internet? There are many options, from IBM’s own [Bluemix](https://console.bluemix.net/docs/runtimes/swift/getting-started.html#getting-started-tutorial) cloud hosting service to using Docker containers to simply just building the app as normal and letting it go. The latter is my preferred method, though I know it’s pretty much unheard of in today’s Linux container culture.

Given that wide variance in how things can be deployed, and all the various complexity that goes along with such things, I haven’t decided on a way to cover it just yet.
