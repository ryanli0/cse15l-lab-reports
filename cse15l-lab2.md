# Lab Report 2

## Part 1

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

![Image](Lab2Screenshot.jpg)

##### This screenshot shows the output if the url "localhost:4000/add-message?s=Hello" is executed. It uses the handleRequest method to properly format the new line by giving it a number, a period, the message itself, and then a "\n" to prepare for another message. Without any message, the message "Empty message list!" is given.

![Image](Lab2Screnshot2.jpg)

##### This screenshot shows the output if the url "localhost:4000/add-message?s=How are you" is executed. As with the last message, it uses the handleRequest method to properly format the new line by giving it a number, a period, the message itself, and then a "\n" to prepare for another message.

##### This URL is converted to "localhost:4000/add-message?s=How%20are%20you" to handle the spaces

## Part 2

##### Image of private key
![Image](Lab2LocalKey.png)

##### Image of public key
![Image](Lab2PublicKey.png)

##### Image of login attempt without password
![Image](Lab2Login.png)
