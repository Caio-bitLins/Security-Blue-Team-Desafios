### Atividade Steganografia |QUIZ|

1. Inicio o Kali Linux no VirtualBox
2. Instalei o arquivo da atividade no Kali linux
3. Depois de instalar usei o comando **|unzip|** para descompactar o arquivo.
4. Então abri o terminal na pasta de ***Downloads e logo em seguida fui para SBT_Steg_Lab***

![Captura de Tela 2024-08-03 às 10 50 10](https://github.com/user-attachments/assets/478efe17-d036-4c24-a7f7-d9f39abacb42)\

5. ExecuteI o comando ***steghide embed -ef secretmessage.txt -cf coverfile.jpg -sf hiddenmessage.jpg*** para incorporar o arquivo ***secretmessage.txt*** dentro do arquivo de capa ***coverfile.jpg*** e nomeie a saída como ***stegofile hiddenmessage.jpg.***
![image](https://github.com/user-attachments/assets/57c69b50-a73e-4362-950e-8378dc439ebd)

6. Fui até ***Stego Files** usando o comando ***cd Stego\ Files/.*** Usando o comando ***ls -a*** para listar todos os arquivos do diretório.
![image](https://github.com/user-attachments/assets/23fbb0f0-89c8-4b31-bd5c-6426ced71e32)

7. Usando o comando *steghide extract -sf nome do arquivo.* O curso deu três possíveis senhas, consegui encontrar ***FLAG1.txt*** no arquivo ***pizza.jpg*** usando a senha ***christmastree***. Usando o comando **cat**, deu para encontrar o a primeira flag ***kAN105KS***.
![image](https://github.com/user-attachments/assets/dae7631d-75b2-4bb1-9295-5f50e7940584)

8. Repetindo a etapa anterior. A FLAG2.txt foi encontrado no arquivo ***verypretty.jpg*** usando a senha *darksky123* tive como resultado ***001JDANL.***
***FLAG3.txt*** foi encontrada no arquivo ***car.jpg*** usando a senha *goldenwatch* tive como resultado ***1LRBA9IU***
![image](https://github.com/user-attachments/assets/1673611c-db41-403b-96e8-9f035f5e58af)
![image](https://github.com/user-attachments/assets/531d1d3c-748e-4c3f-97df-cb5b4895c57f)

### Respostas do Quiz

**1. Incorpore o arquivo 'secretmessage.txt' dentro do arquivo de capa 'coverfile.jpg' e nomeie o stegofile de saída como 'hiddenmessage.jpg'. Qual é o comando completo que você usaria para fazer isso?**
>steghide embed -ef secretmessage.txt -cf coverfile.jpg -sf hiddenmessage.jpg

**2. O sinalizador 1 está oculto dentro de um arquivo de texto em um dos arquivos de esteganografia. Qual é o valor?**
>kAN105KS

**3. O sinalizador 2 está oculto dentro de um arquivo de texto em um dos arquivos de esteganografia. Qual é o valor?**
>001JDANL

**4. A bandeira 3 está oculta dentro de um arquivo de texto em um dos arquivos de esteganografia. Qual é o valor?**
>1LRBA9IU


