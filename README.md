# Phishing para captura de senhas

### Ferramentas

- Kali Linux
- setoolkit

### Configurando o Phishing no Kali Linux

- Acesso root: ``` sudo su ```
- Iniciando o setoolkit: ``` setoolkit ```
- Tipo de ataque: ``` Social-Engineering Attacks ```
![Alt text](./opc1.png "Optional title")
  
- Vetor de ataque: ``` Web Site Attack Vectors ```
![Alt text](./opc2.png "Optional title")
  
- Método de ataque: ```Credential Harvester Attack Method ```
![Alt text](./opc3.png "Optional title")
  
- Método de ataque: ``` Site Cloner ```
  
![Alt text](./opc4.png "Optional title")
  
- Obtendo o endereço da máquina: ``` ifconfig ``` ou utilizando o próprio endereço ip sugerido 
![Alt text](./ip.png "Optional title")

- URL para clone: https://cursos.alura.com.br/loginForm
![Alt text](./clone.png "Optional title")


### Resutados

- Informando um usuário e senha:
  
![Alt text](./login.png "Optional title")

- Usuário e senha capturados:
![Alt text](./CapturaDeSenha.png "Optional title")


### Informes
-Antes de funcionar o Phishing ocorreram alguns erros em relação a captura da senha por conta de um bug --> "AttributeError: module 'cgi' has no attribute 'escape'"
-Esse erro ocorre porque, a partir do Python 3.8, o método cgi.escape() foi removido. Esse método era utilizado para converter caracteres especiais em entidades HTML.
-Para resolver esse erro é necessário modificar no arquivo python "cgi.escape("PARAM: " + line + "\n")" para html.escape("PARAM: " + line + "\n")

``` Passos: ```
- Abrir o explorador de arquivos no endereço: /usr/share/set/src/webattack/harvester/harvester.py:
![Alt text](./pasta.png "Optional title")

- Importar o html:
![Alt text](./import_html.png "Optional title")

- Mudar o codigo cgi.escape("PARAM: " + line + "\n") para html.escape("PARAM: " + line + "\n"):
![Alt text](./alteração.png "Optional title")

- Após essas alterações é só salvar e testar
- Link para vídeo de explicação no youtube: https://youtu.be/aM5yjJ8JUME?si=wRDORgmeoqcl-1s4


