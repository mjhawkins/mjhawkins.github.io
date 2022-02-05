---
layout: page
title: "Installing your XML Editor"
date: '2020-06-11 06:52:00 -0000'
permalink: /foundational-skills-and-knowledge/installing-your-xml-editor
published: true
category: 'Foundational skills and knowledge'
tags: 'Hello World'
---
*This is the second post in a series on the “[‘Hello, World’ for TEI Editors](/foundational-skills-and-knowledge/a-tei-xml-editors-hello-world-exercise)”.*

This post will show you how to install and configure your XML editor. This is the primary tool you’ll use when editing your TEI transcriptions.

## Why do I need an XML Editor?

If you’ve been doing a little reading, you might be wondering why you need a specialised XML editor. You’ve likely read somewhere that you can edit an XML file with any plain-text editor. Your computer likely even has one installed already. Macs come with TextEdit and Windows come with Notepad. So, why have I written an entire post teaching you how to install and configure an XML Editor? The answer is simple: although you can edit XML in a simple plain-text editor, it isn’t a viable long-term approach.[^1]

XML (Extensible Markup Language) is not a file format. It’s a standard for creating markup languages to describe data. It has a rigid syntax (structure) that all XML documents must adhere to. A document that conforms to these rules is said to be ‘well-formed.’ The XML standard, however, doesn’t define what the actual elements or attributes are or how they should be used. This is done by the schema. The full Text Encoding Initiative schema defines over 600 elements and 500 attributes and stipulates precisely where and when they can be used. When a XML document follows the rules laid out in its schema, it is said to be ‘valid.’

It is difficult to ensure that an XML document is well-formed and valid with a simple plain-text editor. It doesn’t know or care about about either of these things.[^2] It’ll let you create files that badly formed and filled with misspelt and misplaced elements. No matter how conscientious you are, you *will* make serious mistakes transcribing your document. A simple plain-text editor won’t help you find them or even let you know that they exist. The longer your transcription becomes, the harder it will be to spot errors.[^3]

You don’t have these problems with XML Editors. They understand both the general structure of XML and your schema. They will complain if your document is badly formed or doesn’t validate.

XML Editors also make it easier to write code. They know what elements and attributes are available to you at any given point in your document and will suggest them to you as you type. When working on a TEI file, for example, an XML Editor will suggest one set of elements when you are encoding metadata in the header and another when you are in the middle of a paragraph of text.

## Which XML Editor should I use?

Two of the more commonly used XML Editors within the TEI community are the [Atom Text Editor](https://atom.io/) and the [oXygen XML Editor](https://www.oxygenxml.com/xml_editor.html). Both are excellent options. They have the essential XML-editing tools and will run on all the major platforms (i.e. Macintosh, Windows and Linux).

Their chief differences are their cost and how much work you have to do to set them up for XML coding. Atom is free, but you have to manually install and configure some extras to support editing TEI XML files. oXygen is a commercial product that has everything you need, including TEI support, baked right in. SyncRO Soft offers a 30-day [Trial license](https://www.oxygenxml.com/xml_editor/register.html?p=editor) so you can try it out for free. If you like it (and are eligible), they sell a discounted [academic license](https://www.oxygenxml.com/academic/).[^4].

Below, please find instructions for:

- [Installing Atom](#install-atom)
- [Installing oXygen XML Editor](#install-oxygen)
- [Changing a few settings](#setting-changes).

- - - - - -

## Install Atom Text Editor

- Install the latest [Java JDK](https://www.oracle.com/java/technologies/javase-downloads.html).[^5] Once you click on the ‘JDK Download’ link, it will take you to a new page with a dozen or so different choices. Download the installer for your computer.

If you are using a Macintosh, run the installer. Once it’s finished, you can move onto the next step and [download and install Atom](#download-atom).

If you are using Windows, you will need to do a bit more.

- Run the JDK installer and make a note of the Destination folder. It will likely be similar to ‘C:\\Program Files\\Java\\jdk-14.0.1\\.’ Don’t worry if it’s different. Just make a note of it.
- Once the installation is finished, you need to edit some system environment variables. In the Windows 10 search field, type ‘environment’, select ‘Edit the system environment variables’ and click on **Open** to add some system environment variables.
- First, you need to add the Java Development Kit’s bin folder to your Path variable.
  - Click on **Environment Variables** in the System Properties window. The top portion of this window will show ‘User variables for windows’, select ‘Path’ and click **Edit**.
  
  
  - In the window that opens, make note of the number of existing paths defined. On my machine, there was only one, but your system might be different.
  - Click **New** to create a slot for an additional path. This will help to ensure that you don’t erase any of the existing paths.
  - You now need to add the bin folder from the Java Development Kit. Click **Browse** and select **This PC** and navigate to the JDK path that you noted earlier. Once there, select the ‘bin’ folder and click **OK**.
  
  
  - You’ll then be back at the previous page. If all went well, the original lines that you noted are still there along with a new one you just added. If you are confident that everything seems fine, click **OK**. Otherwise, click **Cancel** and try the above instructions again.
- Second, you need to add a JAVA\_HOME variable containing the Java Development Kit’s destination folder into ‘System variables’
  - Go to the ‘System variables’ list in the lower portion of the System Properties window and check if an entry for ‘JAVA\_HOME’ exists. If it does, you’re done and you can [download and install Atom Text Editor](#download-atom).
  - If there **isn’t** an entry for ‘JAVA\_HOME’, click on **New**. In the dialogue box that opens, type in ‘JAVA\_HOME’ for the Variable name. Then, click on **Browse directory** and select **This PC**. Then, navigate to the JDK’s destination folder that you noted earlier (in my case it was **Local Disk (C:) > Programme Files > Java > jdk-14.0.1**. Click **OK** to enter the path. This will take you back the the ‘Environment Variables’ window. Click **OK** again to confirm all your changes to the User and System Variables. This will take you back to ‘System Properties’. Click **OK** to confirm all your changes.

- Restart your computer.

### And, finally, download, configure and install Atom

- [Download Atom](https://atom.io/) and install it as you would any other application. Run the installer (if Windows) or expand the zip file and drag Atom into the Applications folder (on Macs).[^6]
- Launch Atom.
  - On Windows, select Atom in the Window’s Start Menu
  - On Macs, you normally run applications by double-clicking on their icons. The first time you run Atom, however, it’s necessary to do something different. Go to the Applications folder and right click (press control and click) on the Atom icon and select open. Depending on your security settings, it might bring up a dialog box talking about possible malicious software. Don’t worry about it. This happens to many legitimate Mac programmes downloaded outside the App Store. Atom Text Editor is a reputable application from a reputable source, so you can safely click the open button. This will launch Atom. You only need to do this procedure the first time you run Atom. In the future you should be able to double click Atom’s icon to launch it.
- Install four packages to give Atom XML-editing capabilities. You can open the package installer by going to **Packages** in the main menu and selecting **Settings View > Install Packages/Themes**. Alternatively, if the ‘Welcome Guide’ is showing in Atom’s main window, you can click on **Install a Package** and then click on the **Open Installer** button. Once you are in the installer, you want to install the following packages:
		- linter-autocomplete-jing
		- atom-wrap-in-tag
		- double-tag
		- tei-framework

The procedure is fairly straightforward. Type the name of each of the packages listed below one by one into the search field and click install button when it appears. If Atom asks whether it can install any extra dependencies, please let it do so. Repeat this procedure on each package.

- Disable some packages that come pre-installed in Atom. Go to the **Packages** menu in the main menu and select **Settings View > Manage Packages** to list all installed packages. Type ‘github’ into the search field to filter the list down. You want to disable ‘github’ and ‘open-on-github’. Click on the **Disable** button for each of these packages.[^7]

Assuming that there were no errors, the installation process is now complete. All you have left to do is [change a few settings](#setting-changes).

- - - - - -

## Install oXygen XML Editor

1. To use oXygen, you need a valid paid or trial license. This will be is emailed to you after purchasing a license or requesting a [free trial](https://www.oxygenxml.com/xml_editor/register.html). Keep this email handy, you’ll need it in a moment.
2. [Download](https://www.oxygenxml.com/xml_editor/download_oxygenxml_editor.html) and install it as you would any other application. On Windows run the installer and follow its recommendations. On Macs, double click the downloaded file and drag the oXygen XML Editor folder into the Applications folder.
3. When you first start oXygen, it’ll ask you to enter your license key. Cut and paste it from the email into oXygen as per their instructions.

At this point, you have everything needed to work with TEI files. All you need to do is [change a few preferences](#setting-changes).

- - - - - -
## Change a Few Preferences

Both oXygen and Atom have a tonne of preferences. Until you are thoroughly familiar with the application, I’d suggest you resist the urge to make any changes. Some drastically alter how the application functions. That said, there are several preferences that need to be checked and, if necessary, changed.

First, open the preferences in whichever editor you are using.
	- In oXygen, go to the **Options > Preferences** menu.
	- In Atom:
		- On Mac, go to the **Atom > Preferences** menu.
		- On Windows, go to the **File > Settings** menu.

### Turn on Line wrap/Soft wrap

When Line wrap/Soft wrap is enabled, your editor automatically wraps your text so that it fits into the window. It doesn’t actually make any changes to your file or insert any paragraph returns. It simply makes the text fit. That means you can resize the window and have the text automatically rewrap to that new size. When this option is turned off, you need to scroll your left and right to read the longer lines. This is a pain when encoding or proofing a transcription.

- in oXygen, type ‘line wrap’ (without the quotes) into the search field in the top left of the preferences window. Then, go to **Editor > Edit Modes > Text** and ensure ‘Line Wrap’ is checked. Click **Apply**.
- In Atom, click on the **Editor** option in the preferences window and scroll down to ‘Soft Wrap’ and ensure that it is checked. Leave this pane open as you’ll next be changing another option in it shortly.

### Make the font bigger

You’re going to be staring at computer code a lot when working in TEI. A lot of people, myself included, find it easier to read computer code when it’s larger. Finding the right size for you will be a process of trial and error. Whenever I change the resolution of my screen or get a new computer, it usually takes me a few trips into the preferences to get it just right.

I recommend only changing the default font size and not the actual font itself. Reading code isn’t like reading a text and there are a lot of issues to consider. There are even more issues if you happen to be transcribing materials that need special characters or glyphs, such as those that occur in historical documents. In a later tutorial, I’ll talk about in greater detail. For now, however, leave the font as it is and only change its size.

- In oXygen, type ‘font’ (without the quotes) into the search field in the top left of the preferences window. Click on **Font** to open the Font pane. Then, click on the **Choose** button for the Editor font and change the font size. oXygen helpfully show a preview, so just keep tweaking it until it feels right. When done, click **Apply**.
- In Atom, click on the **Editor** option in the preferences window and scroll to **Font Size**. Type in your preferred font size into that field. I’d suggest entering a value between 16-18. Atom doesn’t show a preview of the font, so you might find yourself coming back to adjust it after you start editing.

### Hide invisible files in Atom

In **Settings**, click on **Packages** to list all your installed packages. Type **tree-view** into the **Filter by package name** field. This will reveal the tree-view plugin. Click on its **Settings** and ensure that **Hide ignored names** is checked.

### Make sure that Windows knows about Atom

If you are using Atom on Windows, you’ll need to change three settings so it works properly. Click on **System** in the Settings and ensure that the following are all checked:

- ‘Register as file handler’
- ‘Show in file context menus’
- ‘Show in folder context menus’

- - - - - -

You’re now done. If you haven’t done it already at the end of the configuration and installation process, please restart your XML editor. You’re now ready to learn how to [work safely by storing all your transcriptions in a Git repository](/foundational-skills-and-knowledge/work-safely-by-storing-all-your-transcriptions-in-a-git-repository).

[^1]: By ‘simple’, I mean that your plain-text editor has no special bells and whistles installed for working with XML files. A plain-text editor with these extras installed, like Atom (see below), is suitable for editing complex XML documents.

[^2]: Not unless you install some extras, like we do with Atom Text Editor (below).

[^3]: I learned this the hard way when I first started coding in 2002.

[^4]: I use oXygen XML Editor myself. I receive no compensation from SyncRO Soft SRL. My license was bought with project funds.

[^5]: If you have a really old computer, you might not be able to install latest version. Work your way down through the list, trying each one until you find one that works. The linter-autocomplete-jing package will work with Java 1.6 and higher.

[^6]: The Atom manual also provides detailed[ installation instructions](https://flight-manual.atom.io/getting-started/sections/installing-atom/).

[^7]: These plugins allow Atom to interact with Git repositories on a very basic level. However, they aren’t functional enough to act as your core Git client. Moreover, they require certain command line utilities are installed on your computer and Atom will complain every time it starts up if they are not.