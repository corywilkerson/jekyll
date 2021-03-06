---
layout: docs
title: Permalinks
prev_section: templates
next_section: pagination
---

Jekyll supports a flexible way to build your site’s URLs. You can specify the
permalinks for your site through the [Configuration](../configuration) or in the
[YAML Front Matter](../frontmatter) for each post. You’re free to choose one of
the built-in styles to create your links or craft your own. The default style is
`date`.

Permalinks are constructed by creating a template URL where dynamic elements are
represented by colon-prefixed keywords. For example, the default `date`
permalink is defined as `/:categories/:year/:month/:day/:title.html`.

## Template variables

<div class="mobile-side-scroller">
<table>
  <thead>
    <tr>
      <th>Variable</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <p><code>year</code></p>
      </td>
      <td>
        <p>Year from the Post’s filename</p>
      </td>
    </tr>
    <tr>
      <td>
        <p><code>month</code></p>
      </td>
      <td>
        <p>Month from the Post’s filename</p>
      </td>
    </tr>
    <tr>
      <td>
        <p><code>i_month</code></p>
      </td>
      <td>
        <p>Month from the Post’s filename without leading zeros.</p>
      </td>
    </tr>
    <tr>
      <td>
        <p><code>day</code></p>
      </td>
      <td>
        <p>Day from the Post’s filename</p>
      </td>
    </tr>
    <tr>
      <td>
        <p><code>i_day</code></p>
      </td>
      <td>
        <p>Day from the Post’s filename without leading zeros.</p>
      </td>
    </tr>
    <tr>
      <td>
        <p><code>title</code></p>
      </td>
      <td>
        <p>Title from the Post’s filename</p>
      </td>
    </tr>
    <tr>
      <td>
        <p><code>categories</code></p>
      </td>
      <td>
        <p>
          The specified categories for this Post. Jekyll automatically parses
          out double slashes in the URLs, so if no categories are present, it
          will ignore this.
        </p>
      </td>
    </tr>
  </tbody>
</table>
</div>

## Built-in permalink styles

<div class="mobile-side-scroller">
<table>
  <thead>
    <tr>
      <th>Permalink Style</th>
      <th>URL Template</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <p><code>date</code></p>
      </td>
      <td>
        <p><code>/:categories/:year/:month/:day/:title.html</code></p>
      </td>
    </tr>
    <tr>
      <td>
        <p><code>pretty</code></p>
      </td>
      <td>
        <p><code>/:categories/:year/:month/:day/:title/</code></p>
      </td>
    </tr>
    <tr>
      <td>
        <p><code>none</code></p>
      </td>
      <td>
        <p><code>/:categories/:title.html</code></p>
      </td>
    </tr>
  </tbody>
</table>
</div>

## Permalink style examples

Given a post named: `/2009-04-29-slap-chop.textile`

<div class="mobile-side-scroller">
<table>
  <thead>
    <tr>
      <th>Permalink Setting</th>
      <th>Resulting Permalink URL</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <p>None specified, or <code>permalink: date</code></p>
      </td>
      <td>
        <p><code>/2009/04/29/slap-chop.html</code></p>
      </td>
    </tr>
    <tr>
      <td>
        <p><code>permalink: pretty</code></p>
      </td>
      <td>
        <p><code>/2009/04/29/slap-chop/index.html</code></p>
      </td>
    </tr>
    <tr>
      <td>
        <p><code>permalink: /:month-:day-:year/:title.html</code></p>
      </td>
      <td>
        <p><code>/04-29-2009/slap-chop.html</code></p>
      </td>
    </tr>
    <tr>
      <td>
        <p><code>permalink: /blog/:year/:month/:day/:title</code></p>
      </td>
      <td>
        <p><code>/blog/2009/04/29/slap-chop/index.html</code></p>
      </td>
    </tr>
  </tbody>
</table>
</div>
