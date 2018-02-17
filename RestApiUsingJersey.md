#REST API

  1. Jersey using Java-RX , used to write Rest apis for Java. (Earlier we use socket for interaction between server and client / SOAP.)
  2. Built on top of principles of HTTP
  3. Services can return 
    1. XML
    2. JSON
    3. HTML
    4. Plain Text 
    5. Binary/Octet like Images, Pdf etc.
    
#First REST API (Things Required)

  1.  Java8, Netbeans, Maven, Tomcat, spring STS
  2.  Add server as Tomcat version you are using. 
  3.  Download Jersey through Maven dependency.
  4. Most basic service requires : 
    1. @Path : The path to service 
    2. @GET - The request method
    3. @Produces - the response type from server 
 
#RESTFul Architecture
  1. Based on Richardson Maturity Model , Level 2 are verbs based on CRUD and points to post/get/put/delete.
  2. HATEOS : Hypermedia as the Engine of Application State, client interacts through with server through hypermedia. 
  3. JSON prefered for REST, best to use with Javascript. Xml is easy to validate and confirmed well formed but long lines and take time.
  4. Binary for Files,Images,Pdf used as @Produces(MediaType.APPLICATION_OCTET_STREAM).
  
#Using HTTP Get
  1. Needs to add XMLRootElement if error message is MessageBodyWriter not found for media type=xml
  2. Jersey Doesnt know how to add marshal POJO's to XML. Uses JaxB to do Java-to-XML.
  3. We use @Produces with GET. 
  4. JAXB converts POJO to XML and XML to JSON. 
  5. Add Postman to Chrome to have multiple Producer Type. \\ Not required
  
