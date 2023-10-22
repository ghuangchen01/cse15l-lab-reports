By Guan Hao Huang Chen
My codes:

import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    String st = " ";
    int num = 1;
    public String handleRequest(URI url) {
        if(url.getPath().equals("/")){
            return st;
        }else{
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    if(st.equals(" ")){
                        st = "1. ";
                        st = st + parameters[1] + "\n";
                        num++;
                    }else{
                        st = st + String.valueOf(num)+ ". " + parameters[1] + "\n";
                        num++;
                    }
                    return String.format(st);
                }
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


