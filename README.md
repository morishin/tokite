# Tokite [![CircleCI](https://circleci.com/gh/hogelog/tokite.svg?style=svg)](https://circleci.com/gh/hogelog/tokite) [![Gem Version](https://badge.fury.io/rb/tokite.svg)](https://badge.fury.io/rb/tokite)

Tokite send GitHub event (pull-request, issue and comment) to Slack.
 
Notification setting are personalized and customizable by query.

## Installation
Tokite works as rails mountable engine.

Add this line to your rails application's Gemfile:
```ruby
gem "tokite"
```

And mount engine.

```ruby
Rails.application.routes.draw do
  mount Tokite::Engine => "/"
end
```

### Setup database
```console
$ ./bin/rails db:create
$ ./bin/rails tokite:ridgepole:install
$ ./bin/rails tokite:ridgepole:apply
```

### Setup yarn pkg
```console
$ ./bin/rails tokite:yarn:install
```

## Configuration
<table>
<tr><th>GITHUB_CLIENT_ID</th><td>Google+ OAuth2 client ID</td></tr>
<tr><th>GITHUB_CLIENT_SECRET</th><td>Google+ OAuth2 client secret</td></tr>
<tr><th>GITHUB_HOST (optional)</th><td>GitHub Enterprise host</td></tr>
<tr><th>SECRET_KEY_BASE</th><td><code>rails secret</code> key</td></tr>
<tr><th>SLACK_WEBHOOK_URL</th><td>Slack incoming webhook url</td></tr>
<tr><th>SLACK_NAME (optional)</th><td>Slack notification user name</td></tr>
<tr><th>SLACK_ICON_EMOJI (optional)</th><td>Slack notification icon</td></tr>
<tr><th>APP_HOST (optional)</th><td>Application host url</td></tr>
</table>
