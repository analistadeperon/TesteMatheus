using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace AtFinal
{
    class Program
    {

        struct Cliente
        {
            public int cod_cli;
            public string nome, endereco, telefone;
        }

        struct Recebimento
        {
            public decimal valorDoc;
            public DateTime dataEmissao, dataVencimento;
        }

        public static void Main(string[] args)
        {
            Cliente[] clientes = new Cliente[5];
            Recebimento[] recebimentos = new Recebimento[15];

            int qtdCliente = 0;
            int qtdRecebimento = 0;
            int opcao = -1;

            do
            {
                Console.Title = " * SISTEMA DE RECEBIMENTOS * ";
                Console.BackgroundColor = ConsoleColor.White;// Muda a cor da tela.
                Console.ForegroundColor = ConsoleColor.DarkBlue;// Muda a cor da letra.
                Console.Clear(); //limpa a tela

                //Imprime na tela as opções do Menu:
                Console.WriteLine("-------------------------");
                Console.WriteLine("     MENU DE OPÇÕES      ");
                Console.WriteLine("-------------------------");
                Console.WriteLine(" Informe a opção deseja: \n");
                Console.WriteLine("1. Cadastrar Cliente");
                Console.WriteLine("2. Alterar Cliente");
                Console.WriteLine("3. Cadastrar Recebimento");
                Console.WriteLine("4. Sair");
                Console.SetCursorPosition(25, 3); //Move o cursor para o fim da 4a linha

                //lê a opção escolhida pelo usuário
                opcao = Convert.ToInt32(Console.ReadLine());

                //limpa a tela
                Console.Clear();


                //direciona o programa para a opção escolhida pelo usuário:
                switch (opcao)
                {
                    case 1:
                    //Testa se já chegou ao limite de clientes cadastrados
                    //onde o limite é o tamanho (Length) do vetor:
                    if (qtdCliente < clientes.Length)
                    {
                        //Preenche os dados do cliente
                        Console.WriteLine("Digite os dados do cliente \n");
                        Console.Write("Código: ");
                        clientes[qtdCliente].cod_cli = Convert.ToInt32(Console.ReadLine());
                        Console.Write("Nome: ");
                        clientes[qtdCliente].nome = Console.ReadLine();
                        Console.Write("Endereço: ");
                        clientes[qtdCliente].endereco = Console.ReadLine();
                        Console.Write("Telefone: ");
                        clientes[qtdCliente].telefone = Console.ReadLine();

                        //incrementa o número de clientes
                        qtdCliente++;

                        Console.WriteLine("\nCliente Cadastrado com sucesso!");
                    }
                    else
                    {
                        Console.WriteLine("Número máximo alcançado: " + qtdCliente);
                    }

                    Console.Write("\nPressione qualquer tecla para voltar ao menu.");

                    //Aguarda o usuário pressionar qualquer tecla para continuar:
                    Console.ReadKey();
                    break;
                    case 2:
                        Console.WriteLine(" vazio ");
                        Console.ReadKey();
                        break;
                    case 3:
                        //Testa se já chegou ao limite de Recebimentos cadastrados
                        //onde o limite é o tamanho (Length) do vetor:
                        if (qtdRecebimento < recebimentos.Length)
                        {
                            //Preenche os dados dos Recebimentos
                            Console.WriteLine("Digite os dados dos Recebimentos \n");
                            Console.WriteLine("Número do documento: " + (qtdRecebimento + 1));
                            Console.Write("Valor R$: ");
                            recebimentos[qtdRecebimento].valorDoc = Convert.ToDecimal(Console.ReadLine());
                            Console.Write("Data de emissão: ");
                            recebimentos[qtdRecebimento].dataEmissao = Convert.ToDateTime(Console.ReadLine());
                            Console.Write("Data de vencimento: ");
                            recebimentos[qtdRecebimento].dataVencimento = Convert.ToDateTime(Console.ReadLine());

                            qtdRecebimento++;

                            Console.WriteLine("\nRecebimento cadastrado com sucesso!");
                        }
                        else
                        {
                            Console.WriteLine("Número máximo já alcançado: " + qtdRecebimento);
                        }

                        Console.Write("\nPressione qualquer tecla para voltar ao menu.");

                        //Aguarda o usuário pressionar qualquer tecla para continuar:
                        Console.ReadKey();
                        break;
                    case 4:
                        Console.Title = " * SAIR * ";
                        Console.WriteLine("------------------");
                        Console.WriteLine("Saindo do Sistema");
                        Console.WriteLine("------------------");
                        Console.ReadKey();
                        break;

                    default: //executado quando o usuário escolhe uma opção que não existe
                        Console.Title = " * INVALIDO * ";
                        Console.WriteLine("---------------");
                        Console.WriteLine("Opção inválida!");
                        Console.WriteLine("---------------");
                        Console.Write("\nPressione qualquer tecla para voltar ao menu.");
                        //Aguarda o usuário pressionar qualquer tecla para continuar:
                        Console.ReadKey();
                        break;
                }
            } while (opcao != 4);
        }
    }
}
