### On Click Data Attribute to Serve via Ajax
You just need to pass your all data in data attibute to handle this function\n
file name: data-attribute-to-server.html

```
this data attribute is must data-url="https://you-url.com"
```

```
// pass data attribute where to use this function
  <button class="btn btn-primary trigger-js"
    data-url="https://you-url.com"
    data-ask-confirmation="true"
    data-order-id="1"
    data-order-title="1"
  >Call It</button>  
```

```
// handle call response
$('.trigger-js').click(function(){
  //Some code
  data_url = $(this).attr('data-url');
  output = $.fn.callDataAttributeAjax(this);
  output.then(function(data) {
    // handle success here
    // $("#loader").addClass("d-none");
  }).catch(e => {
    toastr['error']('Something went wrong');
    // handle catch
    // $("#loader").addClass("d-none");
  });
});
```
