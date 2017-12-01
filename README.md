# fifth-point
package Quinto;

import java.io.BufferedReader;
import java.io.BufferedWriter;
import java.io.IOException;
import java.io.InputStreamReader;
import java.io.OutputStreamWriter;

/**
 *
 * @author PC-Lenovo
 */
public class Quinto {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) throws IOException {
        // TODO code application logic here
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
        int m;
        bw.write("ingrese el tamaño del arreglo ");
        bw.flush();
        m = br.read();
        double mitad = m / 2;
        
        
        int[][] arreglo = new int [m][m];
        
        for(int i = 0; i < m; i++){
            for(int j = 0; j < m; j++){
                arreglo[i][j] = (int) (Math.random()*100)+1;
                
                if(i == 0){
                    System.out.println(arreglo[0][j]); //borde superior
                    
                }
                if(j == 0){
                    System.out.println(arreglo[i][0]); // borde izquierdo
                    bw.flush();
                }
                if(i == m-1){
                    System.out.println(arreglo[m-1][j]); // borde inferior
                    bw.flush();
                }
                if (j == m-1){
                    System.out.println(arreglo[i][m-1]); //borde derecho
                    bw.flush();
                }
                
            }
        }
        for(int i = 1; i < m-1; i++){// utilizando el borde del arreglo como un limite
            for(int j = 1; j < m-1; j++){ // utilizando el borde del arreglo como un limite
                double medio = mitad - 0.5;
                double derecha = medio;
                if (m % 2 == 0){//par
                
                }
                if(m % 2 != 0){// impar 
                    
                    if(j != medio){ // no se imprimen los numeros ubicados en el medio del arreglo
                        if(derecha < m+1){
                            System.out.println(arreglo[i][j]);
                            derecha = derecha + 1;
                            
                        }else{
                            if(derecha == 1-m){
                                
                            }
                        }
                        
                    
                    
                    
                    }
                }
            }
        }
    }
}
