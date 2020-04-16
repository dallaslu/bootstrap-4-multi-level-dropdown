# Bootstrap 4 Multiple Level Dropdown

Using official HTML without adding extra CSS styles and classes, it's just like native support. 

All things listed in https://getbootstrap.com/docs/4.4/components/dropdowns/ are not effected. You can use css classes and js methods/events/options freely.

Dropdown of bootstrap can be easily changed to infinite level. It's a pity that they didn't do it.

## Usage

Just add js after jquery and bootstrap js files 

```html
<script src="https://raw.githubusercontent.com/dallaslu/bootstrap-4-multi-level-dropdown/master/bootstrap4-dropdown-ml-hack.js"></script>
```
If your want a hover tigger, just add class and some custom styles to reduce spacing to avoid triggering mouseleave.
```css
.dropdown-hover-all .dropdown-menu { margin:0 }
```
Then, add event handler(suggest 'toggle' for best experience):
```javascript
$('.dropdown-hover-all').on('mouseenter', '.dropdown', function() {
  if(!$(this).hasClass('show')){
    $('>[data-toggle="drpodown"]', this).dropdown('toggle');
  }
}
$('.dropdown-hover-all').on('mouseleave', '.dropdown', function() {
  if($(this).hasClass('show')){
    $('>[data-toggle="drpodown"]', this).dropdown('toggle');
  }
}
```


## Demo

Here is a perfect demo: https://jsfiddle.net/dallaslu/adky6jvs/ (works with Bootstrap v4.4.1)
