#include <iostream>
#include <string>

using namespace std;
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

// Função para cadastrar as notas de um aluno
void cadastrarNotas(string& nome, float notas[]) {
    cout << "Escreva o nome do aluno:\n ";
    cin >> nome;

    cout << "Escreva as notas do aluno:\n ";
    for (int i = 0; i < 4; ++i) {
        cin >> notas[i];
void cadastrarNotas(char nome[], float notas[]) {
    printf("Escreva o nome do aluno:\n ");
    scanf("%s", nome);

    printf("Escreva as notas do aluno:\n ");
    int i;
    for (i = 0; i < 4; ++i) {
        scanf("%f", &notas[i]);
    }
}

// Função para calcular a média de um aluno e determinar seu status
void calcularMediaEStatus(const string& nome, const float notas[]) {
void calcularMediaEStatus(const char nome[], const float notas[]) {
    float soma = 0;
    for (int i = 0; i < 4; ++i) {
    int i;
    for (i = 0; i < 4; ++i) {
        soma += notas[i];
    }
    float media = soma / 4;
    
    cout << "A media do aluno " << nome << " e " << media << endl;
    

    printf("A media do aluno %s e %.2f\n", nome, media);

    if (media < 4) {
        cout << "O aluno esta reprovado\n" << endl;
        printf("O aluno esta reprovado\n\n");
    } else if (media >= 6) {
        cout << "O aluno esta aprovado\n" << endl;
        printf("O aluno esta aprovado\n\n");
    } else {
        cout << "O aluno esta de recuperacao\n" << endl;
        printf("O aluno esta de recuperacao\n\n");
    }
}

int main() {
    const int NUM_ALUNOS = 5;
    string nomes[NUM_ALUNOS];
    char nomes[NUM_ALUNOS][50];
    float notas[NUM_ALUNOS][4];

    int opcao;
    do {
        cout << "MENU" << endl;
        cout << "1- Cadastro das Notas dos Alunos" << endl;
        cout << "2- Alteracao das Notas" << endl;
        cout << "3- SAIR" << endl;
        cout << "Escolha uma opcao: ";
        cin >> opcao;
        system ("cls");
        printf("MENU\n");
        printf("1- Cadastro das Notas dos Alunos\n");
        printf("2- Alteracao das Notas\n");
        printf("3- SAIR\n");
        printf("Escolha uma opcao: ");
        scanf("%d", &opcao);
        system("cls");

        switch (opcao) {
            case 1:
            	system("cls");
                cout << "CADASTRO DE NOTAS DOS ALUNOS" << endl;
                for (int i = 0; i < NUM_ALUNOS; ++i) {
                system("cls");
                printf("CADASTRO DE NOTAS DOS ALUNOS\n");
                int i;
				for (i = 0; i < NUM_ALUNOS; ++i) {
                    cadastrarNotas(nomes[i], notas[i]);
                    calcularMediaEStatus(nomes[i], notas[i]);
                }
                break;
            case 2:
            	system("cls");
                cout << "ALTERACAO DE NOTAS\n" << endl;
                for (int i = 0; i < NUM_ALUNOS; ++i) {
                system("cls");
                printf("ALTERACAO DE NOTAS\n");
				for (i = 0; i < NUM_ALUNOS; ++i) {
                    cadastrarNotas(nomes[i], notas[i]);
                    calcularMediaEStatus(nomes[i], notas[i]);
                }
                break;
            case 3:
                cout << "Saindo..." << endl;
                printf("Saindo...\n");
                break;
            default:
                cout << "Opcao invalida! Tente novamente.\n" << endl;
                printf("Opcao invalida! Tente novamente.\n\n");
                system("pause");
                system("cls");
        }
