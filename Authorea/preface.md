# Preface

I am fortunate to have a radio engineer for a father. His radio stations' networks and IT infrastructure (everything from Novell servers and old Mac and Windows workstations in the 90s, to Microsoft and Linux-based servers and everything in-between) were maintained by the engineering staff, and my Dad showed me how it all worked. Even better, he brought home old decommissioned servers and copies of Linux he had burned to CD for me!

I was able to start working with Linux and small-scale infrastructures before I started high school (even building a Cat5 wired network and small rack of networking equipment for a local grade school!), and my passion for managing infrastructure grew. When I started developing full-time, what was once a hobby became a necessary part of my job, so I invested more time in managing infrastructure efficiently. Over the past ten years, I've gone from manually booting and configuring physical and virtual servers, to using relatively complex shell scripts to provision and configure servers, to using configuration management tools to manage many cloud-based servers.

When I began converting my infrastructure to code, some of the best tools for testing, provisioning, and managing my servers were still in their infancy, but they have since matured into fully-featured, robust tools I use every day. Vagrant is an excellent tool for managing local virtual machines to mimic real-world infrastructure locally (or in the cloud), and Ansible (the subject of this book) is an excellent tool for provisioning servers, managing their configuration, and deploying applications---even on my local workstation!

These tools are still improving rapidly, and I'm excited for what the future holds. New tools (like Docker) that are nearing production-ready status also excite me, and I know the time I invest in learning to use these tools well will be helpful for years to come (Ansible, Docker, and Vagrant seems a potent combination for both local and production infrastructure... but that's a little outside of *this* book's scope).

In the following pages, I will share with you all I've learned about Ansible---my favorite tool for server provisioning, configuration management, and application deployment. I hope you enjoy reading this book as much as I did writing it!

-- Jeff Geerling, 2014

## Who is this book for?

Many of the developers and sysadmins I work with are at least moderately comfortable administering a Linux server via SSH, and manage between one and one hundred servers.

Some of these people have a little experience with configuration management tools (usually with Puppet or Chef), and maybe a little experience with deployments and continuous integration using tools like Jenkins, Capistrano, or Fabric. I am writing this book for these friends (who, I think, are representative of most people who have heard of and/or are beginning to use Ansible).

If you are interested in both development and operations, and have at least a passing familiarity with managing a server via command line, you should end up with an intermediate to expert-level understanding of Ansible and how you can use it to manage your infrastructure after reading this book.

## Typographic conventions

Ansible uses a simple syntax (YAML) and simple command-line tools (using common POSIX conventions) for all it's powerful abilities. Code samples and commands will be highlighted throughout the book either inline (for example: `ansible [command]`), or in a code block (with or without line numbers) like:

{lang="yaml"}
    ---
    # This is the beginning of a YAML file.

Links to pertinent resources and websites are added inline, like the following link to [Ansible](http://www.ansible.com/), and can be viewed directly by clicking on them in eBook formats, or by following the URL in the footnotes.

Sometimes, asides are added to highlight further information about a specific topic:

I> Informational asides will provide extra information.

W> Warning asides will warn about common pitfalls and how they can be avoided.

T> Tip asides will give tips for deepening your understanding or optimizing your use of Ansible.

When displaying commands run in a terminal session, if the commands are run under your normal/non-root user account, the commands will be prefixed by the dollar sign (`$`). If the commands are run as the root user, they will be prefixed with the pound sign (`#`).

## Please help improve this book!

This book is a work in progress, and is being expanded and updated on LeanPub at a rather rapid clip. If you think a particular section needs improvement, or find something missing, please contact me via Twitter ([@geerlingguy](https://twitter.com/geerlingguy)), [Google+](https://plus.google.com/+JeffGeerling), a comment on [this book's Feedback page on LeanPub](https://leanpub.com/ansible-for-devops/feedback), or whatever method is convenient for you.

Please note that, since the book is still being written and proofread, the book contains certain imperfections and oddities. I've tried to ensure every line of code, at least, works perfectly, but I may have an occasional typo---you've been warned!

## About the Author

[Jeff Geerling](http://jeffgeerling.com/) is a developer who has worked in programming and devops for companies with anywhere between one to thousands of servers. He also manages many virtual servers for services offered by [Midwestern Mac, LLC](http://www.midwesternmac.com/), and has been using Ansible to manage infrastructure since early 2013.