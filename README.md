#include<bits/stdc++.h>
using namespace std;

float CalcularSalario(float salario);

int main(){
	
	float salario;
	
	cout<<"Ingrese salario: ";
	cin>>salario;
	
	cout<<"Nuevo salario: "<<CalcularSalario(salario)<<" pesos"<<endl;
	
	cout<<"Gano "<<CalcularSalario(salario)-salario<<" pesos"<<endl;
	cout<<"Su salario aumento: "<<((CalcularSalario(salario)-salario)*100)/CalcularSalario(salario)<<" %"<<endl;
	
	return 0;
}

float CalcularSalario(float salario){
	
	float nsalario;
	
		if(salario <= 400){
			nsalario = salario + salario*0.15;
		}
		if(salario > 400 && salario <= 800){
			nsalario = salario + salario*0.12;
		}
		if(salario > 800 && salario <= 1200){
			nsalario = salario + salario*0.10;
		}
		if(salario > 1200 && salario <= 2000){
			nsalario = salario + salario*0.07;
		}
		if(salario > 2000){
			nsalario = salario + salario*0.04;
		}
	
	return nsalario;
}
