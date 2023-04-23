__Name: Xavier Navarro__

__CSE 15L Lab Report 2__

During week 2 lab, I learned about servers. Here is a demonstration of how web servers work! 

_Part 1: StringServer_

I am going to show you 
```import java.io.IOException;
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

///add-message?s=Hello
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
