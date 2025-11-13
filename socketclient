package Pakg;
import java.net.*;
import java.io.*;
import java.util.*;

public class SocketClient {
    public static void main(String[] args)throws Exception
    {
        Scanner in=new Scanner(System.in);
        Socket clientSocket=new Socket("127.0.0.1",4000);
        System.out.println("**** CLient side****");
        System.out.println("enter file name to transfer");
        String fname=in.nextLine();
        OutputStream ostream=clientSocket.getOutputStream();
        PrintWriter pwrite=new PrintWriter(ostream, true);
        pwrite.println(fname);
        InputStream istream=clientSocket.getInputStream();
        BufferedReader socketRead=new BufferedReader(new InputStreamReader(istream));
        
        System.out.println("content of the filew"+ fname+"are");
        String str;
        while((str=socketRead.readLine())!=null)
        {
            System.out.println(str);
        }
        pwrite.close();
        socketRead.close();
        
    }
}