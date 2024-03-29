Learning Objectives for Tyler
-------------------

After completing this unit, you'll be able to:

* Explain the Lightning Web Components programming model.
* List the benefits of using Lightning web components.
* Find what you need to get started developing Lightning web components.

An Open Door to Programming with Web Standards
----------------------------------------------

It's time to bring together your Salesforce knowledge and familiarity with standard technologies like HTML, JavaScript, and CSS to build the next generation of Salesforce apps. Use these common standards to build components for your Salesforce org while maintaining compatibility with existing Aura components.

Lightning Web Components is focused on both the developer and user experience. Because we've opened the door to existing technologies, you use the skill you've developed outside of Salesforce to build Lightning web components. All of this is available to you without giving up what you've already accomplished with Aura components.

> Did you notice a capitalization difference in that last paragraph? If so, you have a keen eye. We capitalize all the words when we refer to the Lightning Web Components programming model. We only capitalize the first word when we refer to the components, themselves, as Lightning web components.

> Also, the Lightning Components programming model you've been using is now called Aura Components. The components themselves are called Aura components.

Before You Go Further
---------------------

You should have a basic understanding of Salesforce DX projects and Salesforce CLI. You'll also need to use a properly configured org in your Trailhead account and VS Code with the Salesforce Extension Pack. You can learn about all of this by completing [Quick Start: Lightning Web Components](https://trailhead.salesforce.com/content/learn/projects/quick-start-lightning-web-components).

If you're using a Developer Edition org you've attached to your Trailhead account, you need to deploy My Domain in Setup (Trailhead Playground orgs automatically have My Domain deployed).

Why Lightning Web Components?
-----------------------------

Modern browsers are based on web standards, and evolving standards are constantly improving what browsers can present to a user. We want you to be able to take advantage of these innovations.

Lightning Web Components uses core [Web Components](https://github.com/w3c/webcomponents/) standards and provides only what's necessary to perform well in browsers supported by Salesforce. Because it's built on code that runs natively in browsers, Lightning Web Components is lightweight and delivers exceptional performance. Most of the code you write is standard JavaScript and HTML.

You'll find it easier to:

* Find solutions in common places on the web.
* Find developers with necessary skills and experience.
* Use other developers' experiences (even on other platforms).
* Develop faster.
* Utilize full encapsulation so components are more versatile.

And it's not like web components are new. In fact, browsers have been creating these for years. Examples include `<select>`, `<video>`, `<input>`, and any tag that serves as more than a container. These elements are actually the equivalent of web components. Our goal is to bring that level of integration to Salesforce development.

Simple Component Creation
-------------------------

The beauty of adhering to web standards is simplicity. You don't need to ramp up on quirks of a particular framework. You simply create components using HTML, JavaScript, and CSS. Lightning web component creation is one, two, three steps. I'm not kidding. It's really that simple. You create (1) a JavaScript file, (2) an HTML file, and optionally (3) a CSS file.

* HTML provides the structure for your component.
* JavaScript defines the core business logic and event handling.
* CSS provides the look, feel, and animation for your component.

Those are the essential pieces of your component.

Here's a very simple Lightning web component that displays “Hello World” in an input field.

**HTML**

``` <template><input value={message}></input></template> ```

The `template` tag is a fundamental building block of a component's HTML. It allows you to store pieces of HTML.

**JavaScript**

``` import { LightningElement } from 'lwc'; export default class App extends LightningElement { message = 'Hello World'; } ```

We get into the import statement and class declaration details later, too.

**CSS**

``` input { color: blue; } ```

At minimum, all you really need is an HTML file and a JavaScript file with the same name in the same folder (also with a matching name). You deploy those to an org with some metadata and you're good to go. Salesforce compiles your files and takes care of the boilerplate component construction for you automatically.

Play Time
---------

Let's go look at our files. Use an integrated development environment (IDE), to try out your components, tinker with them, and see instant results. If you don't already have an IDE you love, follow along as we use the third-party IDE, LWC.studio which includes base components and styles to help you create LWC prototypes.

1.  Navigate to [LWC.studio](https://app.lwc.studio/).
2.  Use your GitHub account to log in and then click **New**.
3.  Copy the above HTML, JavaScript, and CSS examples into the corresponding app._x_ files in the example. Replace everything in the app files.
4.  Save the files.

The **Stories** tab shows the output.

Lightning Web Components and Aura Components Do Work Together
-------------------------------------------------------------

Wondering if you can keep your existing Aura components? Yes you can! You can use Lightning web components without giving up your existing components. You'll likely migrate your existing components to the Lightning Web Component model eventually, but we're introducing Lightning web components without taking anything away from the existing support of the Aura components. Aura components and Lightning web components live well together.

In fact, Aura components can contain Lightning web components (though not vice-versa). But a pure Lightning web components implementation provides full encapsulation and evolving adherence to common standards.

Cool Stuff You Can Use
----------------------

To develop Lightning web components efficiently, use the following tools and environments.

* **Dev Hub and Scratch Orgs**
    Scratch orgs are disposable Salesforce orgs to support development and testing. Dev Hub is a feature that manages your scratch orgs. Both are part of the Salesforce DX tool set. Salesforce DX is an integrated set of development tools built and supported by Salesforce.
    * **Salesforce Command Line Interface (CLI)**
        The Salesforce CLI provides a quick way to run operations for creating and configuring scratch orgs, and also for deploying components. This is also part of the Salesforce DX tool set.
    * **Lightning Component Library**
        The reference for both Aura and Lightning web components and how to use them is found at [https://developer.salesforce.com/docs/component-library/overview/components](https://developer.salesforce.com/docs/component-library/overview/components). You can view the library through your org's instance, too, at http://&lt;MyDomainName&gt;.lightning.force.com/docs/component-library. By viewing the library through your instance, you see only the correct version for your org. And, as you create your own custom components, they appear in the library too.
* **GitHub**
    We share extensions, samples, and more through GitHub repos. Get a GitHub account to make sure you can take advantage of these offerings.
    * **Visual Studio Code Salesforce Extension Pack**
        We've focused on Visual Studio as a development tool, providing an integrated environment for you to build your components. The Salesforce Extension Pack for Visual Studio Code provides code-hinting, lint warnings, and built-in commands: [https://marketplace.visualstudio.com/items?itemName=salesforce.salesforcedx-vscode](https://marketplace.visualstudio.com/items?itemName=salesforce.salesforcedx-vscode).
    * **Lightning Web Components Recipes**
        We provide a GitHub repo to help you see how Lightning web components work. You can clone, tinker, and publish this mix of samples to your own scratch org and see them in action. Get it at [https://github.com/trailheadapps/lwc-recipes](https://github.com/trailheadapps/lwc-recipes).
    * **E-Bikes Demo**
        This GitHub repo is another great way to see how Lightning web components work. The e-bikes demo is an end-to-end implementation of Lightning web components to create an app. Try this example in your own scratch org. Get it at [https://github.com/trailheadapps/ebikes-lwc](https://github.com/trailheadapps/ebikes-lwc).
    * **Lightning Data Service (LDS)**
        Access data and metadata from Salesforce via [Lightning Data Service](https://developer.salesforce.com/docs/component-library/documentation/lwc/lwc.data_ui_api). Base Lightning components that work with data are built on LDS. Customize your own components to take advantage of LDS caching, change-tracking, performance, and more.
    * **Lightning Locker**
        Lightning web components that belong to one namespace are secure from components in a different namespace through [Security with Lightning Locker](https://developer.salesforce.com/docs/component-library/documentation/lwc/lwc.security_locker_service). Lightning Locker also promotes best practices that improve the supportability of your code by only allowing access to supported APIs and eliminating access to nonpublished framework internals.

A Look Ahead
------------

![Welcome to the world of Lightning web components](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lightning-web-components-basics/discover-lightning-web-components/images/1a165d07ca7564fce8db0d17df843cb2_lwc-basics-welcome.png)

We'll use the eBikes demo to see what you can do with the HTML and JavaScript files.

Resources
---------

* [_Developers' Blog_: Introducing Lightning Web Components](https://developer.salesforce.com/blogs/2018/12/introducing-lightning-web-components.html)
* [_Lightning Web Components Dev Guide_: Lightning Web Components and Aura Components Working Together](https://developer.salesforce.com/docs/component-library/documentation/lwc/lwc.interop_intro)
