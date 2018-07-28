
language-ezml
=============
[ezml](http://ezml.info/) language grammar for GitHub's [Atom](https://atom.io/) IDE.

![screenshot](http://ridingtheclutch.com.s3.amazonaws.com/images/language-ezml.png)

## Supported Filetypes

* `.ezml`
* `.ezmlc` (CoffeeScript ezml)

## Supported filters

You can switch to another language right in the middle of your ezml file by
using a "filter":

![screenshot](http://ridingtheclutch.com.s3.amazonaws.com/images/ezml_filters.png)

This ezml bundle currently supports the following filters:

* `:css`
* `:coffee`
* `:javascript`
* `:markdown`
* `:php`
* `:ruby`
* `:ruby2js`
* `:sass`
* `:scss`

The ezml documentation lists the following additional filters:

* `:cdata`
* `:erb`
* `:escaped`
* `:less`
* `:plain`
* `:preserve`
* `:textile`

To add more you can simply copy and paste one of the captures in the `ruby ezml.cson` file
and make the changes necessary to support your filter of choice:

```cson
{
  'begin': '^(\\s*)(:css)'
  'beginCaptures':
    '2':
      'name': 'entity.name.tag.ezml'
  'end': '^(?! *$|\\1 )'
  'name': 'source.css.embedded.html'
  'patterns': [
    {
      'include': 'source.css'
    }
  ]
}
```
