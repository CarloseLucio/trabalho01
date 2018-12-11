# TRABALHO 01:  Projeto Reconhecimento Facial na Escola 
Trabalho desenvolvido durante a disciplina de Banco de Dados do Integrado

# Sumário

### 1. COMPONENTES<br>
Integrantes do grupo<br>
Lúcio Ribeiro Dos Santos : luciorbeio@gmail.com<br>
Carlos Breno Norato Rosa : cb.californacation@gmail.com <br>
...

### 2.INTRODUÇÃO E MOTIVAÇAO<br>
Este documento contém a especificação do projeto do Projeto Reconhecimento Facial na Escola. 
<br> O projeto realizado tem como intuito facilitar o trabalho dos servidores que trabalham na área da educação, auxliando na verificação da presença dos alunos através do reconhecimento facial<br>

>Como Alunos do Instituto Federal do Espírito Santo, temos contato todos os dias com o ambiente escolar, e pudemos perceber que há algumas situações na escola, que com nosso conhecimento com programação e bancos de dados poderiamos auxiliar e otimizar isso, um desses que percebemos foi a chamada que o professor faz. Ocorre muito na sala de aula dos alunos chegarem atrasado alguns minutos e os professores acabam perdendo certo tempo esperando todos chegarem para fazer a chamada, com isso, criamos a Relavabor Company que é a nossa empresa que tem o intuito de auxiliar com a tecnologia o ambiente escolar. Pensamos em vários metodos de ajudar nesse situação e chegamos a conclusão que seria um otimo investimento a utilização de reconhecimento facial para fazer a chamada para os professores. Nosso projeto é a instalação de sensores na porta e quando os estudantes entrarem na sala já seria reconhecido quem é o aluno,a aula, entre outros dados.Criaremos também um site que conterá todas as informações captadas pelo sensor e mais certas coisas como notas,atividades,historico presencial, etc. Pensamos que a educação é o futuro e com a tecnologia só  tende a melhorar.  

### 3.MINI-MUNDO Novo<br>

Descrição textual das regras de negócio definidas como um  subconjunto do mundo real 
cujos elementos são propriedades que desejamos incluir, processar, armazenar, 
gerenciar, atualizar, e que descrevem a proposta/solução a ser desenvolvida.

> O Sistema proposto para a "Relevabor Company" conterá as informações aqui detalhados. O sistema será formado pelo site e pelo sensor da porta que será conectado com o sistema. Cada professor irá ter seu cadastro online com seu email,nome,matrícula e uma senha, o educador possuirá algumas opções sobre o que visualizar ou o que criar.No nosso primeira sistema cada professor só poderá possuir uma única materia mas isso é algo que pretendemos mudar em uma nova versão.O professor poderá acessar a opção criar, onde ele poderá cadastrar um aluno, uma turma,uma atividade ou uma nota. Para cadastrar um estudante ele colocará o nome a matrícula, o email, o sexo, o cpf, a data de nascimento e uma foto para o sensor fazer o reconhecimento. Para cadastrar uma turma precisará de colocar o nome, o ano que foi criada essa turma, o turno e adicionar os alunos através do nomes ou matrícula. Para criar uma atividade ele precisará colocar o nome da atividade, o tipo caso for uma prova ou só uma atividade, a data que ela ocorrerá, o horario, a turma e quantos pontos valerá. Para adicionar notas o usuário colocará a turma, selecionará qual foi a atividade criada, digitara o nome do aluno e escreverá a nota. 
    No sistema proposto o Professor também poderá visualizar certas coisas como o historico presencial dos alunos que será feito diretamente pelo sensor, o usuário só precisará colocar a data,turma e a aula, que irá mostrar todos os alunos e se eles chegaram atrasados ou faltaram.Também será possivel ver um resumo de cada aluno na opção alunos da pagina inicial, nessa opção o usuário colocará o nome do aluno e será possivel ver a foto do estudante junto com o número total de faltas e presenças em todas materias e também a turma a qual ele pertence. Outra opção que o educador terá é o boletim onde ele só selecionará a turma e a matéria e será possivel ver a nota de todos os alunos em ordem alfabética. E a ultima opção será o calendario de atividades onde o professor poderá ver pela data o que já está marcado para uma determinada turma e assim não correr o risco de marcar outra coisa no mesmo horario ou dia.Também será armazenado o endereço de todas as pessoas que fazem parte do endereço com o pais,estado,cidade e bairro.

### 4.RASCUNHOS BÁSICOS DA INTERFACE (MOCKUPS)<br>


![Alt text](https://github.com/discipbd1/trab01/blob/master/balsamiq.png?raw=true "Title")
![Arquivo PDF do Protótipo Balsamiq feito para Empresa Relevabor Company](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/arquivos/ah.pdf?raw=true "Relevabor Company")


#### 4.1 TABELA DE DADOS DO SISTEMA:
    
    https://cdn.discordapp.com/attachments/383721330106957838/450829572360110081/gnt.png
    
    
    O sistema proposto poderá fornecer esses tipos de relatórios e informações : 
    
    1) Os dados de todos os alunos(nome,cpf,endereço,sexo)
    2) O registro de entrada e saída dos alunos
    3) Notas em geral de cada aluno
    4) A qual turma o aluno pertence e quaid matérias ele tem
    5) Calendário de atividades, horário das aulas e de eventos da escola

>## Marco de Entrega 01 em: (24/03/2018)<br>

### 5.MODELO CONCEITUAL<br>
        
![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/conc.png?raw=true "Modelo Conceitual")
    
        
    
#### 5.1 Validação do Modelo Conceitual
    [Grupo01]: [Leonardo Fáfá e Rafael Rodrigues]
    [Grupo02]: [Thamiris Moreira e Lia Casati]
    
    
## Marco de Entrega 01 em: (20/04/2018)<br>

#### 5.2 DECISÕES DE PROJETO
    
         

#### 5.3 DESCRIÇÃO DOS DADOS 
    Aluno : Tabela que recebe os atributos dos alunos
   
    	Matricula : Colocamos o campo matricula pelo fato de cada participante (professores e alunos) possuir uma matricula 
                      diferente de qualquer outra pessoa do sistema,sendo assim,é muito bom para usar de chave primária. 
                      
    	Nome_aluno : Esse atributo é utilizado para a identificação do aluno para amostra de notas ou da pagina que mostra
                        todos os dados dos alunos,pois para o usuário é mais válido lembrar o nome do que lembra a matricúla. 
          
    	dat_nasc : Outro dado utilizado para a identificação do aluno. 
    
    Turma : tabela que receberá os atributos da turma
    
    	Num_Turma : o número da turma é de grande utilidade,pois é quue certamente será diferente de turma para turma,
                        sendo assim, muito utíl para ser a chave primária da objeto turma.
                        
    	Nome_turma : O nome da turma é a principal forma para o usuário poder a identificar, é util para o usuário ver o que                              cada turma possui de atividade,ou marcar uma,entre outras coisas.   
          
    	Data_Criacao : É o ano ínicial da turma e é um outro atributo utilizado para especificar a turma. 
        
    Professor : Tabela que recebe os atributos dos professores 
   	
		Matricula : Colocamos o campo matricula pelo fato de cada participante (professores e alunos) possuir uma matricula 
                      diferente de qualquer outra pessoa do sistema,sendo assim,é muito bom para usar de chave primária. 
		      
    	Nome_prof : atributo para identificação do professor,é recebido no proprio cadastro. 
          
    	Cpf_prof : outro dado para especificação do professor
          
     Avaliacao : Tabela que recebe os atributos daas avaliações 
     
    	Num_avalicao :  Identificador e chave primaria da avaliação.
          
    	Nome_avalicao : Especificação se é uma prova ou uma atividade. 
          
    	Dat_Avalicao : Data que acontecerá a atividade. 
          
    	Valor_avalicao : valor da avaliação. 
          
    	nota : nota que o aluno recebeu na avaliação. 

>## Marco de Entrega 01 em: (12/05/2018)<br>
### 6	MODELO LÓGICO<br>

![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/Sem%20t%C3%ADtulo.png?raw=true "Modelo Logico")



### 7	MODELO FÍSICO<br>
      

		/* Lógico_1: */

	CREATE TABLE aluno (
	    matricula varChar(100),
	    FK_pessoa_cpf varchar(100),
	    FK_turma_numero_turma varChar(100),
	    PRIMARY KEY (matricula, FK_pessoa_cpf)
	);

	CREATE TABLE turma (
	    numero_turma varChar(100) PRIMARY KEY,
	    nome_turma varChar(100)
	);

	CREATE TABLE professor (
	    cod_professor varChar(100),
	    FK_pessoa_cpf varchar(100),
	    PRIMARY KEY (cod_professor, FK_pessoa_cpf)
	);

	CREATE TABLE avaliacao (
	    valor_avaliacao float,
	    data_avaliacao date,
	    numero_avaliacao int PRIMARY KEY,
	    nome_avaliacao varChar(100)
	);

	CREATE TABLE endereco_ (
	    numero int,
	    codigo varChar(100) PRIMARY KEY,
	    FK_complemento_cod_complemento int,
	    FK_bairro__numero_bairro int
	);

	CREATE TABLE bairro_ (
	    nome_bairro varChar(100),
	    numero_bairro int PRIMARY KEY,
	    FK_cidade_numero_cidade int
	);

	CREATE TABLE cidade (
	    nome_cidade varChar(100),
	    numero_cidade int PRIMARY KEY,
	    FK_estado_numero_estado int
	);

	CREATE TABLE pais (
	    nome_pais varChar(100),
	    numero_pais varChar(100) PRIMARY KEY
	);

	CREATE TABLE estado (
	    nome_estado varChar(100),
	    numero_estado int PRIMARY KEY,
	    FK_pais_numero_pais varChar(100)
	);

	CREATE TABLE complemento (
	    cod_complemento int PRIMARY KEY,
	    dec_complemento varChar(100)
	);

	CREATE TABLE logadouro (
	    cod Serial PRIMARY KEY,
	    tipo varChar(100),
	    nome varChar(200),
	    FK_endereco__codigo varChar(100)
	);

	CREATE TABLE Ano (
	    cod varChar(200) PRIMARY KEY,
	    descricao varChar(100),
	    FK_turma_numero_turma varChar(100)
	);

	CREATE TABLE pessoa (
	    nome varchar(100),
	    cpf varchar(100) PRIMARY KEY,
	    data_de_nascimento date,
	    sexo char,
	    FK_endereco__codigo varChar(100)
	);

	CREATE TABLE materia (
	    cod int PRIMARY KEY,
	    descricao varChar(100)
	);

	CREATE TABLE leciona (
	    FK_turma_numero_turma varChar(100),
	    FK_professor_cod_professor varChar(100),
	    FK_professor_FK_pessoa_cpf varchar(100)
	);

	CREATE TABLE aplica (
	    FK_avaliacao_numero_avaliacao int,
	    FK_professor_cod_professor varChar(100),
	    FK_professor_FK_pessoa_cpf varchar(100)
	);

	CREATE TABLE faz (
	    FK_aluno_matricula varChar(100),
	    FK_aluno_FK_pessoa_cpf varchar(100),
	    FK_avaliacao_numero_avaliacao int,
	    nota float
	);

	CREATE TABLE ensina (
	    FK_professor_cod_professor varChar(100),
	    FK_professor_FK_pessoa_cpf varchar(100),
	    FK_materia_cod int
	);

	CREATE TABLE frequenta (
	    FK_aluno_matricula varChar(100),
	    FK_aluno_FK_pessoa_cpf varchar(100),
	    FK_materia_cod int,
	    data date,
	    presenca char
	);

	ALTER TABLE aluno ADD CONSTRAINT FK_aluno_1
	    FOREIGN KEY (FK_pessoa_cpf)
	    REFERENCES pessoa (cpf)
	    ON DELETE CASCADE ON UPDATE CASCADE;

	ALTER TABLE aluno ADD CONSTRAINT FK_aluno_2
	    FOREIGN KEY (FK_turma_numero_turma)
	    REFERENCES turma (numero_turma)
	    ON DELETE RESTRICT ON UPDATE RESTRICT;

	ALTER TABLE professor ADD CONSTRAINT FK_professor_1
	    FOREIGN KEY (FK_pessoa_cpf)
	    REFERENCES pessoa (cpf)
	    ON DELETE CASCADE ON UPDATE CASCADE;

	ALTER TABLE endereco_ ADD CONSTRAINT FK_endereco__1
	    FOREIGN KEY (FK_complemento_cod_complemento)
	    REFERENCES complemento (cod_complemento)
	    ON DELETE CASCADE ON UPDATE CASCADE;

	ALTER TABLE endereco_ ADD CONSTRAINT FK_endereco__2
	    FOREIGN KEY (FK_bairro__numero_bairro)
	    REFERENCES bairro_ (numero_bairro)
	    ON DELETE RESTRICT ON UPDATE RESTRICT;

	ALTER TABLE bairro_ ADD CONSTRAINT FK_bairro__1
	    FOREIGN KEY (FK_cidade_numero_cidade)
	    REFERENCES cidade (numero_cidade)
	    ON DELETE RESTRICT ON UPDATE RESTRICT;

	ALTER TABLE cidade ADD CONSTRAINT FK_cidade_1
	    FOREIGN KEY (FK_estado_numero_estado)
	    REFERENCES estado (numero_estado)
	    ON DELETE RESTRICT ON UPDATE RESTRICT;

	ALTER TABLE estado ADD CONSTRAINT FK_estado_1
	    FOREIGN KEY (FK_pais_numero_pais)
	    REFERENCES pais (numero_pais)
	    ON DELETE RESTRICT ON UPDATE RESTRICT;

	ALTER TABLE logadouro ADD CONSTRAINT FK_logadouro_1
	    FOREIGN KEY (FK_endereco__codigo)
	    REFERENCES endereco_ (codigo)
	    ON DELETE RESTRICT ON UPDATE RESTRICT;

	ALTER TABLE Ano ADD CONSTRAINT FK_Ano_1
	    FOREIGN KEY (FK_turma_numero_turma)
	    REFERENCES turma (numero_turma)
	    ON DELETE RESTRICT ON UPDATE RESTRICT;

	ALTER TABLE pessoa ADD CONSTRAINT FK_pessoa_1
	    FOREIGN KEY (FK_endereco__codigo)
	    REFERENCES endereco_ (codigo)
	    ON DELETE RESTRICT ON UPDATE RESTRICT;

	ALTER TABLE leciona ADD CONSTRAINT FK_leciona_0
	    FOREIGN KEY (FK_turma_numero_turma)
	    REFERENCES turma (numero_turma)
	    ON DELETE RESTRICT ON UPDATE RESTRICT;

	ALTER TABLE leciona ADD CONSTRAINT FK_leciona_1
	    FOREIGN KEY (FK_professor_cod_professor, FK_professor_FK_pessoa_cpf)
	    REFERENCES professor (cod_professor, FK_pessoa_cpf)
	    ON DELETE RESTRICT ON UPDATE RESTRICT;

	ALTER TABLE aplica ADD CONSTRAINT FK_aplica_0
	    FOREIGN KEY (FK_avaliacao_numero_avaliacao)
	    REFERENCES avaliacao (numero_avaliacao)
	    ON DELETE RESTRICT ON UPDATE RESTRICT;

	ALTER TABLE aplica ADD CONSTRAINT FK_aplica_1
	    FOREIGN KEY (FK_professor_cod_professor, FK_professor_FK_pessoa_cpf)
	    REFERENCES professor (cod_professor, FK_pessoa_cpf)
	    ON DELETE RESTRICT ON UPDATE RESTRICT;

	ALTER TABLE faz ADD CONSTRAINT FK_faz_0
	    FOREIGN KEY (FK_aluno_matricula, FK_aluno_FK_pessoa_cpf)
	    REFERENCES aluno (matricula, FK_pessoa_cpf)
	    ON DELETE RESTRICT ON UPDATE RESTRICT;

	ALTER TABLE faz ADD CONSTRAINT FK_faz_1
	    FOREIGN KEY (FK_avaliacao_numero_avaliacao)
	    REFERENCES avaliacao (numero_avaliacao)
	    ON DELETE RESTRICT ON UPDATE RESTRICT;

	ALTER TABLE ensina ADD CONSTRAINT FK_ensina_0
	    FOREIGN KEY (FK_professor_cod_professor, FK_professor_FK_pessoa_cpf)
	    REFERENCES professor (cod_professor, FK_pessoa_cpf)
	    ON DELETE SET NULL ON UPDATE CASCADE;

	ALTER TABLE ensina ADD CONSTRAINT FK_ensina_1
	    FOREIGN KEY (FK_materia_cod)
	    REFERENCES materia (cod)
	    ON DELETE SET NULL ON UPDATE CASCADE;

	ALTER TABLE frequenta ADD CONSTRAINT FK_frequenta_0
	    FOREIGN KEY (FK_aluno_matricula, FK_aluno_FK_pessoa_cpf)
	    REFERENCES aluno (matricula, FK_pessoa_cpf)
	    ON DELETE RESTRICT ON UPDATE RESTRICT;

	ALTER TABLE frequenta ADD CONSTRAINT FK_frequenta_1
	    FOREIGN KEY (FK_materia_cod)
	    REFERENCES materia (cod)
	    ON DELETE RESTRICT ON UPDATE RESTRICT;
        
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
#### 8.1 DETALHAMENTO DAS INFORMAÇÕES
         

		Insert into complemento(cod_complemento,dec_complemento)
			values('01','casa'),
			('02','condominio'),    		
			('03','apartamento');



		Insert into pais(nome_pais,numero_pais)
			values('BR',00),
			('USA',01),  
				('FRA',02),  
				('CHI',03),  
				('ARG',04);

		Insert into estado(nome_estado,numero_estado,fk_pais_numero_pais)
			values('ES',00,00),
				('RJ',01,00),  
				('SP',02,00),  
				('NY',03,01),  
				('RO',04,00);

		   Insert into cidade(nome_cidade,numero_cidade ,fk_estado_numero_estado)
			values('Serra',00,00),
				('Vitoria',01,00),  
				('Rio de Janeiro',02,01),  
				('São Paulo',03,02),  
				('Cariacica',04,00),
				('Vila Velha',05,00);


		   Insert into bairro_(nome_bairro,numero_bairro ,fk_cidade_numero_cidade)
			values('nova almeida',00,00),
			('jardim da penha',01,01),  
				('laranjeiras',02,00),  
				('Cobilândia',03,05),  
				('Jardim Camburi',04,01);	




		   Insert into endereco_(numero,codigo,fk_complemento_cod_complemento,fk_bairro__numero_bairro)
				values(01,'1111',01,00),
				(02,'2222',01,01),  
				(03,'3333',02,02),  
				(04,'4444',03,03),  
				(05,'5555',02,04);	


		 Insert Into Turma( nome_turma, numero_turma)
			   Values ('A', '00'),
			   ('B', '01'),
			   ('C', '02'),
			   ('D', '03'),
			   ('X', '04');

		Insert Into pessoa (cpf,nome,data_de_nascimento,fk_endereco__codigo,sexo)
				Values ('11111111', 'Guilherme Bork','12-12-2002','1111','M'),
				('2222222222', 'Fabio', '09-09-2002','3333','M'),
				('3333333333', 'Daniel', '07-08-2001','2222','M'),
				('4444444444', 'Vanessa', '08-09-2003','3333','F'),
				('5555555555', 'Kamila', '02-09-2000','4444','F'),
				('6666666666', 'Paulo', '17-09-1985','5555','M'),
				('7777777777', 'Jeferson', '20-06-1976','5555','M');



		Insert into logadouro(cod,tipo,nome,fk_endereco__codigo)
		values(01,'Avenida','belo horizonte','1111'),
		(02,'Avenida','Dante Michelini','5555'),
		(03,'Rua' ,'Albérico Bitencourt','4444'),
		(04,'Rua','Boulevard Antilhas','3333'),
		(05,'Avenida','Abido Saad','2222');

		Insert Into aluno (matricula, fk_pessoa_cpf, fk_turma_numero_turma)
		Values ('00000', '11111111','00'),
		('11111', '2222222222', '00'),
		('22222', '3333333333', '02'),
		('33333', '4444444444', '03'),
		('55555', '5555555555', '01');



		Insert Into professor(cod_professor, fk_pessoa_cpf)
		Values ('01111', '6666666666'),
		('02222', '7777777777');



		Insert Into avaliacao(Nome_avaliacao, data_avaliacao, Valor_avaliacao,numero_avaliacao)
		Values ('prova1', '12-12-2018', 10,1),
		('Trab1', '12-12-2018', 25,2),
		('Prova2', '13-12-2018', 10,3),
		('Trab2', '13-12-2018', 5,4),
		('Trab3', '13-12-2018', 10,5);


		Insert Into aplica(fk_avaliacao_numero_avaliacao,fk_professor_cod_professor,fk_professor_fk_pessoa_cpf)
		Values (1,'01111','6666666666'),
		(2,'01111','6666666666'),
		(3,'01111','6666666666'),
		(4,'02222','7777777777'),
		(5,'02222','7777777777');




		Insert into ano(cod,descricao,FK_turma_numero_turma)
		values(01,'2013','00'),
		(02,'2014','01'),
		(03,'2015','02'),
		(04,'2016','03'),
		(05,'2017','04');


		Insert Into ensina(fk_professor_cod_professor,fk_professor_fk_pessoa_cpf,fk_materia_cod)
		Values ('01111','6666666666',1),
		('02222','7777777777',2),



		Insert Into materia(cod,descricao)
		Values (1,'Matematica'),
		(2,'Historia'),


		Insert into leciona(fk_turma_numero_turma,fk_professor_cod_professor ,fk_professor_fk_pessoa_cpf)
			values('00','01111','6666666666'),
				('01','01111','6666666666'),  
				('02','01111','6666666666'),  
				('03','02222','7777777777'),  
				('04','02222','7777777777');	

		Insert into faz(fk_aluno_matricula,fk_aluno_fk_pessoa_cpf ,fk_avaliacao_numero_avaliacao,nota)
			values('00000','11111111','1','7'),
				('11111','2222222222','1','8'),  
				('22222','3333333333','1','10'),  
				('33333','4444444444','1','5.5'),  
				('55555','5555555555','1','6.5');	


		insert into frequenta(fk_aluno_matricula,fk_aluno_fk_pessoa_cpf,fk_materia_cod,data,presenca)
		values('00000','11111111',1,'03-03-2017','.'),
		('11111','2222222222',1,'03-03-2017','.'),
		('22222','3333333333',1,'03-03-2017','.'),
		('33333','4444444444',1,'03-03-2017','.'),
		('55555','5555555555',1,'03-03-2017','F');



#### 8.2 INCLUSÃO DO SCRIPT PARA CRIAÇÃO DE TABELA E INSERÇÃO DOS DADOS
        
		

		CREATE TABLE aluno (
		    matricula varChar(100),
		    FK_pessoa_cpf varchar(100),
		    FK_turma_numero_turma varChar(100),
		    PRIMARY KEY (matricula, FK_pessoa_cpf)
		);

		CREATE TABLE turma (
		    numero_turma varChar(100) PRIMARY KEY,
		    nome_turma varChar(100)
		);

		CREATE TABLE professor (
		    cod_professor varChar(100),
		    FK_pessoa_cpf varchar(100),
		    PRIMARY KEY (cod_professor, FK_pessoa_cpf)
		);

		CREATE TABLE avaliacao (
		    valor_avaliacao float,
		    data_avaliacao date,
		    numero_avaliacao int PRIMARY KEY,
		    nome_avaliacao varChar(100)
		);

		CREATE TABLE endereco_ (
		    numero int,
		    codigo varChar(100) PRIMARY KEY,
		    FK_complemento_cod_complemento int,
		    FK_bairro__numero_bairro int
		);

		CREATE TABLE bairro_ (
		    nome_bairro varChar(100),
		    numero_bairro int PRIMARY KEY,
		    FK_cidade_numero_cidade int
		);

		CREATE TABLE cidade (
		    nome_cidade varChar(100),
		    numero_cidade int PRIMARY KEY,
		    FK_estado_numero_estado int
		);

		CREATE TABLE pais (
		    nome_pais varChar(100),
		    numero_pais varChar(100) PRIMARY KEY
		);

		CREATE TABLE estado (
		    nome_estado varChar(100),
		    numero_estado int PRIMARY KEY,
		    FK_pais_numero_pais varChar(100)
		);

		CREATE TABLE complemento (
		    cod_complemento int PRIMARY KEY,
		    dec_complemento varChar(100)
		);

		CREATE TABLE logadouro (
		    cod Serial PRIMARY KEY,
		    tipo varChar(100),
		    nome varChar(200),
		    FK_endereco__codigo varChar(100)
		);

		CREATE TABLE Ano (
		    cod varChar(200) PRIMARY KEY,
		    descricao varChar(100),
		    FK_turma_numero_turma varChar(100)
		);

		CREATE TABLE pessoa (
		    nome varchar(100),
		    cpf varchar(100) PRIMARY KEY,
		    data_de_nascimento date,
		    sexo char,
		    FK_endereco__codigo varChar(100)
		);

		CREATE TABLE materia (
		    cod int PRIMARY KEY,
		    descricao varChar(100)
		);

		CREATE TABLE leciona (
		    FK_turma_numero_turma varChar(100),
		    FK_professor_cod_professor varChar(100),
		    FK_professor_FK_pessoa_cpf varchar(100)
		);

		CREATE TABLE aplica (
		    FK_avaliacao_numero_avaliacao int,
		    FK_professor_cod_professor varChar(100),
		    FK_professor_FK_pessoa_cpf varchar(100)
		);

		CREATE TABLE faz (
		    FK_aluno_matricula varChar(100),
		    FK_aluno_FK_pessoa_cpf varchar(100),
		    FK_avaliacao_numero_avaliacao int,
		    nota float
		);

		CREATE TABLE ensina (
		    FK_professor_cod_professor varChar(100),
		    FK_professor_FK_pessoa_cpf varchar(100),
		    FK_materia_cod int
		);

		CREATE TABLE frequenta (
		    FK_aluno_matricula varChar(100),
		    FK_aluno_FK_pessoa_cpf varchar(100),
		    FK_materia_cod int,
		    data date,
		    presenca char
		);

		ALTER TABLE aluno ADD CONSTRAINT FK_aluno_1
		    FOREIGN KEY (FK_pessoa_cpf)
		    REFERENCES pessoa (cpf)
		    ON DELETE CASCADE ON UPDATE CASCADE;

		ALTER TABLE aluno ADD CONSTRAINT FK_aluno_2
		    FOREIGN KEY (FK_turma_numero_turma)
		    REFERENCES turma (numero_turma)
		    ON DELETE RESTRICT ON UPDATE RESTRICT;

		ALTER TABLE professor ADD CONSTRAINT FK_professor_1
		    FOREIGN KEY (FK_pessoa_cpf)
		    REFERENCES pessoa (cpf)
		    ON DELETE CASCADE ON UPDATE CASCADE;

		ALTER TABLE endereco_ ADD CONSTRAINT FK_endereco__1
		    FOREIGN KEY (FK_complemento_cod_complemento)
		    REFERENCES complemento (cod_complemento)
		    ON DELETE CASCADE ON UPDATE CASCADE;

		ALTER TABLE endereco_ ADD CONSTRAINT FK_endereco__2
		    FOREIGN KEY (FK_bairro__numero_bairro)
		    REFERENCES bairro_ (numero_bairro)
		    ON DELETE RESTRICT ON UPDATE RESTRICT;

		ALTER TABLE bairro_ ADD CONSTRAINT FK_bairro__1
		    FOREIGN KEY (FK_cidade_numero_cidade)
		    REFERENCES cidade (numero_cidade)
		    ON DELETE RESTRICT ON UPDATE RESTRICT;

		ALTER TABLE cidade ADD CONSTRAINT FK_cidade_1
		    FOREIGN KEY (FK_estado_numero_estado)
		    REFERENCES estado (numero_estado)
		    ON DELETE RESTRICT ON UPDATE RESTRICT;

		ALTER TABLE estado ADD CONSTRAINT FK_estado_1
		    FOREIGN KEY (FK_pais_numero_pais)
		    REFERENCES pais (numero_pais)
		    ON DELETE RESTRICT ON UPDATE RESTRICT;

		ALTER TABLE logadouro ADD CONSTRAINT FK_logadouro_1
		    FOREIGN KEY (FK_endereco__codigo)
		    REFERENCES endereco_ (codigo)
		    ON DELETE RESTRICT ON UPDATE RESTRICT;

		ALTER TABLE Ano ADD CONSTRAINT FK_Ano_1
		    FOREIGN KEY (FK_turma_numero_turma)
		    REFERENCES turma (numero_turma)
		    ON DELETE RESTRICT ON UPDATE RESTRICT;

		ALTER TABLE pessoa ADD CONSTRAINT FK_pessoa_1
		    FOREIGN KEY (FK_endereco__codigo)
		    REFERENCES endereco_ (codigo)
		    ON DELETE RESTRICT ON UPDATE RESTRICT;

		ALTER TABLE leciona ADD CONSTRAINT FK_leciona_0
		    FOREIGN KEY (FK_turma_numero_turma)
		    REFERENCES turma (numero_turma)
		    ON DELETE RESTRICT ON UPDATE RESTRICT;

		ALTER TABLE leciona ADD CONSTRAINT FK_leciona_1
		    FOREIGN KEY (FK_professor_cod_professor, FK_professor_FK_pessoa_cpf)
		    REFERENCES professor (cod_professor, FK_pessoa_cpf)
		    ON DELETE RESTRICT ON UPDATE RESTRICT;

		ALTER TABLE aplica ADD CONSTRAINT FK_aplica_0
		    FOREIGN KEY (FK_avaliacao_numero_avaliacao)
		    REFERENCES avaliacao (numero_avaliacao)
		    ON DELETE RESTRICT ON UPDATE RESTRICT;

		ALTER TABLE aplica ADD CONSTRAINT FK_aplica_1
		    FOREIGN KEY (FK_professor_cod_professor, FK_professor_FK_pessoa_cpf)
		    REFERENCES professor (cod_professor, FK_pessoa_cpf)
		    ON DELETE RESTRICT ON UPDATE RESTRICT;

		ALTER TABLE faz ADD CONSTRAINT FK_faz_0
		    FOREIGN KEY (FK_aluno_matricula, FK_aluno_FK_pessoa_cpf)
		    REFERENCES aluno (matricula, FK_pessoa_cpf)
		    ON DELETE RESTRICT ON UPDATE RESTRICT;

		ALTER TABLE faz ADD CONSTRAINT FK_faz_1
		    FOREIGN KEY (FK_avaliacao_numero_avaliacao)
		    REFERENCES avaliacao (numero_avaliacao)
		    ON DELETE RESTRICT ON UPDATE RESTRICT;

		ALTER TABLE ensina ADD CONSTRAINT FK_ensina_0
		    FOREIGN KEY (FK_professor_cod_professor, FK_professor_FK_pessoa_cpf)
		    REFERENCES professor (cod_professor, FK_pessoa_cpf)
		    ON DELETE SET NULL ON UPDATE CASCADE;

		ALTER TABLE ensina ADD CONSTRAINT FK_ensina_1
		    FOREIGN KEY (FK_materia_cod)
		    REFERENCES materia (cod)
		    ON DELETE SET NULL ON UPDATE CASCADE;

		ALTER TABLE frequenta ADD CONSTRAINT FK_frequenta_0
		    FOREIGN KEY (FK_aluno_matricula, FK_aluno_FK_pessoa_cpf)
		    REFERENCES aluno (matricula, FK_pessoa_cpf)
		    ON DELETE RESTRICT ON UPDATE RESTRICT;

		ALTER TABLE frequenta ADD CONSTRAINT FK_frequenta_1
		    FOREIGN KEY (FK_materia_cod)
		    REFERENCES materia (cod)
		    ON DELETE RESTRICT ON UPDATE RESTRICT;
	
		Insert into complemento(cod_complemento,dec_complemento)
			values('01','casa'),
			('02','condominio'),    		
			('03','apartamento');



		Insert into pais(nome_pais,numero_pais)
			values('BR',00),
			('USA',01),  
				('FRA',02),  
				('CHI',03),  
				('ARG',04);

		Insert into estado(nome_estado,numero_estado,fk_pais_numero_pais)
			values('ES',00,00),
				('RJ',01,00),  
				('SP',02,00),  
				('NY',03,01),  
				('RO',04,00);

		   Insert into cidade(nome_cidade,numero_cidade ,fk_estado_numero_estado)
			values('Serra',00,00),
				('Vitoria',01,00),  
				('Rio de Janeiro',02,01),  
				('São Paulo',03,02),  
				('Cariacica',04,00),
				('Vila Velha',05,00);


		   Insert into bairro_(nome_bairro,numero_bairro ,fk_cidade_numero_cidade)
			values('nova almeida',00,00),
			('jardim da penha',01,01),  
				('laranjeiras',02,00),  
				('Cobilândia',03,05),  
				('Jardim Camburi',04,01);	




		   Insert into endereco_(numero,codigo,fk_complemento_cod_complemento,fk_bairro__numero_bairro)
				values(01,'1111',01,00),
				(02,'2222',01,01),  
				(03,'3333',02,02),  
				(04,'4444',03,03),  
				(05,'5555',02,04);	


		 Insert Into Turma( nome_turma, numero_turma)
			   Values ('A', '00'),
			   ('B', '01'),
			   ('C', '02'),
			   ('D', '03'),
			   ('X', '04');

		Insert Into pessoa (cpf,nome,data_de_nascimento,fk_endereco__codigo,sexo)
				Values ('11111111', 'Guilherme Bork','12-12-2002','1111','M'),
				('2222222222', 'Fabio', '09-09-2002','3333','M'),
				('3333333333', 'Daniel', '07-08-2001','2222','M'),
				('4444444444', 'Vanessa', '08-09-2003','3333','F'),
				('5555555555', 'Kamila', '02-09-2000','4444','F'),
				('6666666666', 'Paulo', '17-09-1985','5555','M'),
				('7777777777', 'Jeferson', '20-06-1976','5555','M');



		Insert into logadouro(cod,tipo,nome,fk_endereco__codigo)
		values(01,'Avenida','belo horizonte','1111'),
		(02,'Avenida','Dante Michelini','5555'),
		(03,'Rua' ,'Albérico Bitencourt','4444'),
		(04,'Rua','Boulevard Antilhas','3333'),
		(05,'Avenida','Abido Saad','2222');

		Insert Into aluno (matricula, fk_pessoa_cpf, fk_turma_numero_turma)
		Values ('00000', '11111111','00'),
		('11111', '2222222222', '00'),
		('22222', '3333333333', '02'),
		('33333', '4444444444', '03'),
		('55555', '5555555555', '01');



		Insert Into professor(cod_professor, fk_pessoa_cpf)
		Values ('01111', '6666666666'),
		('02222', '7777777777');



		Insert Into avaliacao(Nome_avaliacao, data_avaliacao, Valor_avaliacao,numero_avaliacao)
		Values ('prova1', '12-12-2018', 10,1),
		('Trab1', '12-12-2018', 25,2),
		('Prova2', '13-12-2018', 10,3),
		('Trab2', '13-12-2018', 5,4),
		('Trab3', '13-12-2018', 10,5);


		Insert Into aplica(fk_avaliacao_numero_avaliacao,fk_professor_cod_professor,fk_professor_fk_pessoa_cpf)
		Values (1,'01111','6666666666'),
		(2,'01111','6666666666'),
		(3,'01111','6666666666'),
		(4,'02222','7777777777'),
		(5,'02222','7777777777');




		Insert into ano(cod,descricao,FK_turma_numero_turma)
		values(01,'2013','00'),
		(02,'2014','01'),
		(03,'2015','02'),
		(04,'2016','03'),
		(05,'2017','04');


		Insert Into ensina(fk_professor_cod_professor,fk_professor_fk_pessoa_cpf,fk_materia_cod)
		Values ('01111','6666666666',1),
		('02222','7777777777',2),



		Insert Into materia(cod,descricao)
		Values (1,'Matematica'),
		(2,'Historia'),


		Insert into leciona(fk_turma_numero_turma,fk_professor_cod_professor ,fk_professor_fk_pessoa_cpf)
			values('00','01111','6666666666'),
				('01','01111','6666666666'),  
				('02','01111','6666666666'),  
				('03','02222','7777777777'),  
				('04','02222','7777777777');	

		Insert into faz(fk_aluno_matricula,fk_aluno_fk_pessoa_cpf ,fk_avaliacao_numero_avaliacao,nota)
			values('00000','11111111','1','7'),
				('11111','2222222222','1','8'),  
				('22222','3333333333','1','10'),  
				('33333','4444444444','1','5.5'),  
				('55555','5555555555','1','6.5');	


		insert into frequenta(fk_aluno_matricula,fk_aluno_fk_pessoa_cpf,fk_materia_cod,data,presenca)
		values('00000','11111111',1,'03-03-2017','.'),
		('11111','2222222222',1,'03-03-2017','.'),
		('22222','3333333333',1,'03-03-2017','.'),
		('33333','4444444444',1,'03-03-2017','.'),
		('55555','5555555555',1,'03-03-2017','F');



		
		
#### 8.3 INCLUSÃO DO SCRIPT PARA EXCLUSÃO DE TABELAS EXISTENTES, CRIAÇÃO DE TABELA NOVAS E INSERÇÃO DOS DADOS
     
     drop table aluno

	CREATE TABLE aluno (
	    matricula varChar(100),
	    FK_pessoa_cpf varchar(100),
	    FK_turma_numero_turma varChar(100),
	    PRIMARY KEY (matricula, FK_pessoa_cpf)
	);
	
	
	Insert Into aluno (matricula, fk_pessoa_cpf, fk_turma_numero_turma)
	Values ('00000', '11111111','00'),
	('11111', '2222222222', '00'),
	('22222', '3333333333', '02'),
	('33333', '4444444444', '03'),
	('55555', '5555555555', '01');
	
	drop table turma;

	CREATE TABLE turma (
	    numero_turma varChar(100) PRIMARY KEY,
	    nome_turma varChar(100)
	);
	
	 Insert Into Turma( nome_turma, numero_turma)
		   Values ('A', '00'),
		   ('B', '01'),
		   ('C', '02'),
		   ('D', '03'),
		   ('X', '04');
	
	drop table professor;

	CREATE TABLE professor (
	    cod_professor varChar(100),
	    FK_pessoa_cpf varchar(100),
	    PRIMARY KEY (cod_professor, FK_pessoa_cpf)
	);
	
	
	Insert Into professor(cod_professor, fk_pessoa_cpf)
	Values ('01111', '6666666666'),
	('02222', '7777777777');
	
	drop table avaliacao;

	CREATE TABLE avaliacao (
	    valor_avaliacao float,
	    data_avaliacao date,
	    numero_avaliacao int PRIMARY KEY,
	    nome_avaliacao varChar(100)
	);
	
	
	Insert Into avaliacao(Nome_avaliacao, data_avaliacao, Valor_avaliacao,numero_avaliacao)
	Values ('prova1', '12-12-2018', 10,1),
	('Trab1', '12-12-2018', 25,2),
	('Prova2', '13-12-2018', 10,3),
	('Trab2', '13-12-2018', 5,4),
	('Trab3', '13-12-2018', 10,5);

	
	drop table endereco_;

	CREATE TABLE endereco_ (
	    numero int,
	    codigo varChar(100) PRIMARY KEY,
	    FK_complemento_cod_complemento int,
	    FK_bairro__numero_bairro int
	);
	
	
	   Insert into endereco_(numero,codigo,fk_complemento_cod_complemento,fk_bairro__numero_bairro)
			values(01,'1111',01,00),
			(02,'2222',01,01),  
			(03,'3333',02,02),  
			(04,'4444',03,03),  
			(05,'5555',02,04);	
	
	
	dorp table bairro;

	CREATE TABLE bairro_ (
	    nome_bairro varChar(100),
	    numero_bairro int PRIMARY KEY,
	    FK_cidade_numero_cidade int
	);
	
	   Insert into bairro_(nome_bairro,numero_bairro ,fk_cidade_numero_cidade)
		values('nova almeida',00,00),
   		('jardim da penha',01,01),  
    		('laranjeiras',02,00),  
    		('Cobilândia',03,05),  
    		('Jardim Camburi',04,01);	

	drop table cidade;

	CREATE TABLE cidade (
	    nome_cidade varChar(100),
	    numero_cidade int PRIMARY KEY,
	    FK_estado_numero_estado int
	);
	 
	 Insert into cidade(nome_cidade,numero_cidade ,fk_estado_numero_estado)
		values('Serra',00,00),
   		('Vitoria',01,00),  
    		('Rio de Janeiro',02,01),  
    		('São Paulo',03,02),  
    		('Cariacica',04,00),
		('Vila Velha',05,00);

	drop table pais;

	CREATE TABLE pais (
	    nome_pais varChar(100),
	    numero_pais varChar(100) PRIMARY KEY
	);
	
	
	Insert into pais(nome_pais,numero_pais)
		values('BR',00),
   		('USA',01),  
    		('FRA',02),  
    		('CHI',03),  
    		('ARG',04);
		
	drop table estado;

	CREATE TABLE estado (
	    nome_estado varChar(100),
	    numero_estado int PRIMARY KEY,
	    FK_pais_numero_pais varChar(100)
	);
	
		
	Insert into estado(nome_estado,numero_estado,fk_pais_numero_pais)
		values('ES',00,00),
   		('RJ',01,00),  
    		('SP',02,00),  
    		('NY',03,01),  
    		('RO',04,00);
	
	drop table complemento;

	CREATE TABLE complemento (
	    cod_complemento int PRIMARY KEY,
	    dec_complemento varChar(100)
	);
	
	
	 Insert into complemento(cod_complemento,dec_complemento)
		values('01','casa'),
		('02','condominio'),    		
		('03','apartamento');
 
	drop table logadouro;

	CREATE TABLE logadouro (
	    cod Serial PRIMARY KEY,
	    tipo varChar(100),
	    nome varChar(200),
	    FK_endereco__codigo varChar(100)
	);
	
	
	Insert into logadouro(cod,tipo,nome,fk_endereco__codigo)
	values(01,'Avenida','belo horizonte','1111'),
	(02,'Avenida','Dante Michelini','5555'),
	(03,'Rua' ,'Albérico Bitencourt','4444'),
	(04,'Rua','Boulevard Antilhas','3333'),
	(05,'Avenida','Abido Saad','2222');

	drop table ano;

	CREATE TABLE Ano (
	    cod varChar(200) PRIMARY KEY,
	    descricao varChar(100),
	    FK_turma_numero_turma varChar(100)
	);
	
	
	Insert into ano(cod,descricao,FK_turma_numero_turma)
	values(01,'2013','00'),
	(02,'2014','01'),
	(03,'2015','02'),
	(04,'2016','03'),
	(05,'2017','04');

	drop table pessoa;

	CREATE TABLE pessoa (
	    nome varchar(100),
	    cpf varchar(100) PRIMARY KEY,
	    data_de_nascimento date,
	    FK_endereco__codigo varChar(100)
	);
	
	CREATE TABLE pessoa (
	    nome varchar(100),
	    cpf varchar(100) PRIMARY KEY,
	    data_de_nascimento date,
	    FK_endereco__codigo varChar(100)
	    sexo char
	);

	
	Insert Into pessoa (cpf,nome,data_de_nascimento,fk_endereco__codigo,sexo)
		Values ('11111111', 'Guilherme Bork','12-12-2002','1111','M'),
		('2222222222', 'Fabio', '09-09-2002','3333','M'),
		('3333333333', 'Daniel', '07-08-2001','2222','M'),
		('4444444444', 'Vanessa', '08-09-2003','3333','F'),
		('5555555555', 'Kamila', '02-09-2000','4444','F'),
		('6666666666', 'Paulo', '17-09-1985','5555','M'),
		('7777777777', 'Jeferson', '20-06-1976','5555','M');
		
	drop table materia;
	
	CREATE TABLE materia (
	    cod int PRIMARY KEY,
	    descricao varChar(100)
	);
	

	Insert Into materia(cod,descricao)
	Values (1,'Matematica'),
	(2,'Historia'),


	
	
	drop table leciona;

	CREATE TABLE leciona (
	    FK_turma_numero_turma varChar(100),
	    FK_professor_cod_professor varChar(100),
	    FK_professor_FK_pessoa_cpf varchar(100)
	);
	
	Insert into leciona(fk_turma_numero_turma,fk_professor_cod_professor ,fk_professor_fk_pessoa_cpf)
		values('00','01111','6666666666'),
   		('01','01111','6666666666'),  
    		('02','01111','6666666666'),  
    		('03','02222','7777777777'),  
    		('04','02222','7777777777');	
 
	drop table aplica;
	
	CREATE TABLE aplica (
	    FK_avaliacao_numero_avaliacao int,
	    FK_professor_cod_professor varChar(100),
	    FK_professor_FK_pessoa_cpf varchar(100)
	);
	
	Insert Into aplica(fk_avaliacao_numero_avaliacao,fk_professor_cod_professor,fk_professor_fk_pessoa_cpf)
	Values (1,'01111','6666666666'),
	(2,'01111','6666666666'),
	(3,'01111','6666666666'),
	(4,'02222','7777777777'),
	(5,'02222','7777777777');

	
	drop table faz;
	
	CREATE TABLE faz (
	    FK_aluno_matricula varChar(100),
	    FK_aluno_FK_pessoa_cpf varchar(100),
	    FK_avaliacao_numero_avaliacao int,
	    nota float
	);
		
	Insert into faz(fk_aluno_matricula,fk_aluno_fk_pessoa_cpf ,fk_avaliacao_numero_avaliacao,nota)
	values('00000','11111111','1','7'),
		('11111','2222222222','1','8'),  
		('22222','3333333333','1','10'),  
		('33333','4444444444','1','5.5'),  
		('55555','5555555555','1','6.5');	

		
	
	drop table ensina;

	CREATE TABLE ensina (
	    FK_professor_cod_professor varChar(100),
	    FK_professor_FK_pessoa_cpf varchar(100),
	    FK_materia_cod int
	);
	
	Insert Into ensina(fk_professor_cod_professor,fk_professor_fk_pessoa_cpf,fk_materia_cod)
	Values ('01111','6666666666',1),
	('02222','7777777777',2),
	
	
	
	
	drop table frequenta;
	
	
		CREATE TABLE frequenta (
		    FK_aluno_matricula varChar(100),
		    FK_aluno_FK_pessoa_cpf varchar(100),
		    FK_materia_cod int,
		    data date,
		    presenca char
		);

	

		insert into frequenta(fk_aluno_matricula,fk_aluno_fk_pessoa_cpf,fk_materia_cod,data,presenca)
		values('00000','11111111',1,'03-03-2017','.'),
		('11111','2222222222',1,'03-03-2017','.'),
		('22222','3333333333',1,'03-03-2017','.'),
		('33333','4444444444',1,'03-03-2017','.'),
		('55555','5555555555',1,'03-03-2017','F');



### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
   

#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>
            Select * from Aluno
            
   ![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/tabela%20aluno.png?raw=true)
            
	    Select * from ano 
	    
   ![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/tabela%20ano.png?raw=true)
	    
            Select * from aplica
            
   ![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/tabela%20aplica.png?raw=true)
            
            Select * from avaliacao
   
   ![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/tabela%20avaliacao.png?raw=true)
            
            Select * from bairro_
            
   ![Alt text]( https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/tabela%20bairro_.png?raw=true)
   
  
   	Select * from complemento
            
   ![Alt text]( https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/tabela%20complemento.png?raw=true)
           
	   Select * from endereco_
            
   ![Alt text]( https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/tabela%20endereco_.png?raw=true)
           
	   Select * from ensina
            
   ![Alt text]( https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/tabela%20ensina.png?raw=true)
           
	   Select * from estado
            
   ![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/tabela%20estado.png?raw=true)
           
	   Select * from cidade
            
   ![Alt text]( https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/tabela%20cidade.png?raw=true)
   
           
	   Select * from complemento
            
   ![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/tabela%20complemento.png?raw=true)
           
	   Select * from endereco_
            
   ![Alt text]( https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/tabela%20endereco_.png?raw=true)
           
	   Select * from ensina
            
   ![Alt text]( https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/tabela%20ensina.png?raw=true)
   
           
	   Select * from estado
            
   ![Alt text]( https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/tabela%20estado.png?raw=true)
           
	   Select * from faz
            
   ![Alt text]( https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/tabela%20faz.png?raw=true)
           
	   Select * from frequenta
            
   ![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/tabela%20frequenta.png?raw=true)
   
   	
	   Select * from leciona
            
   ![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/tabela%20leciona.png?raw=true)
   
	   Select * from logadouro
            
   ![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/tabela%20logadouro.png?raw=true)
   
	   Select * from materia
            
   ![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/tabela%20materia.png?raw=true)
   	   
	     Select * from pais
            
   ![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/tabela%20pais.png?raw=true)
   
    	    Select * from pessoa
            
   ![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/tabela%20pessoa.png?raw=true)
   
   	    Select * from professor
            
   ![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/tabela%20professor.png?raw=true)
   
    	    Select * from turma
            
   ![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/tabela%20turma.png?raw=true)
   
   
           
	   
           
   

#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>
            
	    Select * from pessoa  Where data_de_nascimento > '12-12-2000'

![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/where%20nascimento.png?raw=true)	    
	  
             Select * from pessoa  Where sexo = 'F'

![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/where%20sexo.png?raw=true)

           Select * from aluno  where fk_turma_numero_turma = '00'

![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/where%20sexo%20turma.png?raw=true)
           
            Select * from ano Where descricao >'2015'
            
![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/2015.png?raw=true)	    
	    
#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
     
     	Select * from Aluno  where matricula='00000' or matricula ='33333' or matricula = '55555'
	
![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/select1.png?raw=true)
	
	Select * from Professor Where cod_professor='02222'
	
![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/select2.png?raw=true)	

       Select * from Turma Where Nome_turma != 'A'
	
![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/select3.png?raw=true)	

       Select * from avaliacao Where Valor_avaliacao = 10 or Valor_avaliacao = 5
	
![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/select4.png?raw=true)
 
 	Select * from Professor Where cod_professor='01111'

![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/select5.png?raw=true)
		
		Select * from Avaliacao
		Where Valor_avaliacao = 10 and 
		Data_avaliacao > '12-03-2017'

![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/select6.png?raw=true)
   		 	
			Select * from avaliacao
        		Where Valor_avaliacao > 10
	
![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/select7.png?raw=true)	
        
	 Select nome as humanos from pessoa
	
![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/select8.png?raw=true)        

  	 Select matricula as Código_de_Barra from Aluno 

![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/select9.png?raw=true)
	
	Select data_avaliacao as data_de_avaliacoes from avaliacao
   
 ![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/select10.png?raw=true)
 	
	 select * from estado where fk_pais_numero_pais='0'
   
 ![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/select11.png?raw=true)
    
#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
    a) Criar outras 5 consultas que envolvam like ou ilike
    b) Criar uma consulta para cada tipo de função data apresentada.


    
#### 9.5	ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>
	
	delete from cidade where fk_estado_numero_estado='1'
 ![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/delete1.png?raw=true)	
	
	delete from estado where fk_pais_numero_pais='1'
 ![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/delete2.png?raw=true)
	
	delete from avaliacao where nome_avaliacao ='prova2'
 ![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/delete3.png?raw=true)	
	
	update avaliacao set nome_avaliacao='prova2' where nome_avaliacao = 'Trab3' 
 ![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/update1.png?raw=true)	
	
	update pessoa set nome='carla' where nome='Guilherme Bork'
 ![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/update2.png?raw=true)	
	
	update pessoa set sexo='F' where nome='carla'
 ![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/update3.png?raw=true)
	
#### 9.6	CONSULTAS COM JUNÇÃO E ORDENAÇÃO (Mínimo 6)<br>
       		     select p.nome,
                            a.nome_avaliacao,
                            a.valor_avaliacao,
                            f.nota,
                            m.descricao as materia
			    from faz f 
                            inner join avaliacao a
                            on (f.fk_avaliacao_numero_avaliacao = a.numero_avaliacao)inner join aluno al
			    on(f.fk_aluno_matricula = al.matricula)inner join pessoa p 
			    on(p.cpf = al.fk_pessoa_cpf )inner join aplica ap
                            on(f.fk_avaliacao_numero_avaliacao = ap.fk_avaliacao_numero_avaliacao)inner join ensina e
                            on(ap.fk_professor_cod_professor = e.fk_professor_cod_professor) inner join materia m 
                            on(e.fk_materia_cod = m.cod)
                            where f.nota >= a.valor_avaliacao *0.6
			    order by nota desc
	
![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/group1.png?raw=true)
        
			  select f.fk_aluno_matricula,
                               f.nota,
                               p.nome,
                               a.nome_avaliacao
                               from faz f
                               inner join avaliacao a
                               on (f.fk_avaliacao_numero_avaliacao = a.numero_avaliacao)
                               inner join pessoa p
                               on (p.cpf = f.fk_aluno_fk_pessoa_cpf)
                               order by f.nota desc
                               limit 3

![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/innejoin2.png?raw=true)
		       
			select ava.nome_avaliacao,
                               t.nome_turma,
                               avg(f.nota)
                               from faz f inner join avaliacao ava
                               on (ava.numero_avaliacao = f.fk_avaliacao_numero_avaliacao)
                               inner join aluno a 
                               on (f.fk_aluno_matricula = a.matricula)
                               inner join turma t
                               on (a.fk_turma_numero_turma = t.numero_turma)
                               group by t.nome_turma,ava.nome_avaliacao
                               order by avg(f.nota) desc

![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/innerjoin3.png?raw=true)
				
				select t.nome_turma,
				sum((case when p.sexo='M' then 1 else 0 end)) as masculino,
				sum((case when p.sexo='F' then 1 else 0 end)) as feminino
				from pessoa p 
				inner join aluno a 
				on (p.cpf = a.fk_pessoa_cpf) inner join turma t
				on (a.fk_turma_numero_turma = t.numero_turma)
				group by t.nome_turma 
				order by t.nome_turma
							
				
![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/innerjoin4.png?raw=true)

			select nome_turma,
                            a.descricao as ano_de_criação
                            from turma t
                            inner join ano a
                            on (t.numero_turma = a.Fk_turma_numero_turma)
                            where a.descricao >'2014'
								
![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/innerjoin5.png?raw=true)	

	select  p.nome,
                    m.descricao as materia,
                    sum((case when f.presenca='.' then 1 else 0 end)) as dias_presentes
                    from pessoa p inner join frequenta f
                    on(p.cpf = f.fk_aluno_fk_pessoa_cpf) inner join materia m 
                    on(m.cod = f.fk_materia_cod)
                    group by p.nome,m.descricao

![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/innerjoin6.png?raw=true)
	
## Marco de Entrega 02 em: (16/06/2018)<br>
### ATUALIZAÇÃO DA DOCUMENTAÇÃO DOS SLIDES PARA APRESENTAÇAO SEMESTRAL (Mínimo 6 e Máximo 10)<br>
<br>
    Data de Entrega: (30/06/2018)
<br>

#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>
					   
			select ava.nome_avaliacao,
                               t.nome_turma,
                               avg(f.nota)
                               from faz f inner join avaliacao ava
                               on (ava.numero_avaliacao = f.fk_avaliacao_numero_avaliacao)
                               inner join aluno a 
                               on (f.fk_aluno_matricula = a.matricula)
                               inner join turma t
                               on (a.fk_turma_numero_turma = t.numero_turma)
                               group by t.nome_turma,ava.nome_avaliacao
                               order by avg(f.nota) desc

![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/innerjoin3.png?raw=true)

				select t.nome_turma,
				sum((case when p.sexo='M' then 1 else 0 end)) as masculino,
				sum((case when p.sexo='F' then 1 else 0 end)) as feminino
				from pessoa p 
				inner join aluno a 
				on (p.cpf = a.fk_pessoa_cpf) inner join turma t
				on (a.fk_turma_numero_turma = t.numero_turma)
				group by t.nome_turma 
				order by t.nome_turma
							
				
![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/innerjoin4.png?raw=true)

	
	select  p.nome,
                    m.descricao as materia,
                    sum((case when f.presenca='.' then 1 else 0 end)) as dias_presentes
                    from pessoa p inner join frequenta f
                    on(p.cpf = f.fk_aluno_fk_pessoa_cpf) inner join materia m 
                    on(m.cod = f.fk_materia_cod)
                    group by p.nome,m.descricao

![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/innerjoin6.png?raw=true)


#### 9.8	CONSULTAS COM LEFT E RIGHT JOIN (Mínimo 4)<br>
#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>
        a) Uma junção que envolva Self Join
        b) Outras junções com views que o grupo considere como sendo de relevante importância para o trabalho
#### 9.10	SUBCONSULTAS (Mínimo 3)<br>

#### 9.11	LISTA DE CODIGOS DAS FUNÇÕES E TRIGGERS<br>
        Detalhamento sobre funcionalidade de cada código.
        a) Objetivo
        b) Código do objeto (função/trigger)
        c) exemplo de dados para aplicação
        d) resultados em forma de tabela/imagem
<br>


#### 9.12	GERACAO DE DADOS (MÍNIMO DE 100 MIL REGISTROS PARA PRINCIPAL RELAÇAO)<br>
        a) principal tabela do sistema deve ter no mínimo 100 mil registros
        b) tabelas diretamente relacionadas a tabela principal 10 mil registros
        c) tabelas auxiliares de relacao multivalorada mínimo de 10 registros
        d) registrar o tempo de inserção em cada uma das tabelas do banco de dados
        e) especificar a quantidade de registros inseridos em cada tabela
        Para melhor compreensão verifiquem o exemplo na base de testes:<br>
        https://github.com/discipbd2/base-de-testes-locadora
        

#### 9.13	Backup do Banco de Dados<br>
        Detalhamento do backup.
        a) Tempo
        b) Tamanho
        c) Teste de restauração (backup)
        d) Tempo para restauração
        e) Teste de restauração (script sql)
        f) Tempo para restauração (script sql)
<br>

Data de Entrega: (Data a ser definida)
<br>

#### 9.14	APLICAÇAO DE ÍNDICES E TESTES DE PERFORMANCE<br>
    a) Lista de índices, tipos de índices com explicação de porque foram implementados nas consultas 
    b) Performance esperada VS Resultados obtidos
    c) Tabela de resultados comparando velocidades antes e depois da aplicação dos índices (constando velocidade esperada com planejamento, sem indice e com índice Vs velocidade de execucao real com índice e sem índice).
    d) Escolher as consultas mais complexas para serem analisadas (consultas com menos de 2 joins não serão aceitas)
    e) As imagens do Explain devem ser inclusas no trabalho, bem como explicações sobre os resultados obtidos.
    f) Inclusão de tabela mostrando as 10 execuções, excluindo-se o maior e menor tempos para cada consulta e 
    obtendo-se a media dos outros valores como resultado médio final.
<br>
    Data de Entrega: (Data a ser definida)
<br>   

### 10	ATUALIZAÇÃO DA DOCUMENTAÇÃO DOS SLIDES PARA APRESENTAÇAO FINAL (Mínimo 6 e Máximo 10)<br>
<br>
    Data de Entrega: (Data a ser definida)
<br>

### 11 Backup completo do banco de dados postgres 
    a) deve ser realizado no formato "backup" 
        (Em Dump Options #1 Habilitar opções Don't Save Owner e Privilege)
    b) antes de postar o arquivo no git o mesmo deve ser testado/restaurado por outro grupo de alunos/dupla
    c) informar aqui o grupo de alunos/dupla que realizou o teste.

    
### 12	TUTORIAL COMPLETO DE PASSOS PARA RESTAURACAO DO BANCO E EXECUCAO DE PROCEDIMENTOS ENVOLVIDOS NO TRABALHO PARA OBTENÇÃO DOS RESULTADOS<br>
        a) Outros grupos deverão ser capazes de restaurar o banco 
        b) executar todas as consultas presentes no trabalho
        c) executar códigos que tenham sido construídos para o trabalho 
        d) realizar qualquer procedimento executado pelo grupo que desenvolveu o trabalho

### 13	DIFICULDADES ENCONTRADAS PELO GRUPO<br>  

    
>## Marco de Entrega 04/Entrega Final em: (Data definida no cronograma)<br>

       
### 14  FORMATACAO NO GIT: https://help.github.com/articles/basic-writing-and-formatting-syntax/
<comentario no git>
    
##### About Formatting
    https://help.github.com/articles/about-writing-and-formatting-on-github/
    
##### Basic Formatting in Git
    
    https://help.github.com/articles/basic-writing-and-formatting-syntax/#referencing-issues-and-pull-requests
   
    
##### Working with advanced formatting
    https://help.github.com/articles/working-with-advanced-formatting/

#### Mastering Markdown
    https://guides.github.com/features/mastering-markdown/

### OBSERVAÇÕES IMPORTANTES

#### Todos os arquivos que fazem parte do projeto (Imagens, pdfs, arquivos fonte, etc..), devem estar presentes no GIT. Os arquivos do projeto vigente não devem ser armazenados em quaisquer outras plataformas.
1. Caso existam arquivos com conteúdos sigilosos, comunicar o professor que definirá em conjunto com o grupo a melhor forma de armazenamento do arquivo.

#### Todos os grupos deverão fazer Fork deste repositório e dar permissões administrativas ao usuário deste GIT, para acompanhamento do trabalho.

#### Os usuários criados no GIT devem possuir o nome de identificação do aluno (não serão aceitos nomes como Eu123, meuprojeto, pro456, etc). Em caso de dúvida comunicar o professor.


Link para BrModelo:<br>
http://sis4.com/brModelo/brModelo/download.html
<br>


Link para curso de GIT<br>
![https://www.youtube.com/curso_git](https://www.youtube.com/playlist?list=PLo7sFyCeiGUdIyEmHdfbuD2eR4XPDqnN2?raw=true "Title")


        
        


    





