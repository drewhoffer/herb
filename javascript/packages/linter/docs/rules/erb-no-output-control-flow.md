# Linter Rule: Disallow output ERB tags with control flow

### Rule: `erb-no-output-control-flow`
##### Description
Disallow using output ERB tags (`<%=`) for control flow statements like `if`, `unless`, `case`, `while`, etc. Control flow should be written with regular ERB tags (`<% ... %>`), since these do not produce output directly.

##### Rationale
Using `<%=` with control flow is typically a mistake or misunderstanding of ERB behavior. Output tags (`<%=`) are designed to render values into the HTML output, while control flow statements only affect execution and do not produce a value to render. This misuse can result in unexpected output, unnecessary blank spaces, or subtle bugs.

Reporting this as a warning can help developers catch likely mistakes while allowing flexibility for rare advanced cases.

#### Examples
###### ✅ Good
<% if condition %>
  Content here
<% end %>

<%= user.name %>
###### 🚫 Bad
<%= if condition %>
  Content here
<% end %>

<%= unless user.nil? %>
  Welcome!
<% end %>
#### References
* [Inspiration](https://x.com/specialcasedev/status/1935013470069719231)
### Rule: `erb-no-output-control-flow`
##### Description
Disallow using output ERB tags (`<%=`) for control flow statements like `if`, `unless`, `case`, `while`, etc. Control flow should be written with regular ERB tags (`<% ... %>`), since these do not produce output directly.

##### Rationale
Using `<%=` with control flow is typically a mistake or misunderstanding of ERB behavior. Output tags (`<%=`) are designed to render values into the HTML output, while control flow statements only affect execution and do not produce a value to render. This misuse can result in unexpected output, unnecessary blank spaces, or subtle bugs.

Reporting this as a warning can help developers catch likely mistakes while allowing flexibility for rare advanced cases.

#### Examples
###### ✅ Good
<% if condition %>
  Content here
<% end %>

<%= user.name %>
###### 🚫 Bad
<%= if condition %>
  Content here
<% end %>

<%= unless user.nil? %>
  Welcome!
<% end %>
#### References
* [Inspiration](https://x.com/specialcasedev/status/1935013470069719231)