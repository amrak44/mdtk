MeshCommander
-------------

The goal of this package is to develop an Intel AMT application using web based technologies. There are many advantages to do this like using the the same code accross platforms and for web management on the intranet and over the cloud. This package contains the code to "Manageability Commander Web Edition" for IIS and NW.js along with a few samples in the "samples" folder for interacting with Intel AMT.


Samples
-------
This is a set of sample Javascript pages that are built to run on NodeWebkit. You will need NW.js (http://nwjs.io/) to run these samples. They can also be made to run within a web server. For details, look at the readme.txt file in the samples folder.


MeshCommander - IIS Hosting
------------------------------------
To run Mesh Commander in IIS8, create a new web site or use the existing default "wwwroot" folder and put the content of the "MeshCommander/IIS-WebSite" into the site's path. You must have IIS8 with .NET 4.5 installed to make it work and "WebSockets" must be installed as an IIS feature. This site uses a WebSocket-to-TCP router (webrelay.ashx) to relay the Intel AMT traffic from the browser to the target machine.


MeshCommander - NodeJS Hosting
------------------------------------
You can host Mesh Commander using NodeJS, this work on Linux. Just run "commander.js" in the "MeshCommander/NodeWebkit" folder.


MeshCommander - NW.js (NodeWebkit)
------------------------------------
To make Mesh Commander run as a stand-alond tool, you will need NW.js (http://nwjs.io/). It's basically a browser frame that allows web applications to run natively. Once you get NW.js installed, open "commander.htm". Mesh Commander will accept the following command line arguments:

	-kvmviewonly		Remote desktop will not allow mouse & keyboard input.
	-host:[hostname]	Directly connect to a target host. If user/pass arguments are not provided, Kerberos will be used.
				The following arguments are only valid if -host is specified

		-user:[username]	Username to use to connect to Intel AMT is digest mode.
		-pass:[password]	Password to use to connect to Intel AMT in digest mode.
		-tls			Connect with TLS security enabled (Currently, Intel AMT certificate is ignored)
		-kvm			Go directly into remote desktop mode and connect to hardware KVM.
		-kvmfull		Go directly into full screen remote desktop and connect to hardware KVM.
		-kvmonly		Go directly into full screen remote desktop, don't do any extra WSMAN calls.
		-sol			Go directly into terminal and connect to Serial-over-LAN. 
		-script:[file]		Run a script targeting [hostname].
		-autoexit		Run a script and exit when done.
		-ignoretls		Causes TLS certificate check to be skipped.

	-list:[listfile]	Loads a list of computers into Mesh Commander. The format of the file is JSON like this.
				For Kerberos, set the user to "*" and password to empty. "name" is optional.

		{
		  "computers": [
		    { "name": "FriendlyName", "host": "hostname", "user": "admin", "pass": "password1", "tls": 0 },
		    { "host": "hostname1", "user": "admin", "pass": "password2", "tls": 1 },
		    { "host": "hostname1", "user": "*", "pass": "", "tls": 1 }
		  ]
		}

		Along with -list:[listfile], you can also use:

		-script:[file]		Run a script targeting all of the computers in [listfile].
		-autoexit		Run a script and exit when done.
		-ignoretls		Causes TLS certificate check to be skipped.

	-debug			Starts MeshCommander with the debug console window visible.
	-wsmantrace		Display all WSMAN traffic in the debug console.
	-norefresh		MeshCommander will not periodically poll for updates.
	-redirtrace		Display all redirection data channel data to the debug console window.
	-kvmdatatrace		Display KVM data channel data in the debug console window.
	-kvmonly		MeshCommander will only get minimal data from Intel AMT in order to only support KVM.
	-logfile:log.txt	Log everything from the debug console windows into a text file.
	-noredirdisconnect	Don't auto-disconnect redirection session with performing certain power commands.


License
-------

MeshCommander is released under the Apache 2.0 open source license. You can see it here: https://www.apache.org/licenses/LICENSE-2.0
