# making-db-Connection

/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package inheri2;

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.ResultSet;
import java.sql.Statement;

/**
 *
 * @author NetworkAcademy
 */
public class dbClass1 {
    public static void main(String[] args) {
        try {
        String username1 = "username1";
        String password1 = "password1";
        String host = "jdbc:derby://localhost:1527/database1";
        Connection con = DriverManager.getConnection(host, username1, password1);
        
        Statement obj1 = con.createStatement();
        
        String query1 = "select * from tablename1";
        ResultSet res = obj1.executeQuery(query1);
        
        res.next();
        
        int id = res.getInt("ID");
        String value = res.getString("value1");
        
        System.out.println("ID is :" + id + "; Values is :" + value);
        }
        
        catch(Exception e){ 
            System.out.println("Exception");
        }
        }
        
    }
    

