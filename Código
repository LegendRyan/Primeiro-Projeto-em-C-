//Screen Sound
using System;

string mensagemDeBoasVindas = "Boas vindas as Screen Sound";
//List<string> listaBandas = new List<string> { "U2", "The Beatles", "Set it off", "Linkin Park"};
Dictionary<string, List<int>> RegistroBandas = new Dictionary<string, List<int>>();
void ExibirLogo()
{
    Console.WriteLine(@"
█▀▀ █▀▀ █▀▀█ █▀▀ █▀▀ █▀▀▄ 　 █▀▀ █▀▀█ █░░█ █▀▀▄ █▀▀▄ 
▀▀█ █░░ █▄▄▀ █▀▀ █▀▀ █░░█ 　 ▀▀█ █░░█ █░░█ █░░█ █░░█ 
▀▀▀ ▀▀▀ ▀░▀▀ ▀▀▀ ▀▀▀ ▀░░▀ 　 ▀▀▀ ▀▀▀▀ ░▀▀▀ ▀░░▀ ▀▀▀░ 
");
    Console.WriteLine(mensagemDeBoasVindas);
}

void ExibirMenu()
{
    ExibirLogo();
    Console.WriteLine("\nDigite 1 para registrar uma banda");
    Console.WriteLine("Digite 2 para mostras todas as bandas");
    Console.WriteLine("Digite 3 para avaliar uma banda");
    Console.WriteLine("Digite 4 para exibir a média de uma banda");
    Console.WriteLine("Digite -1 para sair");

    Console.Write("\nDigite sua opção: ");
    string opcaoEscolhida = Console.ReadLine()!;
    int opcaoEscolhidaNumerica = int.Parse(opcaoEscolhida);

    switch (opcaoEscolhidaNumerica)
    {
        case 1:
            RegistrarBandas();
            break;
        case 2:
            MostrarBandas();
            break;
        case 3:
            AvaliarBanda();
            break;
        case 4:
            ExibirMedia();
            break;
        case -1:
            Console.WriteLine("Tchauu :)");
            break;
        default:
            Console.WriteLine("Opção Inválida :(");
            break;
    }
}

ExibirMenu();


void RegistrarBandas(){
    Console.Clear();
    Console.WriteLine("Bem vindo ao registro de bandas\n");
    Console.Write("Digite o nome da banda que deseja registrar: ");
    string nomeBanda = Console.ReadLine()!;
    RegistroBandas.Add(nomeBanda, new List<int>());
    Console.WriteLine($"\nA banda {nomeBanda} foi registrada com sucesso!");
    Thread.Sleep(2000);
    Console.Clear() ;

    ExibirMenu();
}

void MostrarBandas()
{
    Console.Clear();
    Console.WriteLine("Mostrando bandas registradas\n");
    //for (int i = 0; i < listaBandas.Count; i++)
    //{
       // Console.WriteLine($"Banda: {listaBandas[i]}");
    //}
    foreach (string banda in RegistroBandas.Keys)
    {
        Console.WriteLine($"Banda: {banda}");
    }
        Console.WriteLine("\nDigite qualquer tecla para voltar ao menu principal");
        Console.ReadKey();
        Console.Clear();
        ExibirMenu();
    
}

void AvaliarBanda()
{
    Console.Clear();
    Console.WriteLine("Bem vindo, Avalie uma banda!");
    Console.Write("\nDigite a banda que deseja avaliar: ");
    string nomeDaBanda = Console.ReadLine()!;
    if (RegistroBandas.ContainsKey(nomeDaBanda))
    {
        Console.Write($"\nQual nota a banda {nomeDaBanda} merece? ");
        int nota = int.Parse(Console.ReadLine()!);
        RegistroBandas[nomeDaBanda].Add(nota);
        Console.WriteLine($"\nA nota {nota} foi atribuida a banda {nomeDaBanda}!");
        Thread.Sleep(3000);
        Console.Clear() ;
        ExibirMenu();
    }
    else
    {
        Console.WriteLine($"\nA banda {nomeDaBanda} nao esta registrada!");
        Console.WriteLine("\nDigite qualquer tecla para voltar ao menu principal!");
        Console.ReadKey();
        Console.Clear();
        ExibirMenu() ;
    }
}
    
   void ExibirMedia()
{
    Console.Clear();
    Console.WriteLine("Bem vindo(a) ao campo de exibição das médias das bandas");
    Console.Write("\nMe diga, qual banda você quer saber a média? ");
    string nomeDaBanda = Console.ReadLine()!;
    
    if (RegistroBandas.ContainsKey(nomeDaBanda))
    {
        double media = RegistroBandas[nomeDaBanda].Average();
        Console.Write($"\n A média da banda {nomeDaBanda} é {media}");
        Thread.Sleep(3000);
        Console.Clear();
        ExibirMenu();
    } else
    {
        Console.WriteLine($"\nA banda {nomeDaBanda} nao esta registrada!");
        Console.WriteLine("\nDigite qualquer tecla para voltar ao menu principal!");
        Console.ReadKey();
        Console.Clear();
        ExibirMenu();
    }

}
