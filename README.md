# JAXIFY.JS
A JavaScript Library for AJAX Requests (Recursive) with form submission, url registeration, **Recursive Requests**

##JAX APIS

1. #### Url Registeration
    **Format:** `JAX.URL(URL, QUERY_PARAMETERS, REQUEST_METHOD, SUCCESS_CALLBACK, FAILURE_CALLBACK, END_RESULT)`
    
    **Example:** `JAX.URL("http://github.com", {}, "POST", (function($data){ console.log($data); }), null, "JSON")`


