# Heroku buildpack: fping

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks)
for adding [fping](http://fping.org/) to your dyno environment.

## Multipacks

Using [multipack](https://github.com/ddollar/heroku-buildpack-multi) you are able to utilize more than one buildpack in your dyno environment.

Enable multipack:

    $ heroku config:add BUILDPACK_URL=git://github.com/ddollar/heroku-buildpack-multi.git

Then create `.buildpacks` in the root of your application containing the following:

    git://github.com/heroku/heroku-buildpack-ruby.git
    git://github.com/meskyanichi/heroku-buildpack-fping.git

The next time you deploy your application this will ensure you're using both the Ruby and `fping` buildpacks.
