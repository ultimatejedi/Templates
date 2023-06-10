<html>
<body>

<H1>Plex Updater</H1>

I originally borrowed this concept from Doug Lock
https://www.douglocks.blog/posts/20220823_updating-synology-plex-with-ansible/

His tool was specific for a Synology DSM NAS.  I took it and converted it to be applicable to CentOS and RPM files.

It will do the following:
<ul>
	<li>Retrieves a JSON payload from Plex host at <a href='https://plex.tv/api/downloads/5.json'>https://plex.tv/api/downloads/5.json</a></li>
	<li>Parses out the latest version number published.</li>
	<li>Queries the version currently installed</li>
	<li>Displays a couple of debug messages</li>
	<li>Loops through the available downloads and pulls the latest version IF it matches the system architecture AND is newer than the currently installed version.</li>
	<li>Stops the Plex service.</li>
	<li>Installs the RPM package.</li>
	<li>Starts the Plex service.</li>
	<li>Triggers webhook (I utilize this to notify me through HomeAssistant that an update was completed.</li>
	<li>If the install fails, restarts the Plex service.</li>
	<li>Triggers webhook if install files to notify me.</li>
	<li>Cleans up temporary files.</li>
</ul>
</body>
</html>