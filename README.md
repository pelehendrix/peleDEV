# peleDEV
import java.util.Scanner;

 public class Codificacao{
 
public static void main(String[] args) {
    // TODO Auto-generated method stub
        System.out.println("Digite a sequencia");
        
    Scanner s =new Scanner(System.in);
    String input=s.nextLine();
    
    
        int tamanho = input.length();
        int i = 0;
        int pas = 0;
        char quebra = input.charAt(0);

            String saida = "";
            
            for(;i<tamanho;i++)
            {
                if(i+1<tamanho)
                {
                    if(input.charAt(i) == input.charAt(i+1))
                        
                    {
                        pas++;
                    }
                    
                    else
                    { 
                        
                        saida = saida + 
  (pas+1) + quebra;
                        pas = 0;
                        quebra = input.charAt(i+1);
                    }
                }
                else
                {
                    saida = saida + 
 (pas+1) + quebra;
                }
            }

            System.out.println("Resultado " + saida);   

        }
}
