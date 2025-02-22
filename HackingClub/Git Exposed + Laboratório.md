
Vulnerabilidade que ocorre quando a pasta .git vai para produção(não é inclusa no .gitignore) o que torna possível fazer o dump de todas as informações de logs, branchs, e código fonte. 


Ferramenta utilizada para fazer o dump do .git:

Git-dumper python3: [[https://github.com/arthaud/git-dumper]]

Comando: ./git-dumper.py URL Diretorio para criar o .git;


Passos realizados para capturar a flag do laborátorio(Git Exposed):

1 - Acessar o laboratório
2 - Perceber que tem um .git exposto
3 - Baixar o .git para maquina propria simulando o git da "empresa"
4 - Analisar os logs: git log
5 - Analisar quais foram as alterações entre eles: git show id(visualizar no git log)
6 - Capturar a flag 