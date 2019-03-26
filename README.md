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

## Using Recursive Requests
Recursive/Cyclic/Repititive Requests are requests that gets made at intervals of time, they can be hold or left to run to infinity. Recursive Requests are useful for doing a no load message chatting system, instant notification system e.t.c

### Let's Dive In
You Create a JAX Cyclic Request
    ```$cq = new JAX.CyclicRequest(URL, REQUEST_METHOD, QUERY_PARAMETERS, DELAY_IN_MILLISECONDS);```
    
You Start it:
    ```$cq.start();```
    
#### Events
**Format:** ```$cq.EVENT_NAME = function(){ //...block of code }```

##### onsuccess
When the Request was completed successfully just like the success callback
##### onfailure
When the Request Failed (Normally not Always Called)
##### oncyclestart
Called Before the Start of every request cycle
##### oncycleend
Called at the very end of every request cycle

#### Controls
**Format:** ```$cq.CONTROL_NAME()```

##### hold
stops the continuity of the request
##### unhold
continues a sttoped requests

## Brief Explanation
   CALLBACKS can either be a function or the name of a function and they take argument which will contain the refined responseText from the url. At present, JAX can only runs 1 Request at a time but we hope to change this soon meanwhile, Enjoy JAXIFY to the Fullest.
   
**Note: THIS IS NOT YET A STABLE RELEASE OF JAXIFY.JS BUT YOU ARE FREE TO TRY IT AND GIVE US CONTRIBUTIONS OR IDEAS**
   
