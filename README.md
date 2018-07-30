# MyException

public class MyException extends Exception
{
    @Override
    public String toString()
    {
        return "You are not valid voter";
    }
}


# Main

import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class Main
{
    public static void main(String[] args) throws IOException, MyException {
        BufferedReader br=new BufferedReader(new InputStreamReader(System.in));
        System.out.println("Enter your age:");
        int age;
        age=Integer.parseInt(br.readLine());

        if(age<18)
        {
            throw new MyException();
        }
        else
        {
            System.out.println("You are valid user");
        }
    }
}
