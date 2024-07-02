---
tocOrder: 8
title: 'Chapter 5: Collaborate'
---
![Chapter 5: Collaborate](image/ch05.png)

“Responsive is not a project. Responsive is a permanent new way of working.”

—SCOTT KELTON JONES, *Expedia*

I’VE SPENT THE PAST twenty years designing (and redesigning) websites. When I got started, a paper-first way of working made sense. Wireframes and Photoshop comps were the easiest way to communicate with teams and with clients—everybody had a printer, everybody could comment on a PDF. Here’s how I once described my job: “You know what I think I’m going to do today? I’m going to draw some pictures of hypothetical future web pages and see if anyone likes them” ([http://bkaprt.com/gr/05-01/](http://bkaprt.com/gr/05-01/)).

But the old ways of working just don’t work anymore. Pictures of web pages, constructed in Photoshop and distributed as PDFs—or worse, hard copies—seem like vestiges of another era, like watching a television broadcast of actors in a radio program speaking their lines. That’s why advocates for agile methodologies or Lean UX recommend moving away from set-in-stone requirements, waterfall processes, and the fetishization of deliverables.

And yet, making changes so teams can work together in new ways requires more than an idealistic vision. Organizational structures often limit how people collaborate. New tools and libraries must be built or purchased, and they’re not included in the budget or timeline. Stakeholders accustomed to working in a familiar process are resistant to change.

Responsive is your best opportunity to fix the way people work together. You may never get a better chance to change your team dynamics. In fact, responsive will force you to work in new ways—whether you want to or not. Frank Chimero, author of *The Shape of Design,* noted:

> Everyone that I’ve spoken with that’s worked on a large responsive project with a big client says that the process disrupts workflows, expectations, and work culture. Simply put, the edgelessness of the web tears down the constructed edges in the company. Everything is so interconnected that nobody has a clear domain of work any longer—the walls are gone, so we’re left to learn how to collaborate in the spaces where things connect ([http://bkaprt.com/gr/05-02/](http://bkaprt.com/gr/05-02/)).

Rather than leave your team to develop a new way of working on the fly, let’s talk about how everyone’s participation in the design and development process will change. Let me be clear: this section is not intended to provide a detailed guide for designers and developers about how their workflows will evolve—there are many other resources available to help answer that question, some of which appear in the back of the book. This section explains what everyone on your team needs to know to effectively collaborate in a responsive design process.

## ORIENTATION

Plan to conduct an orientation session—or series of sessions—for everyone who might be involved in the redesign process. Think broadly about whom to invite, because QA testers, customer service representatives, and even lawyers will potentially be affected by this change.

While designers and developers probably have a good understanding of what going responsive means, you need to build a shared vision with the rest of the team. The goal of this orientation is to help everyone understand what will be different, what new language will be used, and what will be expected of them.

These are a few topics you might consider for your agenda. (You can download these talking points in PowerPoint and PDF formats: [http://bkaprt.com/gr/05-03/](http://bkaprt.com/gr/05-03/)).

* **Unfamiliar jargon.** What’s a breakpoint? What’s a media query? Teams may not need to know *how* to build websites using these concepts, but they do a need a level of comfort with new vocabulary. (A glossary with common terms appears in the back of the book and online: [http://bkaprt.com/gr/05-04/](http://bkaprt.com/gr/05-04/)).
* **Site traffic.** Do you have analytics data showing what percentage of your traffic comes from smartphones and tablets? That’s often the most compelling argument for going responsive, because it shows just how important “mobile” is to your organization. You might supplement that data by sharing industry trends showing the rise of mobile devices and the proliferation of mobile platforms—even if your traffic isn’t exploding with mobile visitors, your competitors’ might be.
* **Mobile first.** Many organizations toss the buzzword “mobile first” around without having a shared understanding of what it means. Spend some time coaxing your team away from their fixation on the desktop and explain what a mobile-first decision-making process means to you.
* **Fluid designs.** Focusing on specific device types—mobile, tablet, and desktop—is meaningless when responsive designs are completely fluid. Yet stakeholders will fixate on these labels. Explain why avoiding device-specific discussions helps avoid making flawed assumptions.
* **Pixel perfection.** Stakeholders must move away from obsessing over pixel-perfect details. Not every device will get an identical experience, and that’s okay. Your orientation session should cover the basics of progressive enhancement and what it means to develop for all devices holistically.
* **Prototype reviews.** The way team members offer feedback on work-in-progress designs is likely to change. Explain how stakeholders will access prototypes from their mobile device or on shared devices in the lab (and explain that you won’t be distributing PDFs).
* **Device support.** Even though you expect the website to work on most every device, you’ll need to select a subset of devices and browsers for testing. Share a list of the ones you plan to support, and why.
* **Reporting and analytics****.** While key metrics don’t change with a responsive design, stakeholders accustomed to getting reports on a desktop website will need to look at the data in new ways. How will you evaluate the new site?

## PROTOTYPING

Much ink has been spilled about the value of agile methods, iterative design, and functional prototyping. Some organizations have embraced these methods wholeheartedly. Others still cling to static comps.

Responsive can create a “lightbulb moment” for teams and stakeholders, because it’s simply not feasible to demonstrate how designs will render and reflow at different breakpoints using static mockups. Teams accustomed to receiving documents or presentations will work together on reviewing functional prototypes. Joe Stewart, Partner at Work & Co, which teamed up with Dean Cookson, CIO of Virgin America on that company's responsive redesign, said:

> Prototyping is our number one tool. Our philosophy on how to go about a responsive project is to race to a prototype as quickly as possible. We actually never once made a presentation, but we did constantly work on making prototypes. The very first time we got to meet Dean and the Virgin America team, we showed them a responsive prototype ([http://bkaprt.com/gr/05-05/](http://bkaprt.com/gr/05-05/).

A shift to responsive prototyping changes the way design and development teams collaborate and changes the way stakeholders respond to the work.

### Breakpoints

Resize a browser window on a responsive website, and notice how the design reflows or flexes. Perhaps it shifts down from three columns to two, and then to a single column, or images and text that once sat side by side now stack vertically. These changes are defined using CSS and media queries, and the points at which the design shifts are called *breakpoints*. (The previous chapter discussed content choreography; breakpoints may be thought of as the way content choreography gets coded.)

In a responsive project, even teams that embrace the concept of device-agnostic design will find themselves pulled into discussing device types when the question of breakpoints arises. In an adaptive grid, the design “snaps” at specific sizes, but in a fully responsive design, the layout is completely fluid.

Breakpoints do not and should not neatly map to device sizes. If you’ve been following along at home, the reason should be obvious. There is no single definition for how wide a “smartphone” screen is; new devices come on the market all the time that defy expectations of a particular device type (hello, iPhone 6+!). Breakpoints are defined by the *content*—when line lengths get too long or whitespace becomes too big, designers decide to insert a breakpoint.

Your designers will also tell you that breakpoints don’t all happen at once—while *major* breakpoints are defined to indicate major shifts in the layout, a number of *minor* breakpoints will also be defined to, say, manage small changes in the way navigation options appear in the header. A combination of major and minor breakpoints helps the responsive design work fluidly across all screen sizes, not just a handful of preselected resolutions.

Exactly where to place major and minor breakpoints is a decision best left to designers and developers—you don’t need a team meeting to discuss them. But you *do* need a way to talk about the relationship between screen sizes and breakpoints. Here are some tips for doing that well:

* **Don’t** **identify breakpoints based on screen resolutions.** It’s tempting to look at your analytics data (or your iOS devices) and choose breakpoints based on known screen sizes. A content-driven approach to defining breakpoints places them wherever needed to make line lengths and image sizes appropriate for any screen width.
* **Don’t talk about breakpoints using device types.** Trust me, you will have meetings where you discuss the “smartphone” or “tablet” size of the website. Trust me, it will be a hard habit to break. Trust me, you will be better off if you do. Device types carry with them a bundle of assumptions about capabilities and scenarios of use that aren’t always true of a given screen width. Some teams get around this by using t-shirt sizes (or bears) as a way to refer to a broad category of screen size without implying anything about connection speed, input mechanism, or use cases.
* **Don’t freak out** **about small differences.** When reviewing prototypes in context on different devices, stakeholders may agonize over minor differences in sizing, layout, or alignment. Remember: the goal isn’t to have the site look exactly the same on every device. It’s to create a website that *works* on every device. Don’t waste time sweating the small stuff.

### Prototyping tools

Many teams say they move into code much more quickly and make more of their decisions based on a working prototype. Dave Augustine from Airbnb said:

> This whole thing was prototyped in code, for the most part. We didn’t receive Photoshop comps of what it looked like at different breakpoints. We received code, an actual functioning website ([http://bkaprt.com/gr/01-45/](http://bkaprt.com/gr/01-45/)).

Applications like Sketch ([http://bkaprt.com/gr/05-06/](http://bkaprt.com/gr/05-06/)), Macaw ([http://bkaprt.com/gr/05-07/](http://bkaprt.com/gr/05-07/)), InVision ([http://bkaprt.com/gr/05-08/](http://bkaprt.com/gr/05-08/)), and Edge Reflow from Adobe ([http://bkaprt.com/gr/05-09/](http://bkaprt.com/gr/05-09/)) offer prototyping capabilities so designers can quickly create responsive designs, review them in context, and solicit feedback from other members of the team, without requiring actual coding.

For functional prototyping and designing in the browser, front-end frameworks (a.k.a. CSS frameworks) offer configurable features—typography, forms, buttons, and reusable components, all within a responsive grid. Of the many frameworks out there, some popular ones are Bootstrap ([http://bkaprt.com/gr/05-10/](http://bkaprt.com/gr/05-10/)), Foundation ([http://bkaprt.com/gr/05-11/](http://bkaprt.com/gr/05-11/)), Gumby ([http://bkaprt.com/gr/05-12/](http://bkaprt.com/gr/05-12/)), and Skeleton ([http://bkaprt.com/gr/05-13/](http://bkaprt.com/gr/05-13/)). Teams often report that they start with a third-party framework and heavily customize it for their own needs. These frameworks can be quite useful for prototyping, even by people with modest development skills. (There are some downsides to using them for production code, but let’s not go there.)

### Deciding in the browser

Reports of the death of Photoshop are unevenly distributed. Despite the enthusiasm for prototyping solutions—what’s been called “designing in the browser”—teams may find code-based prototyping to be slower than other methods. If you’re changing your workflow and testing out new frameworks, you may need more time in the project plan for training and collaboration.

Responsive projects require new tools and skills, but your team can keep using the applications and workflows they’re most comfortable (and fastest) with while testing out new ones. Teams that have adopted code-based prototyping methods still report using Photoshop, Illustrator, InDesign, and other static tools for developing the overall visual system and wireframes to present design decisions to stakeholders. Prototyping tools do not entirely replace existing applications—we need a variety of techniques to create great responsive designs.

Dan Mall famously quipped, “Let’s change the phrase ‘designing in the browser’ to ‘deciding in the browser’”([http://bkaprt.com/gr/05-14/](http://bkaprt.com/gr/05-14/)). The point of prototyping isn’t to have code-based methods replace the *design* process—it’s more important that it modernize the *review* process. Let the team use whatever tools and methods it needs to get to a functioning prototype. But stakeholders should be expected to provide feedback on the prototype, gently guided away from expecting static comps for every breakpoint.

Scott Kelton Jones said he found that stakeholders from Expedia prefer reviewing prototypes—his teams never go back to static documents after they make the switch:

> Whether it’s me as I’m judging design solutions, or it’s my boss, or it’s the head of Expedia, once they see a prototype, once they see something being designed in code, people don’t go back to static Photoshop comps. Once they get spoiled, people start saying, “What is this going to work like on the phone? What is it going to work like on the tablet? How is this really going to work?” You don’t get to go back to static comps ([http://bkaprt.com/gr/01-20/](http://bkaprt.com/gr/01-20/)).

Livia Labate from Marriott said that the value for them in using prototypes for reviews was faster turnaround and iteration. Teams would present work-in-progress, then quickly turn around changes—even updating the prototype during the meeting, which dramatically shortened time required for review and feedback. The functional prototype also meant that stakeholders could review and provide feedback at any time, without requiring a member of the design team to hold their hand:

> If stakeholders have any questions about how users do X, Y, or Z, they look at the prototype. It’s immensely powerful. People can access it at any time and they don’t need me or another expert from our responsive program to explain how the site is going to work. They can just look at it, play with it, and they’ll understand ([http://bkaprt.com/gr/01-53/](http://bkaprt.com/gr/01-53/)).

Teams that use front-end frameworks and prototyping to speed up the design process and help stakeholders envision how the site will work often make the natural leap to developing prototypes and production code from a pattern library.

## DESIGN SYSTEMS AND PATTERN LIBRARIES

Responsive design often goes hand in hand with developing a reusable set of design styles and components—sometimes called a *pattern library,* *design system, style* *guide,* or *framework*. The terms *module* and *component* are likewise used interchangeably (although component does have a more specific meaning in CMS development). Teams working on a pattern library should start by defining the language they’ll use to describe patterns and modules ([http://bkaprt.com/gr/05-15/](http://bkaprt.com/gr/05-15/)).

While it’s totally possible to implement a responsive design without a pattern library—and there are many good reasons for building a design system that go beyond responsive web design—having a modular framework makes the responsive design process go more smoothly.

Rather than starting with pages or page templates, teams first create reusable modules or components that are later assembled within a grid structure to create pages. These components are often described as “LEGO blocks” that can be combined in different ways.

Jeremy Keith from Clearleft, which partnered with Code for America on their responsive redesign, recalled that the pattern library was their main deliverable:

> Some people call it a front-end style guide or a pattern library. Essentially it means breaking down the components of a page or a site into their atomic pieces and making sure that everything stands alone and works by itself. We deliver a collection of all those pieces as the main deliverable. We still provide pages, but pages are just examples of the patterns in action, almost like assembling LEGO blocks ([http://bkaprt.com/gr/05-16/](http://bkaprt.com/gr/05-16/)).

If you remember the content modeling exercises from Chapter 4, this concept may sound familiar. The process of defining a more granular content model is closely related to the process for creating reusable design patterns.

I often describe three levels of modularization:

* **Front-end patterns.** A pattern library may exist solely as reusable pieces of front-end code, in a browsable format that explains how each pattern can be used. Rather than reinventing the wheel each time a new calendar widget or login form is needed, teams can grab a version that has already been designed and tested. But because the styles or code snippets are merely copied and pasted, there’s no built-in management or enforcement of the design system—teams can modify the styles as they see fit, and changes to the system cannot be rolled out automatically.
* **Content modeling.** Design systems are often thought of as, well, design—a foundational visual language for common styles like tabs, buttons, tables, charts, and graphs. But as we saw in Chapter 4, content can also be structured and stored in a modular way. Like chocolate and peanut butter, design systems and content models go better together. If your pattern library only shows text, button labels, and form elements with dummy text, and your content model shows headings, teasers, and microcopy character counts, the next step in your journey is to fit these two systems together.
* **Backend components.** Components can also be implemented through the content management system, enabling designers and developers to construct and publish pages from reusable modules on the backend. A solid implementation means that changes can be made and tested on components, then rolled out across the entire system—much more efficient than updating each instance of front-end code. Capital One estimated that they publish 2,500 unique pages (encompassing a total of 4,000 adaptive page variations), but need only twenty backend components to maintain them ([http://bkaprt.com/gr/01-39/](http://bkaprt.com/gr/01-39/)).

### Benefits of modularization

Code for America ([http://bkaprt.com/gr/05-17/](http://bkaprt.com/gr/05-17/)), MailChimp ([http://bkaprt.com/gr/05-18/](http://bkaprt.com/gr/05-18/)), and Starbucks ([http://bkaprt.com/gr/05-19/](http://bkaprt.com/gr/05-19/)) have all shared their pattern libraries to help other companies understand the value of these systems.

Focusing on modular pieces over pages has many benefits:

* **It’s inherently responsive.** Flexible modules within a fluid grid system make it easy for designs to reflow across different screen sizes and breakpoints. Joe Stewart from Work & Co described the value of the modular system for Virgin America: “Anything that you do will automatically be responsive. If it fits in one of these modules, it will be responsive because the module system itself is naturally responsive” ([http://bkaprt.com/gr/05-05/](http://bkaprt.com/gr/05-05/)).
* **It improves consistency.** Page-based models can be wildly inefficient, virtually guaranteeing that sites will store duplicate content and display variations in design. Building and enforcing a modularized system means that content or design elements can be updated in one place and distributed site-wide, which makes it easier to maintain quality and consistency.
* **It supports** **prototyping.** Once the design system has been built, teams can quickly and easily create functional prototypes from the reusable modules. Tyler Fleck, Principal Web Designer at Expedia, said, “Once we published our documentation site that outlined all the core components, and showed what you could achieve by using the design and front-end framework, people really started to see the value of it in terms of how quickly we could assemble more finished UIs” ([http://bkaprt.com/gr/05-20/](http://bkaprt.com/gr/05-20/)).
* **It’s faster to deploy.** It takes time to develop a design system, but once it’s in place, a responsive design can be implemented more easily. Dave Augustine from Airbnb noted that their responsive relaunch was “one of the quickest and smoothest launches we’ve had” due to their front-end framework ([http://bkaprt.com/gr/01-45/](http://bkaprt.com/gr/01-45/)). Capital One pulled off a complete responsive redesign in just two months, giving all the credit to their modular design system and component CMS—and their heroic UI Architect, Brian Dillon ([http://bkaprt.com/gr/01-39/](http://bkaprt.com/gr/01-39/)).
* **It streamlines testing and** **QA.** Components can be tested and validated once and then rolled out site-wide, which speeds up the testing and QA process. Brian Dillon of Capital One said, “The great thing about our site being so modular is that all we have to do is test an update on one or two pages and that meets the needs of our full regression testing. We don’t have to review all 2,500 pages to know that the new module is going to work. It makes it a lot easier to quickly go through all those devices and only test what we need” ([http://bkaprt.com/gr/05-21/](http://bkaprt.com/gr/05-21/)).
* **It’s cheaper** **in the long run.** Stakeholders get in the habit of expecting a custom design—their own special snowflake—for every single page. The BBC found bespoke page design to be much more costly than working with pre-designed and tested components. Niko Vijayaratnam, formerly Senior Product Manager at BBC Digital, stated, “It focuses people on the fact that creating new patterns costs time and money. Having a central pattern library, having that as the common language that we can all get behind, is really helping us” ([http://bkaprt.com/gr/05-22/](http://bkaprt.com/gr/05-22/)).

### Design systems and responsive design

Teams that have wanted to create a modularized framework may find that a responsive redesign is the right time to do it—it’s an easier sell when presented as part of a responsive program, as Livia Labate from Marriott found:

> Standards and a design system were things that we needed. But how do you make a business case to unify your visual identity? That’s incredibly hard, especially as you compete against a hundred other initiatives and priorities. Unifying the visual system in the interest of making it easier to code and maintain our front end is a much more compelling business case. So things like that were absolutely possible in the context of making the site responsive ([http://bkaprt.com/gr/01-53/](http://bkaprt.com/gr/01-53/)).

Some companies find that implementing a design system *before* going responsive means the responsive design process goes more quickly. Rob Huddleston of Capital One said, “Let’s think design system first. Design systems and patterns are probably the best place to start. They give you the most flexibility moving forward in terms of scalability and future-forward thinking” ([http://bkaprt.com/gr/05-21/](http://bkaprt.com/gr/05-21/)).

The challenge in implementing a pattern library is getting distributed teams to use it—rather than having them do their own thing or feel constrained by solutions that don’t meet their needs. Marriott and Fidelity both have full-time employees responsible for their design systems. These team members lead monthly meetings to share new patterns and discuss changes to the system. They also oversee a governance process to ensure the pattern library is implemented as expected, and resolve issues that arise when teams need a style that isn’t documented yet.

## STAKEHOLDER REVIEWS

When I talk to clients about stakeholder reviews, they describe their typical approach to getting feedback from the wider organization:

* Teams ask for feedback on content in Word documents, which doesn’t happen. Stakeholders demand to see polished Photoshop comps of every page.
* Photoshop comps get exported to PDF, then circulated via email or printed out so stakeholders can follow along when designs are projected on screen in meetings.
* Stakeholders provide feedback via email or in the PDF. Or by fax. Sometimes they handwrite comments and fax them. Everyone loves faxes.
* Feedback is provided on the design direction. And content. And functionality. Anything is fair game, really.
* Teams aggregate feedback and make changes. Ideally, this would be the end of the review process, but stakeholders demand a final round of comps before giving approval.
* Finally the work is ready to go into development. But changes to content from the last round of comps didn’t get reflected in the latest Word documents. Someone’s feedback (probably sent via fax) was mysteriously overlooked.
* Teams spend time tracking down and resolving conflicting feedback. Fixing version control problems seems to take more time than the actual design work.

When we talk through this process, everyone laughs, but it’s an awkward laugh, like they’re ashamed. During a break, meeting attendees pull me aside and hiss under their breath, “Our review process is broken. How do we fix it?”

Responsive design can be a forcing function that helps solve this problem, but only if you spend the time getting stakeholders on board. In the same way that going responsive requires a more collaborative, iterative process among design, development, and content teams, it also requires active collaboration with the rest of the organization.

### Prototypes, not PDFs

Showing prototypes is the best advertisement for responsive design. Scott Childs of Capital One said, “We realized during the selling of this project that showing people how it worked and what it did, what responsive was in a browser or on a device, was what sold the project for us” ([http://bkaprt.com/gr/01-39/](http://bkaprt.com/gr/01-39/)).

Stakeholders may still want to focus on device types—“What does the tablet website look like?” or “My widget needs to be above the fold.” The review and approval process needs to communicate that responsive design is completely flexible, and their “thing” doesn’t “live” in a particular place. A prototype makes that clear.

Many teams report that they make a working prototype available on the server for comment at any time—which means that stakeholders must be made aware that work-in-progress prototypes will occasionally seem kind of janky. Stakeholders should be taught to look at the prototype on their personal phones or tablets—or on devices from the device lab—in addition to simply resizing the browser. Stakeholders may also benefit from using emulators, like the Responsive Web Design Testing Tool from Matt Kersley ([http://bkaprt.com/gr/05-23/](http://bkaprt.com/gr/05-23/)) or Breakpoint Tester from Macula Internet ([http://bkaprt.com/gr/05-24/](http://bkaprt.com/gr/05-24/)) that show how a site will appear at different breakpoints—though this should not replace looking at the site on actual devices.

Put new mechanisms in place to gather feedback on prototypes. How will teams capture notes from stakeholders and track which device, browser, and breakpoint the feedback references? Soliciting feedback on content choreography at different breakpoints will make gathering and evaluating feedback more complex. Prototyping apps like InVision are designed to simplify the feedback process by giving stakeholders an easy way to share comments. Jason Grigsby from Cloud Four said they use a tool called LICEcap to generate animated GIFs, which they use to solicit feedback from stakeholders ([http://bkaprt.com/gr/05-25/](http://bkaprt.com/gr/05-25/)). If you don’t want to use a proprietary solution, you’ll need to decide how you want to track and manage feedback at different breakpoints.

### Devices, not projectors

During team collaboration and review sessions, seeing the site in context on a device is much more powerful than seeing it projected on a screen. Having a few different devices available in meetings is a great idea, especially if stakeholders don’t have ongoing access to a prototype. Brian Greene from Nationwide described their device-specific review process:

> Having the latest devices, the iPad mini with Retina display—so that they could really see what it would look like—got a lot of excitement with our business partners. Bringing in devices to show off the progress on the site was instrumental in getting their buy-in. Everything is so much more crisp and responds so well, it looks like the site was meant for that device. We did our best to not ever project. There were some scenarios where we had to project, but those projections are horrible, you can’t see all the colors, and it doesn’t really do it justice ([http://bkaprt.com/gr/04-05/](http://bkaprt.com/gr/04-05/)).

Showing the site on devices is also a great way to encourage stakeholders to consider how the content will be presented, navigated, and read.

### Legal review

Legal and compliance review either isn’t a problem for you at all or it’s your biggest problem. In heavily regulated industries like financial services and pharmaceuticals, going through legal and compliance reviews is always challenging, but never more so than when reviewing responsive designs. Rules for placement of footnotes, disclosures, and other bits of legalese are governed by requirements for print—which can be frustrating, if not comical, on smaller form factors. Legal and compliance processes traditionally require PDFs of desktop screens for review and comment; this won’t be sufficient when the information shifts around in a responsive design.

Many design teams have worked hard to build collaborative relationships with friendly lawyers to streamline this process. See if you can find a “yes” lawyer who can help translate your design requirements to legalese and find creative solutions for this new environment—remember, lawyers use phones too. Legal and regulatory requirements will eventually change to take device types and screen sizes into account. Brian Hurley, SVP, Fidelity.com Platform Experience, reported that they’re working with the regulatory agency to address this situation:

> We’re literally helping the regulatory body rewrite their rules around disclosure, meaning how much needs to be shown and how disclosures are rendered in context versus in footnotes. This one regulatory body in particular has recognized that there’s enough movement in the industry that they need to change their standards. Our legal team has been incredible in stepping up and helping lead that charge ([http://bkaprt.com/gr/01-16/)](http://bkaprt.com/gr/01-16/\)).

Responsive design changes the way people work. Teams benefit from a more collaborative process, which encourages different perspectives and puts the focus on building an actual functioning website. Many teams find this new collaborative approach saves time and makes the process go more smoothly.

So what are you going to do with the extra time you saved? I have some bad news: you’re going to spend it all QA testing the website.
