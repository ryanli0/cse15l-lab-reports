# Lab Report 2

``` bash
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    ArrayList<String> messageList = new ArrayList<>();
    

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            //handles an empty message list
            if (messageList.isEmpty()){
                return "Empty message list!";
            } else {
                //builds line by line if the messageList is not empty
                StringBuilder allMessages = new StringBuilder();
                for (int i = 0; i < messageList.size(); i++) {
                    allMessages.append((i+1)).append(". ").append(messageList.get(i)).append("\n");
                }
                return allMessages.toString();
            }
        }
        //adds message if URL contains a message and places the given message to
        //messageList
        else if (url.getPath().contains("/add-message")) {
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")) {
                messageList.add(parameters[1]);
                return "Message successfully added";
            }
        }
        return "Invalid request!";
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
