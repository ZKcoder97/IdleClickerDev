using System;
using System.Collections.Generic;
using System.Data;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace IdleClickDev
{
    internal class Program
    {
        static void Main(string[] args)
        {
            //Variaveis
            bool repeticaoInicio = true;
            int Dinheiro = 0; int CLick = 1; string ganhaPao = null; int precoItemCLick = 50;
            //Inicio
            while (repeticaoInicio)
            {
                Console.WriteLine("Idle Clicker Dev");
                Console.WriteLine($"Dinheiro: {Dinheiro}");
                Console.WriteLine("Digite UPGRADE Para Acessar Menu De Melhorias!");
                Console.WriteLine("Pressione A Tecla ENTER Para Ganhar Dinheiro!");
                Console.WriteLine($"Dinheiro Por Click: {CLick}");
                ganhaPao = Console.ReadLine();
                ganhaPao = ganhaPao.ToLower();
                switch (ganhaPao)
                {
                    case "upgrade":
                        var repostaMetodo = UPGRADE(Dinheiro, CLick, precoItemCLick);
                        Dinheiro = repostaMetodo.Dinheiro;
                        CLick = repostaMetodo.Click;
                        precoItemCLick = repostaMetodo.precoItemCLick;
                        Console.Clear();
                        break;
                    default:
                        Console.Clear();
                        Dinheiro = Dinheiro + CLick;
                        break;
                }
            }
            //Fim
        }

        //Classe Upgrade
        static (int Dinheiro, int Click, int precoItemCLick) UPGRADE(int Dinheiro, int Click, int precoItemCLick)
        {
            //Variaveis
            bool repeticaoUP = true; string opcao = null; 
            //Inicio
            while (repeticaoUP)
            {
                Console.Clear();
                Console.WriteLine("Idle Clicker Dev");
                Console.WriteLine($"Dinheiro: {Dinheiro}");
                Console.WriteLine($"Click: {Click}");
                Console.WriteLine($"Upgrade Para Click: {precoItemCLick}");
                Console.WriteLine("Click, Sair");
                Console.Write("Digite O Item Que Deseja Melhorar: ");
                opcao = Console.ReadLine();
                opcao = opcao.ToLower();
                switch (opcao)
                {
                    case "click":
                        if (Dinheiro >= precoItemCLick) { Dinheiro = Dinheiro - precoItemCLick; Click = Click * 2; precoItemCLick = precoItemCLick * 2; }
                        else { Console.Clear(); Console.WriteLine("Saldo Insuficiente"); }
                        break;
                    case "sair":
                        repeticaoUP = false;
                        break;
                    default:
                        Console.Clear();
                        break;
                }
            }
            return (Dinheiro, Click, precoItemCLick);
        }
    }
}
