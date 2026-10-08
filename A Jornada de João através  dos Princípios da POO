using System;

// ABSTRAÇÃO
// Classe abstrata que representa um veículo terrestre
abstract class Veiculo
{
    // ENCAPSULAMENTO
    private string modelo;

    public string Modelo
    {
        get { return modelo; }
        set { modelo = value; }
    }

    public Veiculo(string modelo)
    {
        this.Modelo = modelo;
    }

    // Método que será implementado de forma diferente
    // por cada tipo de veículo
    public abstract void Mover();

    public void ExibirModelo()
    {
        Console.WriteLine("Modelo: " + Modelo);
    }
}

// CLASSE
// CarroJoao é a classe principal dos carros
class CarroJoao : Veiculo
{
    protected int Potencia;

    public CarroJoao(string modelo, int potencia)
        : base(modelo)
    {
        Potencia = potencia;
    }

    public override void Mover()
    {
        Console.WriteLine(Modelo + " está se movendo com seu motor.");
    }

    public void EconomiaCombustivel()
    {
        Console.WriteLine(Modelo + " possui boa economia de combustível.");
    }
}

// HERANÇA
// CarroJoaoSports herda características de CarroJoao
class CarroJoaoSports : CarroJoao
{
    public CarroJoaoSports(string modelo, int potencia)
        : base(modelo, potencia)
    {
    }

    public override void Mover()
    {
        Console.WriteLine(Modelo + " está se movendo rapidamente!");
    }

    public void DesignEsportivo()
    {
        Console.WriteLine(Modelo + " possui um design esportivo.");
    }
}

// HERANÇA
class CarroJoaoSUV : CarroJoao
{
    public CarroJoaoSUV(string modelo, int potencia)
        : base(modelo, potencia)
    {
    }

    public override void Mover()
    {
        Console.WriteLine(Modelo + " está se movendo em diferentes tipos de terreno.");
    }

    public void CapacidadeCarga()
    {
        Console.WriteLine(Modelo + " possui maior capacidade de carga.");
    }
}

// HERANÇA
class CarroJoaoEco : CarroJoao
{
    public CarroJoaoEco(string modelo, int potencia)
        : base(modelo, potencia)
    {
    }

    public override void Mover()
    {
        Console.WriteLine(Modelo + " está se movendo com propulsão elétrica.");
    }

    public void EconomiaEnergia()
    {
        Console.WriteLine(Modelo + " utiliza energia elétrica e reduz o consumo de combustível.");
    }
}

// Outros veículos terrestres

class OnibusJoao : Veiculo
{
    public OnibusJoao(string modelo)
        : base(modelo)
    {
    }

    public override void Mover()
    {
        Console.WriteLine(Modelo + " está transportando passageiros.");
    }
}

class CaminhaoJoao : Veiculo
{
    public CaminhaoJoao(string modelo)
        : base(modelo)
    {
    }

    public override void Mover()
    {
        Console.WriteLine(Modelo + " está transportando cargas.");
    }
}

class MotoJoao : Veiculo
{
    public MotoJoao(string modelo)
        : base(modelo)
    {
    }

    public override void Mover()
    {
        Console.WriteLine(Modelo + " está se movendo rapidamente pelas ruas.");
    }
}

// PROGRAMA PRINCIPAL
class Program
{
    static void Main(string[] args)
    {
        Console.WriteLine("====================================");
        Console.WriteLine("       PROJETO CARRO JOÃO");
        Console.WriteLine("====================================\n");

        // OBJETOS
        CarroJoao carro = new CarroJoao("CarroJoao", 120);
        CarroJoaoSports sports = new CarroJoaoSports("CarroJoao Sports", 250);
        CarroJoaoSUV suv = new CarroJoaoSUV("CarroJoao SUV", 180);
        CarroJoaoEco eco = new CarroJoaoEco("CarroJoao Eco", 150);

        // Outros objetos
        OnibusJoao onibus = new OnibusJoao("OnibusJoao");
        CaminhaoJoao caminhao = new CaminhaoJoao("CaminhaoJoao");
        MotoJoao moto = new MotoJoao("MotoJoao");

        // CARRO ORIGINAL
        Console.WriteLine("--- Carro original ---");
        carro.ExibirModelo();
        carro.Mover();
        carro.EconomiaCombustivel();

        Console.WriteLine();

        // CARRO SPORTS
        Console.WriteLine("--- Carro esportivo ---");
        sports.ExibirModelo();
        sports.Mover();
        sports.DesignEsportivo();

        Console.WriteLine();

        // SUV
        Console.WriteLine("--- SUV ---");
        suv.ExibirModelo();
        suv.Mover();
        suv.CapacidadeCarga();

        Console.WriteLine();

        // CARRO ELÉTRICO
        Console.WriteLine("--- Carro Eco ---");
        eco.ExibirModelo();
        eco.Mover();
        eco.EconomiaEnergia();

        Console.WriteLine();

        // POLIMORFISMO
        Console.WriteLine("--- Polimorfismo ---");

        Veiculo[] veiculos =
        {
            carro,
            sports,
            suv,
            eco,
            onibus,
            caminhao,
            moto
        };

        foreach (Veiculo veiculo in veiculos)
        {
            veiculo.Mover();
        }

        Console.WriteLine();

        Console.WriteLine("Todos os veículos foram criados com sucesso!");

        Console.ReadKey();
    }
}
