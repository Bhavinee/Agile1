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
        HashSet<Character> fset = new HashSet<>();
        ArrayList<String> list = new ArrayList<>();
        
        for(int i=0; i<n; i++)
            fset.add(s.charAt(i));
            
        String temp = "";
        Iterator<Character> it = fset.iterator();
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
        System.out.println(list.get(0));
        
        
    }
   
}
