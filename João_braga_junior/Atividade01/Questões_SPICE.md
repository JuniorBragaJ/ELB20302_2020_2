__Respostas da questão 5A do trabalho de ELB__


1) O que é netlist?
Podendo ser criado manualmente, netlist é um arquivo de texto, que interpreta a linguagem de descrição de um circuito.
	

2) Como descrever o netlist de um circuito?
Primeiramente deve-se colocar o título como primeiro parâmetro digitando um * antes do que deseja escrever, logo após será necessário declarar os componentes usados no circuito. Para sabermos onde o componente está conectado usamos números inteiros e maiores ou iguais a zero para definir cada nó do circuito, e por último declaramos o valor do componente. 
Exemplo:
     __R1 0 2 80__=Resistor R1 está conectado entre os nós 0 e 2 com valor de 80ohms

	3) Como é representado cada um dos componentes?
  https://lh3.googleusercontent.com/pw/ACtC-3fdahxroSSt-ttTfHjeRodu_SPeKTIWmU8r5puokumM87_sn__1jWN3sf7XmPLJybVi9303_d9e_9mVKnk4KMST2ldNkDTbL4uOZvFUgdoRevih8T69cPRVV61OFdq_1Nvhi861ArOq327EOGjOsdJp=w510-h352-no?authuser=0
	

	4) O que é o “LABEL” de um nó e qual a vantagem de usar o mesmo? 
È utilizado para identificar mais facilmente ponto específicos do circuito, fazendo assim com que a análise e até uma possível alteração seja feita de forma mais rápida e sucinta.


	5) Quais os componentes básicos implementados no SPICE? (resistor, capacitor etc)
Resistores (R), Capacitores (C), Indutores (L), Diodo (D), Mosfet (M), Fonte de Tensão independente (V) e Fonte de corrente independente (I).

	

6) O que é um “SUBCKT”? Faça um exemplo. 
é uma declaração usada para definir um sub-circuito. Exemplo:
	
.SUBCKT NOME N1 N2 N3…

	Declaração dos elementos
	.
	.
	.ENDS SUBNAME



	7) Como incluir novos modelos de componentes em um simulador SPICE?
Através do menu Ferramentas > Biblioteca de componentes (Tools > Component Library). Nessa biblioteca constam transistores, diodos, LED’s, AMPOP’s, dentre outros componentes comerciais comumente usados em projetos eletrônicos. 








__Respostas da questão 5B do trabalho de ELB__

1) O que é simulação transiente (.trans)? Quando usar?
A Análise Transiente permite determinar a resposta do circuito em função de sinais variáveis no domínio do tempo. O comportamento no tempo “zero” é obtido pela Análise de polarização DC; portanto esta será sempre realizada antes da Análise Transiente, mesmo que não tenha sido solicitada.

	2) O que é simulação “ DC operating point” (.op)? Quando usar?
Esta declaração instrui o spice a calcular os pontos de operação CC:  tensão no nós, corrente em cada fonte de tensão e ponto de operação para cada elemento. 

	3) Quando usar .trans ou .op no SPICE?
