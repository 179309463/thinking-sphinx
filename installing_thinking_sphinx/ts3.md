---
layout: en
title:  Installing Thinking Sphinx
---

## Installing Thinking Sphinx (Rails 3.1 or Newer)

<div class="note">
  <p><strong>Note</strong>: Thinking Sphinx v3.x (as documented here) is written for Ruby 1.9. If you are using Ruby 1.8.7 (or equivalent), please use a v2 release - covered in <a href="/thinking-sphinx/installing_thinking_sphinx/ts2.html">the Rails 3.0 installation instructions</a>.</p>
</div>

<div class="note">
  <p><strong>Note</strong>: Thinking Sphinx v3 is a complete rewrite from previous versions, and there are many small and big changes. These are noted accordingly in this documentation.</p>
</div>

If you're using Rails 3.1, 3.2 or 4.0, then you should use the version 3 releases of Thinking Sphinx. If you're using MRI, you'll also need the mysql2 gem 0.3.13 or newer for connecting to Sphinx. If you're using JRuby, you'll need the jdbc-mysql gem (and Sphinx 2.1.2 or newer). Even if you're using **PostgreSQL**, you will _still_ need to have the mysql2 gem installed (along with the pg gem too, of course).

Install them like you would any other gem - either manually:

{% highlight sh %}
gem install thinking-sphinx -v "~> 3.1.0"
gem install mysql2 -v "~> 0.3.13"
# or, for JRuby:
gem install jdbc-mysql -v "~> 5.1.28"
{% endhighlight %}

Or by adding them to your Gemfile:

{% highlight ruby %}
gem 'mysql2',          '~> 0.3.13', :platform => :ruby
gem 'jdbc-mysql',      '~> 5.1.28',   :platform => :jruby
gem 'thinking-sphinx', '~> 3.1.0'
{% endhighlight %}

You can also refer directly to the git repository - but if you're doing this, specifying the version, branch and commit reference is recommended so when you next go to upgrade the gem, it's clear what you were using (and perhaps why).

{% highlight ruby %}
gem 'mysql2',          '~> 0.3.13', :platform => :ruby
gem 'jdbc-mysql',      '~> 5.1.28',   :platform => :jruby
gem 'thinking-sphinx', '~> 3.1.0',
  :git    => 'git://github.com/pat/thinking-sphinx.git',
  :branch => 'master',
  :ref    => '4491f44a2d'
{% endhighlight %}

At the time of writing this, Rails 4.0 is supported with anything from 3.0.2 or newer. Rails 4.1.0-beta is not yet supported though, due to complex changes in ActiveRecord join generation. It's certainly on the roadmap though!

[Return to [Installing Thinking Sphinx]](/thinking-sphinx/installing_thinking_sphinx.html)
