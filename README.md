//dockerfile for hello

FROM eclipse-temurin:21-jdk

WORKDIR /app

COPY hello.java /app

RUN javac hello.java

CMD ["java", "hello.java"]


///java code for login app

import java.util.Scanner;

class user {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Username: ");
        String u = sc.nextLine();

        System.out.print("Password: ");
        String p = sc.nextLine();

        if(u.equals("admin") && p.equals("1234"))
            System.out.println("Login Successful!");
        else
            System.out.println("Invalid Login!");

        sc.close();
    }
}
