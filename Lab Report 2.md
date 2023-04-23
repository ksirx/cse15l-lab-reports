__Name: Xavier Navarro__

__CSE 15L Lab Report 2__

During week 2 lab, I learned about servers. Here is a short demonstration of how web servers work! 

__Part 1: StringServer__

Here is some code which adds strings over and over to a server using the ```\add-message?s=<string>``` as a path at the end of a url.
```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    String message = "";
    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format("%s", message);
        } else {
            System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/add")) {
                String[] parameters = url.getQuery().split("/");
                for (int i = 0; i < parameters.length; i++) {
                    String[] toAdd = parameters[i].split("=");
                    message = message + toAdd[1] + "\n";
                }
                return String.format("%s\n", message);
            }
            return "404 Not Found!";
        }
    }
}

class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```

This code results in something like this happening...

![Image](2023-04-22 (1).png)

As you can see, the main method in the ServerString class takes in a integer between 1024 and 49151 and forms a link to the created server. In this example, I chose 1235 which can clearly be seen through the url. This change happens when ```Server.start(port, new Handler());``` is called. 

You'll also notice that the string added to path specified earlier was added to the server itself. This occurs in the Handler class where the handleRequest method is called. It takes the url as an arguement which in this case would be ```localhost:1235/add-messages?s=Hello```. In this code, the url is first split by ```/``` to isolate the path, then split by ```=``` to isolate the wanted term. This is then added to an empty string with the addition of ```\n``` to form a new line. When the site is updated, ```Hello``` will be shown on the server.

![Image](2023-04-22 (2).png)
