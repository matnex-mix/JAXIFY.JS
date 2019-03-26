# JAXIFY.JS
A JavaScript Library for AJAX Requests (Recursive) with form submission, url registeration, **Recursive Requests**

## JAX APIS

1. #### Url Registeration
    **Format:** `JAX.URL(URL, QUERY_PARAMETERS, REQUEST_METHOD, SUCCESS_CALLBACK, FAILURE_CALLBACK, END_RESULT)`
    
    **Example:** `JAX.URL("http://github.com", {}, "POST", (function($data){ console.log($data); }), null, "JSON")`
    
2. #### Getting Data From Url
   **Format:** `JAX.GET(RGISTERED_URL_INDEX)` or `JAX.URL(URL, QUERY_PARAMETERS, REQUEST_METHOD, SUCCESS_CALLBACK, FAILURE_CALLBACK, END_RESULT)`
   
   **Example:** `JAX.URL(0)`
   
3. #### Using HTML/CSS Loader
   **Format:** `JAX.registerLoader(HTML_ID_OR_HTML_OBJECT, CLASS_THAT_STARTS_THE_LOADER)`
   
   **Example:** `JAX.registerLoader($('#loader')[0], "active")` or `JAX.registerLoader("loader", "active")`

4. #### Starting Loader: (USED BY JAX ITSELF)
   **Format:** `JAX.runLoader()`
   
5. #### Sending Forms Data to url
   **Format:** `JAX.sendForm(REGISTERED_URL_INDEX, HTML_FORM_ELEMENT)`
   
   **Example:** `$('form').on("submit", function() { JAX.sendForm(0, this); })`
   
  ## Brief Explanation
   
