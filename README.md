# Agile1

#This is simple project using GitHub

import java.io.*;
import java.util.*;
import java.math.*;
import java.lang.*;
 
class ex {
   
    public static void main(String args[])
    {
        Scanner in = new Scanner(System.in);
        
        String s = in.next();
        int n = s.length();
        char a[] = new char[n];
        HashSet<Character> fset = new HashSet<>();
        ArrayList<String> list = new ArrayList<>();
        
        for(int i=0; i<n; i++)
            a[i] = s.charAt(i);
            
        String temp = "";
        int i = 0;
        while(i!=n)
        {
            char c = a[i];
            for(int i=0; i<n; i++)
            {
                if(s.charAt(i)!=c)
                    temp = temp + s.charAt(i);
            }
            list.add(temp);
            temp = "";
        }
        
        Collections.sort(list);
        System.out.println("Answer:-");
        System.out.println(list.get(0));
        
        
    }
   
}
