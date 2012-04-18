API Guidelines
==============

 *  User/password authentication via HTTP basic, since it's fast, doesn't 
    require more than `curl`, and you can even make some requests from a 
    browser. (We're using SSL on all ends, so there's no security issues.)

 *  Use HTTP verbs to mean something
    
    Any API consumer is capable of sending GET, POST, PUT, and DELETE verbs, and 
    they greatly enhance the clarity of what a given request does. It’s 
    terrifying to use an API where a GET request can change the underlying data.

 *  Sensible resource names
    
    Having sensible resource names/paths (e.g., `/posts/23` instead of 
    `/api?type=posts&id=23`) improves the clarity of what a given request does.

 *  Examples that show the full request.
    
    **Request:**
    <pre>GET http://api.kundportalen.se/users.json</pre>
  
    **Expected Response:**
    <pre>
    HTTP/1.1 200 OK
    Content-Type: application/json; charset=utf-8
    
    [
      {
        "id": 535131,
        "name": "Bobby Idol"
      }
    ]
    </pre>

  * Error handling
    
    A client who sends in a request that causes an error, from runtime error to 
    business logic violation, should receive a informative error (formatted as JSON)
    message and optionally a body describing or showing where the error came from. I.e.

    <pre>
    HTTP/1.1 403 
    Content-Type: application/json; charset=utf-8
    
    errors => [
      {
        "message": "User id invalid or missing"
      }
    ]
    </pre>   
    
    The http status code should be set to something in the 4xx or 5xx depending on
    which is appropriate to the error. 400 for unparsable JSON in request, 401 for 
    an authorisation problem and so on. More than one error can be returned.
    
    