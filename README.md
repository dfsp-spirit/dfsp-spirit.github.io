# dfsp-spirit.github.io

My personal website, generated with Jekyll.

This is my new website. The website is build with [Jekyll](https://jekyllrb.com/), a static site generator written in Ruby.

## How the repo contents gets turned into the website

The *current state of this repository* is always visible at [dfsp-spirit.github.io](https://dfsp-spirit.github.io/), but my real website at [ts.rcmd.org](https://ts.rcmd.org/) is **not** necessarily identical to that version. The version you see in this repo (and thus at `dfsp-spirit.github.io`) may be work in progress (WIP), that only gets released to `ts.rcmd.org` once it is ready. 

Once more, to make it clear: I only use a GitHub repo to store the raw data from which the site gets generated, and GitHub Pages (ghpages) to preview the WIP version. I decided against hosting the real website on ghpages, instead I build the site locally, and then upload the result to my own server. This means I also do not use ghpages-specific gems in my Gemfile. If one would like to deploy the website to ghpages, one should change this to get access to the Jekyll plugins/themes available on GitHub (see GitHub's official documentation on ghpages, and the commented out parts in the Gemfile).

## Pros and Cons

The advantage of this Jekyll-based website over my old, homebrew HTML/CSS solution is that it is more mobile friendly and looks a bit more professional (usage of whitespace, font size scaling). The disadvantage is a more complicated setup that requires Ruby at generation time (not at runtime on the server, of course, it is just static HTML then). 

Overall, I decided that the pros of outweight the cons for now. (And I was also just sick of the old website.)

*Note 1*: At generation time means *every time you want to make changes to the website* in my case though, because I am not hosting on ghpages. If one used ghpages, one would only need Ruby once, to initialze the repo. From then on, one could just edit the contents on GitHub, commit, and be done (as Github automatically re-deploys when the repo content changes). One can even do that in the web interface of GitHub without a local repo. Still, I decided to host this on my own server after trying the ghpages solution. The main reason was that the DNS and SSL configuration is way simpler that way, which is more important to me than a simpler site generation process.


## First time installation

I installed [Ruby](https://www.ruby-lang.org/en/) and [bundler](https://bundler.io/) first. This can be quite a pain, depending on which version of Ruby your distribution ships with. I would highly recommend to ignore that version entirely and use [rbenv](https://github.com/rbenv/rbenv) to install your own Ruby version. I tried with the Ruby version that can with Ubuntu 20.04 and encountered one error after another when trying to install the latest jekyll version and its dependencies, until I gave up. Do yourself a favor and use `rbenv` from the start, even if it is also a bit annoying to setup. If you use bash and Ubuntu 22.04, what you have to do is:

```shell
git clone https://github.com/rbenv/rbenv.git ~/.rbenv
echo 'eval "$(~/.rbenv/bin/rbenv init - bash)"' >> ~/.bashrc
bash    # to start a new bash with rbenv in the PATH.
git clone https://github.com/rbenv/ruby-build.git "$(rbenv root)"/plugins/ruby-build  # Installs a plugin for the 'rbenv install' command.
rbenv install -l   # lists latest stable Ruby versions. Pick one, then install it:
rbenv install 3.1.4  # install a version
rbenv global 3.1.4   # set installed version as default (global means in all directories, local would create an env in current folder only)
```

Note: On my laptop at work, the `rbenv install` command above failed on my work machine because `libssl-dev` and `zlib1g-dev` were not available. Since I do not have root access, I had to ask the IT department to install them via `apt.` Ruby installation seems quite a pain, and I am already considering to move away from Jekyll because of it. I have no time to look for alternatives at this time, though. If you have root, this will help:

```shell
sudo apt install libssl-dev zlib1g-dev
```

Once you have Ruby installed, installation of [bundler](https://bundler.io/) is possible via `gem`, which comes with Ruby (though for some reason no installation instructions could be found on their website at the time of writing, they seem to assume you are a Ruby programmer and aware of `gem`): `gem install bundler`.

Then, in the repo, make bundler install all the dependencies:

```shell
cd <local_repo_copy>/
bundle  # This will install jekyll and everything in the Gemfile.
```

## Updating / Building the website

This is what you need to do after each change to the contents. It assumes that you have already done the First Time Installation explained above (Ruby install, Bundler install, run bundler on Gemfile to install Jekyll etc.).

Run jekyll to generate the website from the templates:

```shell
cd <local_repo_copy>/
bundle exec jekyll build
```

Now you can upload the generated website in the `_site` directory to your webhost, e.g., via FTP.
