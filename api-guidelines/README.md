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