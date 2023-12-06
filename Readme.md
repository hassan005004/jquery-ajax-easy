### On Click Data Attribute to Serve via Ajax
You just need to pass your all data in data attibute to handle this function\n
file name: data-attribute-to-server.html

```
// on time triggering function
// this function is needed to handle response like loader or somethig different
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

```
// this is calling method
  <button class="btn btn-primary trigger-js"
    data-url="https://you-url.com"
    data-ask-confirmation="true"
    data-order-id="1"
    data-order-title="1"
  >Call It</button>  
```

