# dfsp-spirit.github.io
My personal website, generated with Jekyll.

This is my new website. The website is build with Jekyll, a static site generator written in Ruby. The current state from this repository is always visible at [dfsp-spirit.github.io](https://dfsp-spirit.github.io/). This is now also served from [ts.rcmd.org](https://ts.rcmd.org/) via a DNS CNAME record.

The advantage of this website over my old, homebrew HTML solution is that it is more mobile friendly and looks a bit more professional. The disadvantage is a more complicated setup, and that it requires Ruby at generation time (not at runtime).

I decided that this pros outweight the cons, especially since GitHub takes away the major part of the Ruby pain though: you only need to get it to work once for the initial repo setup unless you want to preview locally before committing.

## First time installation

I installed [Ruby](https://www.ruby-lang.org/en/) and [bundler](https://bundler.io/) first. This can be quite a pain, depending on which version of Ruby your distribution ships with. I would highly recommend to ignore that version entirely and use [rbenv](https://github.com/rbenv/rbenv) to install your own Ruby version. I tried with the Ruby version that can with Ubuntu 22.04 and encountered one error after another when trying to install jekyll, until I gave up. Do yourself a favor and use `rbenv` from the start. Once you have Ruby installed, installation of [bundler](https://bundler.io/) is easy (though for some reason no installation instructions could be found on their website at the time of writing): `gem install bundler`.

Then, in the repo, make bundler install all the dependencies:

```shell
cd repo/
bundle  # that Note it's bundle, not bundler. This will install jekyll and everything in the Gemfile.
```

## Building the website


Run jekyll to generate the website from the templates:

```shell
bundle exec jekyll build
```

Now you can copy the generated website in the `_site` directory to your webhost. It does not need Ruby, of course.
