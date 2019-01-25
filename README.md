# slack-sandbox

If like me you think Slack is a car crash of an application you may wish to run
it in a sandbox.

## Instructions

1) Copy slack.sb to ~/Documents/ and change all instances of "/Users/admin" in
it to your own home directory.

2) Create an apple script with the following command replacing the paths as
appropriate:

````
do shell script "/usr/bin/sandbox-exec -f /Users/admin/Documents/slack.sb 
  /Applications/Slack.app/Contents/MacOS/Slack &>/dev/null&"
````

3) Export the appple script to an applicaton bundle named similar to the real
application but with an additional space at the end, eg:

````
/Applications/Slack .app
````

4) Open System Preferences -> Spotlight -> Privacy and drag the real Slack.app
from Applications into the private list.

Now when you use Spotlight to launch Slack it will appear to be launching
Slack but it's really launching the launcher instead and will never launch the
real Slack directly because it's excluded from Spotlight.
