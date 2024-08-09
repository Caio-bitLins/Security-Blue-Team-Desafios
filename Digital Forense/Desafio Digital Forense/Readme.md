## Cenário do desafio e detalhes

O SOC recebeu um relatório anônimo de que um usuário está potencialmente exfiltrando dados da empresa. 
Foi tirada uma imagem do disco rígido do usuário e você é responsável por analisar o conteúdo de uma cópia perfeita para encontrar 
qualquer evidência de atividade mal-intencionada. Utilizando as suas competências recentemente desenvolvidas, pesquise as pastas e 
ficheiros utilizando técnicas para descobrir 4 peças de informação oculta (cada prova conterá a string {1 de 4} ou similar). Será testado 
quanto à sua capacidade de descobrir esta informação utilizando todas as técnicas leccionadas neste curso; Linux CLI 
navegação, identificação de extensões de ficheiros incorretas, identificação de ficheiros/pastas ocultas, esteganografia e 
cracking de palavras-passe.

## Do que precisa para fazer este desafio?
- Virtualbox (https://www.virtualbox.org/wiki/Downloads) ou qualquer software alternativo de máquina virtual (VMware, etc)

- Kali Linux VM (https://www.kali.org/downloads)

- Challenge Disk Image (arquivo .zip para facilidade de uso. Transfira isto para a sua VM Kali, descompacte e continue! Parte inferior da página)

## Evidência 1
1. Abri o arquivo no KaliLinux
2. Usei o comando ***unzip*** para analisar o que tem dentro dele.
3. Então usei comando *cd J\ Harrison Disk\ Image\ 10.09.2019/* para ver-lo melhor
![image](https://github.com/user-attachments/assets/51466fe9-2fcc-4b27-b028-cf52b99b98a2)

4. Usando o comando ***tree*** para exibir a estrutura de diretórios em formato de árvore. Mostra a hierarquia de diretórios e seus subdiretórios junto com os arquivos. Para usar esse comando precisa instalar usando **sudo apt-get install tree**
![image](https://github.com/user-attachments/assets/9862b501-7b46-4f12-9098-3e83f87508c7)
![image](https://github.com/user-attachments/assets/04cf9c26-3542-42f0-bf31-0d699f3f29c3)

5. Explorando a “Disk Drive”, me deparei com um diretório vazio chamado “to-do”. Embora pareça vazio à primeira vista, se usasse o comando ls -a, descobrir que na verdade ele contém um arquivo zip oculto. Mas precisa de uma senha.
![image](https://github.com/user-attachments/assets/ab5d2aa5-d5b3-4287-bbb3-06f7b17ba43a)

6. Usando um ataque de dicionário eu conseguir achar a senha do arquivo anterior. E por fim achei um **employee dump,** ou informações confidenciais.

![image](https://github.com/user-attachments/assets/595db03e-cc98-48aa-963b-7c0dcc059162)

## Evidência 2
1. Comecei a examinar o diretório ***Images*** para ver se há alguma informação valiosa em potencial, visto que stegofiles são frequentemente encontrados em cenários de treinamento. Para verificar as extensões dos arquivos, executei o comando |file *| e usei ***ls -l*** para verificar os tamanhos dos arquivos. Observei que os arquivos ***laptop.jpg e office 2.jpg*** tinham um tamanho de byte incomumente grande para uma imagem típica, tornando-os suspeitos.

![image](https://github.com/user-attachments/assets/0b1f98fa-1ae6-47a8-ad37-9b1d20099e30)

2. Navegando até **Images** usei o comando ***steghide extract -sf laptop.jpg*** para extrair informações dentro do arquivo
e usei **cat** para ler os *passwords*
![image](https://github.com/user-attachments/assets/3f3e0f8c-4bcd-42a7-ad78-30425ffc8dbc)

