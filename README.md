### apostrophe
---
https://github.com/apostrophecms/apostrophe

https://apostrophecms.org/docs/tutorials/getting-started/setting-up-your-environment.html

```
brew install node
touch ~/.profile && open ~/.profile
export NODE_PATH="/usr/local/lib/node"
export PATH="/usr/local/share/npm/bin:$PATH"
echo $PATH
npm
curl -L https://npmjs.org/install.sh | sh
brew install git
brew install mongo
mongo
brew install imagemagick

npm install apostrophe-cli -g
apostrophe create-project test-project
cd test-project
npm install
node app.js apostrophe-users:add admin admin
node app.js
curl http://localhost:3000
curl http://localhost:3000/login

node app.js
node install -g nodemon
nodemon
node app.js
```

```
// lib/modules/apostrophe-pages/views/pages/home.html
{% extends "layout.html" %}
{% block title %}Home{% endblock %}
{% block main %}
  <div class="main-content">
    <h3>Hello world!
      {% if not data.user %}
        <a class="login-link" href="/login">Login</a>
      {% endif %}
    </h3>
    <p></p>
    {{ apos.area(data.page, 'body', {
      widgets: {
        'apostrophe-images': {
          size: 'full'
        },
        'apostrophe-rich-text': {
          toolbar: [ 'Styles', 'Bold', 'Italic', 'Link', 'Unlink' ],
          styles: [
            { name: 'Heading', element: 'h3' },
            { name: 'Subheading', element: 'h4' },
            { name: 'Paragraph', element: 'o' }
          ]
        }
      }} }}
  </div>
{% endlock %}

{% extends "layout.html" %}

{% block beforeMain %}
  {#
    ...text
  #}
{% endblock %}
{% block main %}
  {#
    ...text
  #}
{% endblock %}
{% block afterMain %}
  {#
    ...text
  #}
{% endblock %}

{% blcok beforeMain %}
  <div class="block hero">
    <div class="inner">
      <div class="hero-text">
        <h4>...text</h4>
      </div>
    </div>
  </div>
{% endblock %}
```

```js
// app.js
'apostrophe-pages': {
  types: [
    {
      name: 'default',
      label: 'Default'
    },
    {
      name: 'home',
      label: 'Home'
    },
  ]
}

```

