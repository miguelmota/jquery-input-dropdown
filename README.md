# jQuery inputDropdown

# Demo

[http://lab.miguelmota.com/jquery-input-dropdown/demo/](http://lab.miguelmota.com/jquery-input-dropdown/demo/)

# Install

Available via [bower](http://bower.io/)

```bash
bower install jquery-inputdropdown
```

# Example

```html
<input type="text" class="indpn-input" placeholder="Country">
<span class="indpn-dropdown-arrow"></span>
<div class="indpn-dropdown"></div>
```

```javascript
var countries = [{"id":0,"text":"Abkhazia"},{"id":1,"text":"Aland"},{"id":2,"text":"Albania"}];

$('.indpn-input').inputDropdown({
    data: function() {
        return $.map(countries, function(o,i) {
            return o.text;
        });
    },
    onSelect: function(selected) {
        console.log(selected);
    },
    toggleButton: $('.indpn-dropdown-arrow'),
    container: $('.indpn-container'),
    dropdownContainer: $('.indpn-dropdown'),
    image: function(item) {
        return ['/images/flags/32/',item.replace(/\s+/, '-'),'.png'].join('');
    },
    defaultImage: '/images/search.png',
    debug: false
});
```

# License

Released under the MIT License.
