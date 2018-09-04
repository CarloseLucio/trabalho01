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

>Como Alunos do Instituto Federal do Espírito Santo, temos contato todos os dias com o ambiente escolar, e pudemos perceber que há algumas situações na escola, que com nosso conhecimento com programação e bancos de dados poderiamos auxiliar e otimizar isso, um desses que percebemos foi a chamada que o professor faz. Ocorre muito na sala de aula dos alunos chegarem atrasado alguns minutos e os professores acabam perdendo certo tempo esperando todos chegarem para fazer a chamada, com isso, criamos a Relavabor Company que é a nossa empresa que tem o intuito de auxiliar com a tecnologia o ambiente escolar. Pensamos em vários metodos de ajudar nesse situação e chegamos a conclusão que seria um otimo investimento a utilização de reconhecimento facial para fazer a chamada para os professores. Nosso projeto é a instalação de sensores na porta e quando os estudantes entrarem na sala já seria reconhecido quem é o aluno, o horario que ele entrou,a aula, entre outros dados.Criaremos também um site que conterá todas as informações captadas pelo sensor e mais certas coisas como notas,atividades,historico presencial, etc. Pensamos que a educação é o futuro e com a tecnologia só  tende a melhorar.  

### 3.MINI-MUNDO Novo<br>

Descrição textual das regras de negócio definidas como um  subconjunto do mundo real 
cujos elementos são propriedades que desejamos incluir, processar, armazenar, 
gerenciar, atualizar, e que descrevem a proposta/solução a ser desenvolvida.

> O Sistema proposto para a "Relevabor Company" conterá as informações aqui detalhados. O sistema será formado pelo site e pelo sensor da porta que será conectado com o sistema. Cada professor irá ter seu cadastro online com seu email,nome,matrícula e uma senha, o educador possuirá algumas opções sobre o que visualizar ou o que criar. O professor poderá acessar a opção criar, onde ele poderá cadastrar um aluno, uma turma,uma atividade ou uma nota. Para cadastrar um estudante ele colocará o nome a matrícula, o email, o sexo, o cpf, a data de nascimento e uma foto para o sensor fazer o reconhecimento. Para cadastrar uma turma precisará de colocar o nome, o ano que foi criada essa turma, o turno e adicionar os alunos através do nomes ou matrícula. Para criar uma atividade ele precisará colocar o nome da atividade, o tipo caso for uma prova ou só uma atividade, a data que ela ocorrerá, o horario, a turma e quantos pontos valerá. Para adicionar notas o usuário colocará a turma, selecionará qual foi a atividade criada, digitara o nome do aluno e escreverá a nota. 
    No sistema proposto o Professor também poderá visualizar certas coisas como o historico presencial dos alunos que será feito diretamente pelo sensor, o usuário só precisará colocar a data,turma e a aula, que irá mostrar todos os alunos e se eles chegaram atrasados ou faltaram.Também será possivel ver um resumo de cada aluno na opção alunos da pagina inicial, nessa opção o usuário colocará o nome do aluno e será possivel ver a foto do estudante junto com o número total de faltas e presenças em todas materias e também a turma a qual ele pertence. Outra opção que o educador terá é o boletim onde ele só selecionará a turma e a matéria e será possivel ver a nota de todos os alunos em ordem alfabética. E a ultima opção será o calendario de atividades onde o professor poderá ver pela data o que já está marcado para uma determinada turma e assim não correr o risco de marcar outra coisa no mesmo horario ou dia. 

### 4.RASCUNHOS BÁSICOS DA INTERFACE (MOCKUPS)<br>


![Alt text](https://github.com/discipbd1/trab01/blob/master/balsamiq.png?raw=true "Title")
![Arquivo PDF do Protótipo Balsamiq feito para Empresa Relevabor Company](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/arquivos/ah.pdf?raw=true "Relevabor Company")


#### 4.1 TABELA DE DADOS DO SISTEMA:
    
    https://cdn.discordapp.com/attachments/383721330106957838/450829572360110081/gnt.png
    
    
    O sistema proposto poderá fornecer esses tipos de relatórios e informações : 
    
    1) Os dados de todos os alunos
    2) O registro de entrada e saída dos alunos
    3) Notas em geral de cada aluno
    4) A qual turma o aluno pertence e quaid matérias ele tem
    5) Calendário de atividades, horário das aulas e de eventos da escola

>## Marco de Entrega 01 em: (24/03/2018)<br>

### 5.MODELO CONCEITUAL<br>
        
![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/gg.png?raw=true "Modelo Conceitual")
    
        
    
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

![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/tey.png?raw=true "Modelo Logico")



### 7	MODELO FÍSICO<br>
       Create Table Aluno(
          Matrícula Varchar(10) Primary Key, 
          Nome_aluno Varchar(85), 
          dat_nasc Date);

        Create Table Turma(
          Num_Turma Serial Primary Key,
          Nome_turma Varchar(85),
          Data_Criacao Date);

        Create Table Professor(
          Matricula Varchar(10) Primary Key,
           Nome_prof Varchar(85),
           Cpf_prof Varchar(11));

        Create Table Avaliacoes(
           Num_avalicao Serial Primary Key,
           Nome_avalicao Varchar(45),
           Dat_Avalicao date,
           Valor_avalicao float);      
        
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
#### 8.1 DETALHAMENTO DAS INFORMAÇÕES
        
          Insert Into aluno (Matrícula, Nome_aluno, dat_nasc)
			Values ('11111111', 'Guilherme Bork','12-12-2002'),
            ('2222222222', 'Fabio', '09-09-2002'),
            ('3333333333', 'Daniel', '07-08-2001'),
            ('4444444444', 'Vanessa', '08-09-2003'),
            ('5555555555', 'Kamila', '02-09-2000');
             
            Insert Into Turma( Nome_turma, Data_criacao)
            Values ('A', '01-01-2017'),
            ('B', '01-01-2017'),
            ('C', '01-06-2017'),
            ('D', '01-01-2018'),
            ('X', '01-06-2018');
            
         Insert Into Professor(Matricula, Nome_prof, cpf_prof)
            Values ('0111111111', 'Cesar', '111111111'),
            ('0222222222', 'Morgana', '222222222'),
            ('0333333333','Pedro', '3333333333'),
            ('0444444444', 'Thais', '444444444'),
            ('0555555555', 'Rick', '555555555');
            
            Insert Into Avaliacoes(Nome_avalicao, Dat_avalicao, Valor_avalicao)
            Values ('prova1', '12-12-2018', 10),
            ('Trab1', '12-12-2018', 25),
            ('Prova2', '12-12-2018', 10),
            ('Trab2', '12-12-2018', 5),
            ('Trab3', '12-12-2018', 10);
             
#### 8.2 INCLUSÃO DO SCRIPT PARA CRIAÇÃO DE TABELA E INSERÇÃO DOS DADOS
          Create Table Aluno(
          Matrícula Varchar(10) Primary Key, 
          Nome_aluno Varchar(85), 
          dat_nasc Date);

        Create Table Turma(
          Num_Turma Serial Primary Key,
          Nome_turma Varchar(85),
          Data_Criacao Date);

        Create Table Professor(
          Matricula Varchar(10) Primary Key,
           Nome_prof Varchar(85),
           Cpf_prof Varchar(11));

        Create Table Avaliacoes(
           Num_avalicao Serial Primary Key,
           Nome_avalicao Varchar(45),
           Dat_Avalicao date,
           Valor_avalicao float);    
          
	  Insert Into aluno (Matrícula, Nome_aluno, dat_nasc)
	  Values ('11111111', 'Guilherme Bork','12-12-2002'),
            ('2222222222', 'Fabio', '09-09-2002'),
            ('3333333333', 'Daniel', '07-08-2001'),
            ('4444444444', 'Vanessa', '08-09-2003'),
            ('5555555555', 'Kamila', '02-09-2000');
             
            Insert Into Turma( Nome_turma, Data_criacao)
            Values ('A', '01-01-2017'),
            ('B', '01-01-2017'),
            ('C', '01-06-2017'),
            ('D', '01-01-2018'),
            ('X', '01-06-2018');
            
         Insert Into Professor(Matricula, Nome_prof, cpf_prof)
            Values ('0111111111', 'Cesar', '111111111'),
            ('0222222222', 'Morgana', '222222222'),
            ('0333333333','Pedro', '3333333333'),
            ('0444444444', 'Thais', '444444444'),
            ('0555555555', 'Rick', '555555555');
            
            Insert Into Avaliacoes(Nome_avalicao, Dat_avalicao, Valor_avalicao)
            Values ('prova1', '12-12-2018', 10),
            ('Trab1', '12-12-2018', 25),
            ('Prova2', '12-12-2018', 10),
            ('Trab2', '12-12-2018', 5),
            ('Trab3', '12-12-2018', 10);
	    
#### 8.3 INCLUSÃO DO SCRIPT PARA EXCLUSÃO DE TABELAS EXISTENTES, CRIAÇÃO DE TABELA NOVAS E INSERÇÃO DOS DADOS
    
    drop table aluno;
    
	 Create Table Aluno(
      	 Matrícula Varchar(10) Primary Key, 
     	 Nome_aluno Varchar(85), 
      	 dat_nasc Date);

	Insert Into aluno (Matrícula, Nome_aluno, dat_nasc)
 	 Values ('11111111', 'Guilherme Bork','12-12-2002'),
        ('2222222222', 'Fabio', '09-09-2002'),
        ('3333333333', 'Daniel', '07-08-2001'),
        ('4444444444', 'Vanessa', '08-09-2003'),
        ('5555555555', 'Kamila', '02-09-2000');

    drop table turma; 
 
 	Create Table Turma(
      	Num_Turma Serial Primary Key,
      	Nome_turma Varchar(85),
	Data_Criacao Date);

	Insert Into Turma( Nome_turma, Data_criacao)
        Values ('A', '01-01-2017'),
        ('B', '01-01-2017'),
        ('C', '01-06-2017'),
        ('D', '01-01-2018'),
        ('X', '01-06-2018');
        
    drop table professor;
    
   	 Create Table Professor(
     	 Matricula Varchar(10) Primary Key,
 	 Nome_prof Varchar(85),
      	 Cpf_prof Varchar(11));
	   
	Insert Into Professor(Matricula, Nome_prof, cpf_prof)
        Values ('0111111111', 'Cesar', '111111111'),
        ('0222222222', 'Morgana', '222222222'),
        ('0333333333','Pedro', '3333333333'),
        ('0444444444', 'Thais', '444444444'),
        ('0555555555', 'Rick', '555555555');
        

    drop table Avaliacoes;

	Create Table Avaliacoes(
        Num_avalicao Serial Primary Key,
        Nome_avalicao Varchar(45),
        Dat_Avalicao date,
        Valor_avalicao float);    
        
        Insert Into Avaliacoes(Nome_avalicao, Dat_avalicao, Valor_avalicao)
        Values ('prova1', '12-12-2018', 10),
        ('Trab1', '12-12-2018', 25),
        ('Prova2', '12-12-2018', 10),
        ('Trab2', '12-12-2018', 5),
        ('Trab3', '12-12-2018', 10);


### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
   

#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>
            Select * from Aluno
            
   ![Alt text](https://raw.githubusercontent.com/ReconhecimentoFacial/trabalho01/master/imagens/turma.png )
            
            Select * from Avaliacoes
            
   ![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/avalia%C3%A7%C3%B5es.png?raw=true)
            
            Select * from Professor
   
   ![Alt text](https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/professor.png?raw=true)
            
            Select * from Turma
            
   ![Alt text]( https://github.com/ReconhecimentoFacial/trabalho01/blob/master/imagens/turma.png?raw=true)
           
   

#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>
            Select * from Aluno
            Where dat_nasc > '12-12-2000'

![Alt text](https://raw.githubusercontent.com/ReconhecimentoFacial/trabalho01/master/imagens/9.2%20-%201.png)	    
	  
            Select * from Aluno
            Where dat_nasc < '12-12-2000'

![Alt text](https://raw.githubusercontent.com/ReconhecimentoFacial/trabalho01/master/imagens/9.2%20-%202.png)

            Select * from Professor
       	    Where matricula = '0111111111'

![Alt text](https://raw.githubusercontent.com/ReconhecimentoFacial/trabalho01/master/imagens/9.2-3.png)
           
            Select * from Turma
            Where data_criacao >= '01-01-2017'
            
![Alt text](https://raw.githubusercontent.com/ReconhecimentoFacial/trabalho01/master/imagens/9.2-4.png)	    
	    
#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
        Select * from Aluno
       	Where dat_nasc > '12-12-2000' and dat_nasc < '12-12-2003'
	
![Alt text](https://raw.githubusercontent.com/ReconhecimentoFacial/trabalho01/master/imagens/931.png)

        Select * from Avaliacoes
        Where Valor_avalicao = 10 or Valor_avalicao = 5
	
![Alt text](https://raw.githubusercontent.com/ReconhecimentoFacial/trabalho01/master/imagens/932.png)	

        Select * from Professor
        Where Nome_Prof = 'Pedro' or Nome_prof = 'Thais'
	
![Alt text](https://raw.githubusercontent.com/ReconhecimentoFacial/trabalho01/master/imagens/933.png)	

        Select * from Turma
        Where Nome_turma != 'A'
	
![Alt text](https://raw.githubusercontent.com/ReconhecimentoFacial/trabalho01/master/imagens/934.png)

        Select * from Avaliacoes
        Where Valor_avalicao = 10 and 
        Dat_avalicao > '12-03-2017'

![Alt text](https://raw.githubusercontent.com/ReconhecimentoFacial/trabalho01/master/imagens/935.png)

        Select * from Avaliacoes
        Where Valor_avalicao > 10
   
![Alt text](https://raw.githubusercontent.com/ReconhecimentoFacial/trabalho01/master/imagens/936.png)
   
        Select Nome_aluno as batutinhas from Aluno
	
![Alt text](https://raw.githubusercontent.com/ReconhecimentoFacial/trabalho01/master/imagens/937.png)	
        
	Select Matrícula as Código_de_Barra from Aluno 
	
![Alt text](https://raw.githubusercontent.com/ReconhecimentoFacial/trabalho01/master/imagens/938.png)        
	
	Select dat_avalicao as data_avaliacao from avaliacoes

![Alt text](https://raw.githubusercontent.com/ReconhecimentoFacial/trabalho01/master/imagens/939.png)
    
    
#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
    a) Criar outras 5 consultas que envolvam like ou ilike
    b) Criar uma consulta para cada tipo de função data apresentada.


    
#### 9.5	ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>


#### 9.6	CONSULTAS COM JUNÇÃO E ORDENAÇÃO (Mínimo 6)<br>
        a) Uma junção que envolva todas as tabelas possuindo no mínimo 3 registros no resultado
        b) Outras junções que o grupo considere como sendo as de principal importância para o trabalho
        

## Marco de Entrega 02 em: (16/06/2018)<br>
### ATUALIZAÇÃO DA DOCUMENTAÇÃO DOS SLIDES PARA APRESENTAÇAO SEMESTRAL (Mínimo 6 e Máximo 10)<br>
<br>
    Data de Entrega: (30/06/2018)
<br>

#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>

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


        
        


    





