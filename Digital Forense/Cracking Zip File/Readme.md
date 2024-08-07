# Atividade de Cracking Zip |QUIZ|

1. Inicio o Kali Linux no VirtualBox
2. Instalei o arquivo da atividade no Kali linux
4. Então abri o terminal na pasta de Downloads e logo em seguida fui para **SBT_ZIP_Cracking**
![image](https://github.com/user-attachments/assets/7cc67ac9-e41b-4fd8-a142-d2d066d50196)

***OBS🚨 Nesse desafio, para descobrir a senha precisei usar um ataque de dicionario, e usei uma WordList
chamada "rockyou.txt" e tem um repositório que mostro qual arquivo usei. só clicar
[Aqui.](https://github.com/Caio-bitLins/Como-baixar-WordList-no-Linux)***

5. Usando o comando **fcrackzip -D -p /home/caiofabao/Downloads/rockyou.txt -u BruteForceAttack.zip**
Depois de achar a senha ***a1b3c5** usei o comando *unzip* para acessar o arquivo e utilizei a senha. E achei *FLAG1.txt*
que teve como resultado ***J201AKKLO.***

•  fcrackzip — Seleccionar a ferramenta que queremos utilizar.

•  -D — Seleção da opção para um ataque de dicionário.

•  -u — Isso garante que o fcrackzip tenta realmente descompactar o arquivo, sem isso, não obteremos a senha correta.

•  -p — Use strings como senha.

•/home/caiofabao/Downloads/rockyou.txt — Esse é o local da nossa lista de palavras, necessária para realizar um ataque de dicionário.

•BruteForceAttack.zip — O arquivo que queremos quebrar.
![Captura de Tela 2024-08-07 às 15 23 11](https://github.com/user-attachments/assets/6b37e03e-ac5b-4088-bc09-b086377f9b9d)

6. Repetindo o mesmo processo, no arquivo ***DictonaryAttack.zip*** obtive a senha **FRIENDSHIPSTARS** e FLAG2.txt como ***91MD0QL11***

![Captura de Tela 2024-08-07 às 15 21 17](https://github.com/user-attachments/assets/49d8145c-f20e-4d3e-acc5-47e9175148f5)

# Respostas do QUIZ



