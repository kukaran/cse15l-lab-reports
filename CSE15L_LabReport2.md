CSE 15L Lab Report 2

Kumail Karan 

A17688437

Part 1:

Code For ChatServer:

```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    String chat = "";

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return chat;
        } else if (url.getPath().equals("/add-message")) {
            String[] parameters = url.getQuery().split("=");
            String[] MessageAndUser = parameters[1].split("&");
            chat = chat+parameters[2]+": "+MessageAndUser[0]+"\n";
            return chat;

        } else {
            return "Error! Path Not Found!";
        }
    }
}

class ChatServer {
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
Screenshots of using /add-message:


