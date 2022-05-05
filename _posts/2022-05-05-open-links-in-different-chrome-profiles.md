---
title: How to open links in different Chrome profiles in OSX
excerpt: Finicky to the rescue!
last_modified_at: 2022-05-05
categories:
  - Productivity
tags:
  - Productivity
---
Are you annoyed by work stuff openning in your personal Chrome? Follow
these steps and see how your productivity skyrockets 🚀

- Install [Finicky](https://github.com/johnste/finicky): `brew install --cask finicky`.
-  Create a new `Finicky` config.
{:refdef: style="text-align: center;"}
![Config](/assets/images/finicky/create-config.png)
{: refdef}
-  In Chrome, visit `chrome://version` and find your the name of the profile you want to use.
{:refdef: style="text-align: center;"}
![Config](/assets/images/finicky/chrome-profile.png)
{: refdef}
-  Edit the new config `~/.finicky.js` and use something similar to:
{% highlight javascript linenos %}
const personal = {
  name: "Google Chrome",
  profile: "Profile 3",
};

const work = {
  name: "Google Chrome",
  profile: "Profile 2",
};

const slackApp = "/Applications/Slack.app";

module.exports = {
  defaultBrowser: "Google Chrome",
  options: {
      hideIcon: false,
      checkForUpdate: true,
  },
  handlers: [
      // Links opened from Slack
      {
          match: ({
              opener
          }) => ["Slack"].includes(opener.name),
          browser: work,
      },
      // Matches links containing the name of my company
      {
          match: /myCompany/,
          browser: work,
      },
      // Social media
      {
          match: /facebook|twitter|instagram/,
          browser: personal,
      },
      // Slack deeplinks
      {
          match: ({
              url
          }) => url.protocol === "slack",
          browser: slackApp,
      },
      // Open Slack links in the app
      {
          match: /slack.com/,
          browser: slackApp,
      },
  ],
};

{% endhighlight %}

-  Reload `Finicky` config.

{:refdef: style="text-align: center;"}
![Reload](/assets/images/finicky/reload-config.png)
{: refdef}
I hope this tip improves your productivity as much as it improved mine!