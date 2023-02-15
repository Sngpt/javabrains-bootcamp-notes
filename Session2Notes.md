1) Learned about what is Dotcom bubble.
2) To become successful software engineer, one needs the Ability to apply technology, solve new problems, empathize with users or audience.
3) This bootcamp improves our ability to become  better backend developer.

1) What exactly meant by java backend engineer? 
Your customers are most often other developers(people who write front ends or other backends).
You are suppling api's. We write code which interfaces with others code.
2) Mostly deals with 3 tier architecture in java applications.
Frontend , Mid and data tier.

Currently most of the applications uses CDN in this way:
 Browser makes the request to CDN.(most of the web applications are rich client applications which are written mainly in javascript and have distinct separation from java side of things)
 u have a webpage loaded.Javascript makes the rest call to the server side.
3) As a backend developer we are goona building API Gateway and services.
4) CDN means Content Delivery Network.

1) What will happen when we type a address in webbrowser?
A: CDN are distributed servers that deliver web content to users based on their geographic location.
Eg: Aws has CDN servers called cloud front. There are other CDN servers called cloud flair.
CDN has two types of servers : Origin Server and Edge Server.

**A web Request:**
Browser sends a request to the DNS(domain name system) Server to resolve the domain name of the URL to its
corresponding IP address.
DNS is basically an aliasing system of domain names to ip address.
The DNS server returns the IP address of the closest CDN edge server to the user's location.
The browser sends the request to the CDN edge server.
The CDN edge server checks its cache.
If found in the cache, the CDN edge server returns the cached version.
If not found in the cache, the CDN edge server sends a request to the origin server.
The origin server returns the requested content to the CDN edge server.
The CDN edge server stores it in cache
The CDN edge server returns the content to the browser.


**A Web Page**

CDN contain ony static content like HTML page,CSS assests,Images, JS assets,Fonts.
IF two users accessing the web page, they both get the same content, this is called static content.

Grpc,GraphQL,Rest are the possible api calls from javascript of UI.

REST Requests:
1) JavaScript code constructs an HTTP Request(XMLHttpRequest)
2) Adds endpoint API URL and HTTP Method (get,post,put,delete)
3) Includes necessary parameters and data
4) Server gets request and returns response. --> As backend developer, we work on this.
5) JavaScript receives Response and processes it.
6) Response manifests as a UI change

A capable backend has to
1) Intercept requests
2) Extract data from requests
3) Process the request
4) Pull necessary data from database.
5) Process the data and prepare response.
6) Return the response.

Handling Requests (HTTP Protocol):
1) HTTP request is a message sent by a client (such as a web browser) to a server to request specific information.
2) Every http request comprises of three main components: 
     a) Request line (Get/index.html HTTP/1.1)
     b) Headers : Meta info about the request.(What is the nature of the request)
        Host: www.example.com
        User-agent : Mozilla/5.0
         Accept-language:en-US,en;q=0.5   (q is for preference.Default preference value is 1. If language is not found, server returns 400 error)
         Accept-Encoding:gzip,deflate
         Connection : keep-alive
       c) Request body
3) Every http request excepts a http response. Components of http response:
 Status line: First line eg:'HTTP/1.1 200 OK'
  Headers : Meta information about the response. (Date,Server:Apache/2/4/46,Last-Modified,Content-type,content-length,connection)
  Body : Actual Data being sent.
4) Http request call from javascript returns a json as response body. { "message": "Hello world","timestamp":"Mon,01 Feb2023"}

5) An opinionated way of using http is REST. REST set standards about how to use http protocol.
HTTP is a mechanism.
6) If connection is alive, multiple requests and responses can be made in a single connection.
Connection ends when its timeout. 
7) If we keep connection as alive, we can avoid three handshakes as part of http protocol between client and server.

8) HTTP is a Stateless protocol. 
Server cannot remember a pervious request.
Every request should be self sufficient.
We cannot refer a previous request inside a request
A request cannot remember its previous request.
Cookies allows multiple requests to be tied together.
Cookies are initiated by server. These are sent to the client in the set-cookie header of a response by server.
9) Automatically the client will send back the cookie to the server in the cookie header of subsequent requests.
Eg: Login flow.(Session id will be set as cookie in the response)

What we need as a back end developer:
1) A programming language (java)
2) A server runtime (tomcat,jetty . These are application servers.)
3) A framework to handle common concerns.(spring/spring boot)
4) A framework to interact with the database.
5) A framework to handle security. (Spring security)
6) A framework to manage infrastructure (microservices) (Spring cloud)

webserver hosts and serves static content(html,css,javascript) that doesn't require execution of code.
Appserver serves content that is result of execution of code.
CDN is a webserver.

Diff between services and application: facebook is an app. Services are things that work together to form an application.
An application needs multiple services to achieve its functionality. 

If we build an app using cloud native way, everything is a service (database,authentication...)

Fat jar is a jar with main method which spins out its own servlet container.

Git - manages versions of your code locally or on a remote servers.
GitHub - is a potential main remote server.



Session2 

https://www.markdownguide.org/cheat-sheet/

Primitive Datatypes:
double(8 bytes) is larger than float(4 bytes). These store decimal numbers.
int(4 bytes),long(8 bytes),short(2 bytes),byte store whole numbers.

int,double are most commonly used.

Non Primitive Datatypes: String,Array,Class,Interface,Enum,Record(Record is an extension of class.Its a new feature)
An array is a collection of similar data types.Each element in an array is accessed by its index.

Always refer as member variables and methods in the context of class.

An enum is a special datatype that allows the programmer to define a set of named values.

A Record is a special datatype that allows programmer to define a "carrier" of data.

float a = 1.2345f;
long w = 375937434883408L;

In java, right expressions are evaluated first and then left expressions in assignments like float a = 1.234f;

As per java standard or convention,compiler considers a number literal as an int and decimal number literal as double.

A reference variable holds the address of the object .

Collection framework is introduced in java 5.
Wrapper classes came into picture to use primitive data types in collections.

AutoBoxing -> Integer i = 10;


Operator precedence:
PEMDAS : Parenthasis,Exponents,(Multiplication,Division),(Addition,subtraction)

Ternary operator is shortway of writing if else statement: int m = (x<y)?x:y;

sout+enter or soutv gives the stmt system.out.println in intellij. Its a shortcut.

Integer in = new Integer(2); (this kind of initialisation is deprecated as it can be acheived using autoboxing)

From java11, we no need to separately use javac command for compilation of java files from command prompt. java command alone compiles and runs .java file.
Give command java HelloWorld.java.

System.arraycopy(array1,0,array2,0,5);
java.util.Arrays class has so many static methods like sort,binarySearch,fill.

Encapsulation is used to hide the implementation details of a class and expose only the necessary information 
to the outside world. It can be achieved through private,public,protected access modifiers.
Predictable controlled access and expose apis are the benefits of encapsulation.

Polymorphism allows objects of different classes to be treated as objects of a common parent class.

Static is used to indicate that a member belongs to the class itself rather than to a class instance.

Explore the concept of shadowing in inheritance ?? 
Static block is a block of code that gets executed when a class is first loaded into memory.

A static field is a field that belongs to the class.
A static inner class is a nested class that is a member of its enclosing class but doesnot have access
to the enclosing class's instance variables.

Why main is static? JVM needs a static method(a piece of code) to create a first instance.
A static method can only access static variables and static methods.
Static variables are also called as Class variables.They are shared by all instances of a class.
If one object modifies the value of a static variable, the change is reflected in all instances
of that class.

Nested classes - A class defined in another class. Two types-> Static nested classes or static inner classes, inner classes
class outerclass{
    static class NestedClass {
    }
}
OuterClass.NestedClass nestedObject = new OuterClass.NestedClass();

Inner class:
class OuterClass {
    class InnerClass {
    }
}
OuterClass outerObject = new OuterClass();
OuterClass.InnerClass innerObject = outerObject.new InnerClass();

Inner CLasses types:
1) Member inner class - a class defined inside another class but outside a method.
2) Local inner class - a class defined inside a method.
3) Anonymous inner class
4) Lambda expression

Records:
Records are a compact and easy to use way to create simple data classes that have only private
fields and a public constructor and no methods.
Introduced in java 14 as preview feature and available to public from java 17.

Records are shallowly immutable and are carrier for a fixed set of values.
Records are used to carry the values for its member variables that uniquely represent the instance entirely.

eg: public class Point {
        private int x;
        private int y;
    } 
is equivalent to 
public record Point(int x, int y) {}

How record works:
fields are automatically generated as private final.
Constructor is automatically generated to initialise all fields.
Automatically generates methods like equals(),hashcode(),toString()
Automatic accessors.

Point point1 = new Point(1,2);
Point point2 = new Point(1,2);
System.out.println(point1.equals(point2));
point1.x() // stmt to access x variable.

Records are not meant to replace classes.

data abstraction???
--------------------
Encapsulation is a concept that refers to the practice of bundling data and methods together into a single unit, called a class, and controlling access to that data and those methods from outside the class. This helps to prevent unauthorized access and modification of the data, and promotes modularity and code reuse.
Encapsulation can be understood as an application of the principle of abstraction. Abstraction is one of the key concept in mathematics as well that refers to the process of isolating and focusing on certain aspects of a system, while ignoring others. This allows us to reason about the system in a more general and simplified way, and to apply our knowledge and understanding of the system to a wide range of situations.

In the case of encapsulation, we are abstracting away the details of the implementation of a class, and instead focusing on its interface, which consists of the methods that can be called and the data that can be accessed from outside the class. By controlling access to this interface, we can ensure that the data is used and modified in a safe and consistent way, and that the methods operate correctly and efficiently.
For example we could provide some logic and precondition in our setters (do not allow certain values to be set. Let's say we won't allow a negative value to be entered for age (for the Person class).).

From a philosophical perspective, encapsulation can be seen as an application of the principle of information hiding or data hiding. This principle states that information should only be accessible to those who need it, and that unnecessary exposure of information can lead to some errors and vulnerabilities. Encapsulation achieves this goal by hiding the implementation details of a class, and only exposing its interface to the outside world.

-----------------------
Abstraction is the practice of hiding the complex implementation details of a software component, and presenting a simplified interface to the user. This allows the user to interact with the component without needing to know or understand the underlying details. Example:
A TV remote control that has buttons for changing channels, adjusting the volume, and turning the TV on and off. The implementation details of how the TV actually changes channels or adjusts the volume are hidden from the user of the remote control. The user simply presses the button labelled "channel up" or "volume up" and the TV responds as expected.

Encapsulation, on the other hand, refers to the bundling of data and functions into a single unit, or object. In Java, this is achieved through the use of classes and objects. Encapsulation provides a mechanism for enforcing data hiding and protecting the data from unwanted access and modification. Example:
Consider a class named Person that has three attributes: name, age, and address. To protect these attributes from being directly accessed and modified by code outside of the Person class, we could declare these attributes as private and provide public methods for accessing and modifying them.
class Person {
private String name;
private int age;
private String address;

public String getName() {
return name;
}

public void setName(String name) {
this.name = name;
}

public int getAge() {
return age;
}

public void setAge(int age) {
this.age = age;
}

public String getAddress() {
return address;
}

public void setAddress(String address) {
this.address = address;
}
}

In summary, abstraction is about hiding complexity and encapsulation is about hiding data. Both concepts are important for creating maintainable, scalable, and secure software.
---------------
Java is strictly pass by value.
The value stored by the variable is always copied. But the trick is what type is the variable and value passed into the method.

If the variable is of a primitive type, it stores its value on the stack part of the memory (most often), and all primitive values are generally stored there, in binary notation also all primitives values are immutable.
In the case of the reference type of the variable, the address of the memory location of the "object" located in the Heap part of the memory (again the binary record of that memory location) is stored on the stack.

In the first case, if we have int a = 5, the value 5 in the binary record is copied. Any handling with this copied variable ie. local variable and the value it has has no effect on the original variable. You cannot change the value of a primitive variable, you can only assign a new value to the variable in another location, but that has no effect on the value stored by the original variable. That is why it is an immutable value.

In the second case, with reference or address variables, if we say Person a = new Person(); and pass a to a method, the direct memory location (address) of the created object is copied from the Heap (more precisely, with new Person() we allocate a certain memory space on the Heap part of the memory and it is located at a memory address). In this way, we have two variables that are named differently but point to the same memory location, i.e. the same instance (the original and the one passed to the method, i.e. the copied one). Now with this copy of the variable we have access to the same instance that the original variable points to and we can also change the values (If the object is mutable).
This is not the case with Immutable object types, such as String.




