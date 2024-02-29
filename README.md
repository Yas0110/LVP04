//Inicializando um array

#include <iostream>
#include <iomanip>
#include <string>
#include <locale>
#include <stdlib.h> 
using namespace std;



struct dados{
	
	//ESTRURA DE PACOTES DE VARIÁVEOS DE TIPOS DIFERENTES, CADA VARIÁVEL É UM CAMPO DO REGISTRO.
	//Definindo os tipos de dados que agrupam variáveis sob um mesmo tipo de dado.
	
	string nome;
	float n_horas;
	float v_horas;
	float salario;
	string  cpf;
	
};

int main(){
	
	int maxima_de_funcionarios = 5; // quantidade de funcionários para serem solicitados, com limite de 5.
	
	dados funcionario[maxima_de_funcionarios]; // declaração do array
	
	int salario_maior  = 0; // soma
	
	cout << "Insira os dados dos 5 funcionários: " << endl;
	
	for (int i = 0; i < maxima_de_funcionarios; i++){
	    
		cout << "Funcionário " << i+1 << ":" << endl; //contador + 1 para informar o número do funcionarios.
		cout << "Qual o nome do funcionário? "; 
		cin >> funcionario[i].nome; // inserir o valor no array
		cout << "Qual o número do CPF? ";
		cin >> funcionario[i].cpf;
		cout << "Qual o número de horas trabalhadas? ";
		cin >> funcionario[i].n_horas;
		cout << "Qual valor da hora? ";
		cin >> funcionario[i].v_horas;
		
		//calculo do salário dos funcionários
		
		funcionario[i].salario =  funcionario[i].v_horas * funcionario[i].n_horas *;
		
		//condição para o maior salário
		
		if (funcionario[i].salario > funcionario[salario_maior].salario){
			
			salario_maior = i;
			
		}
	}
	cout << "O funcionário com o maior salário é " << funcionario[salario_maior].nome << " que tem o salário " << funcionario[salario_maior].salario << endl;
	return 0;
}
