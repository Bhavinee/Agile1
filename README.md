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
        PrintWriter out = new PrintWriter(System.out,true);
        
        String s = in.next();
        int n = s.length();
        HashSet<Character> set = new HashSet<>();
        ArrayList<String> list = new ArrayList<>();
        
        for(int i=0; i<n; i++)
            set.add(s.charAt(i));
            
        String temp = "";
        Iterator<Character> it = set.iterator();
        while(it.hasNext())
        {
            char c = it.next();
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
        out.println(list.get(0));
        
        out.flush();
        
        
    }
   
}
