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

3) Export the appple script to an applicaton bundle at something like
/Applications/Slack Launcher.app

4) Set your launcher to prefer the Slack Launcher rather than the real Slack
app. If you use Spotlight this can be achieved by typing the first few
characters of "slack" and then selecting the launcher for the result rather than
Slack.app. If you do this for "sl", "sla", "slac" and "slack" you should never
accidentally run Slack directly.
