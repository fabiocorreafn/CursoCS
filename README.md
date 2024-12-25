# CursoCS
Repositório para registro dos exercícios do curso de C#

// 1. Criar um dicionário que represente um aluno, com uma lista de notas, e mostre a média de suas notas na tela.

// ---- NOTAS E MÉDIAS DE ALUNOS ----
Dictionary<string, Dictionary<string, List<double>>> alunos = new Dictionary<string, Dictionary<string, List<double>>>();

alunos.Add("Fábio", new Dictionary<string, List<double>>
{
    {"C#", new List<double> { 9, 10, 10 } },
    {"Python", new List<double> {10, 10, 9.5} }
});

alunos.Add("Gézica", new Dictionary<string, List<double>>
{
    {"C#", new List<double> { 8, 6, 7 } },
    {"Python", new List<double> {9, 9, 9.8} }
});

foreach (var aluno in alunos.Keys)
{
    Console.WriteLine($"Aluno(a): {aluno}");
    Console.WriteLine($"Médias:");
    foreach (var materia in alunos[aluno].Keys)
    {
        double media = alunos[aluno][materia].Average();
        Console.WriteLine($"    > {materia}: {media:F2}");
    }
    Console.WriteLine();
}
