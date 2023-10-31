Manageability Developer Tool Kit
--------------------------------

For updated and community support, go to:
  http://opentools.homeip.net

The Open Active Management Technology (AMT) Developer Tools Kit (DTK) is a free set of tools for
designers, developers and testers that are building and testing Intel(R) AMT applications.

To help developers build applications that make use of Intel AMT, Intel provides a Software Development Kit (SDK)
with source code and basic building blocks. In addition, Intel is now offering the Intel AMT Developer Tool Kit (DTK).
The DTK provides tools that help with the training and development process. The DTK is designed to compliment the
Intel AMT SDK by adding solid and easy to use reference and test tools.

Requirements and limitations

Note that Manageability Director Tool is early development code, many features don't work.

The sample console and agent tools are generally designed and tested to run on Intel AMT 2.0 or above, but can run on an Intel AMT 1.0 machine with some limitations. The tools also require Microsoft Windows running the Microsoft .NET 2.0 framework. Currently, only Intel AMT machines provisioned in “small business mode” are supported, with limited support for "enterprise mode". The user must have correctly provisioned the Intel AMT machines before using the DTK, and all necessary platform drivers must be installed. Since the DTK is only intended for development and testing, all stored passwords are kept in clear text in the computer’s registry. Currently, the DTK assumes that the user always provides the username and password of the Intel AMT administrator account.

Also note that the DTK is a set of tools, not a product. It is not supported by Intel support. Still, we appreciate your comments and feedback at: ylian.saint-hilaire@intel.com and on the community discussion forums.

Ylian Saint-Hilaire
Senior Software Engineer,
Intel Corporation.


----- Manageability DTK Translation -----

We are looking for people to translate the Manageability DTK to other languages. The Manageability DTK includes a simple tool to help translate to other languages. 

- Run Intel Resource Tranlator
- Open this file "Manageability DTK Translation Dictionary.doc"
- Select a language
- In View, "Filter Locations..." select a portion of the DTK to translate
	- Starting out with ManageabilityNetStatusTool is a good option.
- Save the file back in .DIC format and mail it to:

	ylian.saint-hilaire@intel.com

Please let me know if you need another language added to the list or there are bugs in the tool or need help. If you start translating, you can send me mail
to mail sure no-one else is working on the same language and modules. Also, if you are not an Intel employee, you must agree that your translation will be
posted publicaly with source code under the terms of the Manageability DTK license.



--- Rebranding Manageability Commander Tool -----

You can easily "rebrand" Manageability Commander Tool to make it look a different way. Just create a folder called "Branding" in the folder where Manageability Commander Tool
is located and create the following files:

AboutBox.png				(Size 500 x 357, displayed as background in the about box)
Branding.txt				(Changed the tools name, see below)
Console.ico				(New icon used on the top left of every dialog box)
Image-Battery.jpg			(Size 200 x 150, displayed in Commander's main form)
Image-Card.jpg				(Size 200 x 150, displayed in Commander's main form)
Image-CDROM.jpg				(Size 200 x 150, displayed in Commander's main form)
Image-Computers.jpg			(Size 200 x 150, displayed in Commander's main form)
Image-CPU.jpg				(Size 200 x 150, displayed in Commander's main form)
Image-Cube.jpg				(Size 200 x 150, displayed in Commander's main form)
Image-Flash.jpg				(Size 200 x 150, displayed in Commander's main form)
Image-Harddisk.jpg			(Size 200 x 150, displayed in Commander's main form)
Image-Lab.jpg				(Size 200 x 150, displayed in Commander's main form)
Image-Motherboard.jpg			(Size 200 x 150, displayed in Commander's main form)
Image-NetworkPlug.jpg			(Size 200 x 150, displayed in Commander's main form)
Image-RAM.jpg				(Size 200 x 150, displayed in Commander's main form)
Image-Slots.jpg				(Size 200 x 150, displayed in Commander's main form)
TopBanner.jpg				(Size 1080x60, displayed at the top of the tool)

The file branding.txt should contain something like this (Remove the "---" and no initial spaces on each line).

	---
	Compagny(R) Management Console
	Compagny(R) Management Console - v0.00 - Unautorised demonstration branding for sales demos only.
	About Compagny(R) Management Console...
	Compagny(R) Console
	Management Console
	---

All of these files are optional, but if present will override the default bitmaps and branding names.


----- Attributions -----

This product includes software developed by the OpenSSL Project for use in the OpenSSL Toolkit (http://www.openssl.org/).
Eric Young is the author of the parts of the OpenSSL library.
This product includes software written by Tim Hudson (tjh@cryptsoft.com)


-------------------------------------------------------------------
 * Other names and brands may be claimed as the property of others.
 * "Intel(R) AMT" is a registered trademark of Intel.