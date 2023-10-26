**Sistemas Operacionais Linux**

**Problema 1:**

Imagine que a Vanessa é uma administradora de sistemas em uma empresa de tecnologia. Ela recebeu a tarefa de criar uma nova conta de usuário para um novo membro da equipe. Vanessa precisa demonstrar seu conhecimento ao explicar o processo para seus colegas de trabalho.

**Descreva o processo para criar um novo usuário no Linux, incluindo os comandos e opções utilizadas de forma mais detalhada possível.**

**Resolução: **

step 1. Abra um terminal navegando atraves do sistema ou pelo atalho **ctrl+alt+t**
![image](https://github.com/daviamarall/Vem-Ser-Tech---DevOps/assets/40430859/57957e1f-af93-4548-9fb5-6c754a852718)
![image](https://github.com/daviamarall/Vem-Ser-Tech---DevOps/assets/40430859/33f81cc0-134d-49a7-bfc7-71e60c41ebf3)


step 2. Use o comando `sudo adduser` para criar um novo usuário. Substitua "nome_de_usuário" pelo nome que você deseja atribuir ao novo usuário:
   
   ```bash
   sudo adduser nome_de_usuário
   ```
![image](https://github.com/daviamarall/Vem-Ser-Tech---DevOps/assets/40430859/7bd733fb-12a8-4e39-88c1-a2429a67da7c)

step 3. Pressione Enter e siga as instruções para definir uma senha para o novo usuário.

![image](https://github.com/daviamarall/Vem-Ser-Tech---DevOps/assets/40430859/7c0e80f7-d448-4977-8b46-7bdfb2fc4fe5)

step 4. Forneça informações adicionais sobre o novo usuário, como Nome completo, Número da sala, Número de telefone, etc., ou deixe em branco pressionando Enter.

![image](https://github.com/daviamarall/Vem-Ser-Tech---DevOps/assets/40430859/013ff272-ac50-403d-aef2-ff7f8d3fa411)

step 5. Confirme se as informações estão corretas, pressionando "Y" para aceitar ou "N" para rejeitar.

![image](https://github.com/daviamarall/Vem-Ser-Tech---DevOps/assets/40430859/6c91029c-2eb1-4062-be2a-a90157172b8b)

step 6. O novo usuário foi criado com sucesso.

![image](https://github.com/daviamarall/Vem-Ser-Tech---DevOps/assets/40430859/15a5191a-1e95-42d2-899c-4d5f3ab60b6e)


**Problema 2:**

Em uma pequena cidade chamada Linuxville, vive o Lucas, um entusiasta de tecnologia. Ele está ajudando seu amigo Rafael a entender o funcionamento das permissões de arquivo no sistema Linux. Lucas decide contar uma história, explicando que os arquivos em Linux são como valiosos tesouros guardados em cofres. Cada cofre possui uma combinação única de permissões, representadas por símbolos especiais. Lucas usa essa analogia para explicar como as permissões de arquivo são representadas e qual o acesso que cada símbolo representa.

**Crie uma Pasta qualquer e 5 arquivos de texto. Em seguida define as permissões 400 para a pasta e todos os arquivos recursivamente. Use esse exemplo para explicar o que são as permissões de arquivo no Linux e como elas são representadas de forma mais detalhada possível.**

- Crie uma pasta usando o comando `mkdir` e cinco arquivos de texto usando o comando `touch`.

```bash
mkdir minha_pasta
touch minha_pasta/arquivo1.txt
touch minha_pasta/arquivo2.txt
touch minha_pasta/arquivo3.txt
touch minha_pasta/arquivo4.txt
touch minha_pasta/arquivo5.txt
```

Exemplo: 

![image](https://github.com/daviamarall/Vem-Ser-Tech---DevOps/assets/40430859/b78f45be-8e27-49d9-8098-d00237793ac0)


- Para definir permissões "400" recursivamente (leitura somente para o proprietário), use o seguinte comando:

```bash
chmod -R 400 minha_pasta
```
Exemplo: 

![image](https://github.com/daviamarall/Vem-Ser-Tech---DevOps/assets/40430859/06b1a444-9a86-4d23-bfd6-5439bc23139a)

No exemplo, "400" significa que o proprietário tem permissão de leitura (r) e os outros não têm permissão (---) para todos os arquivos e a pasta.

**Problema 3:**

Em uma cidade futurística chamada Adalandia, existe uma equipe de jovens DevOps liderada pela Andreza. Eles estão trabalhando em um novo projeto e precisam configurar um servidor web para hospedar sua aplicação. Andreza, como líder do time, guia seus colegas pelo processo de instalação e configuração do servidor Nginx, compartilhando suas experiências passadas com a ferramenta e fornecendo orientações detalhadas para garantir uma configuração correta.

**Descreva o processo para instalar e configurar o servidor Web Nginx no Linux. O Objetivo é alterar a página Default do Nginx para os seguintes caracteres:**

```
ADA + AdaTech + seu_nome = Sucesso!
```

**Apenas esse texto deve ser renderizado na página padrão do servidor. Não esqueça de tirar um print e documentar tudo que foi feito até chegar a esse resultado.**

step 1. Abra um terminal.

step 2. Use o seguinte comando para instalar o servidor Nginx:

```bash
sudo apt-get install nginx
```
![image](https://github.com/daviamarall/Vem-Ser-Tech---DevOps/assets/40430859/3c44ac20-4c9b-4093-a098-7f96b81f507d)

step 3. Após a instalação, inicie o serviço Nginx com o comando:

```bash
sudo systemctl start nginx
```
![image](https://github.com/daviamarall/Vem-Ser-Tech---DevOps/assets/40430859/b112284f-8832-4d65-942f-7bbd0f49e034)

step 4. Para habilitar o Nginx para iniciar automaticamente com o sistema, use o comando:

```bash
sudo systemctl enable nginx
```
![image](https://github.com/daviamarall/Vem-Ser-Tech---DevOps/assets/40430859/91d5de53-633c-49bd-b5e6-0e9996b41254)

step 5. Agora, edite o arquivo de configuração padrão do Nginx usando um editor de texto. Vamos usar o nano neste exemplo:

```bash
sudo nano /etc/nginx/sites-available/default
```
![image](https://github.com/daviamarall/Vem-Ser-Tech---DevOps/assets/40430859/16a8873d-ce5f-4156-a683-5d4ef0efa90f)

step 6. No arquivo de configuração, encontre a seção que define a página padrão e substitua o conteúdo pelo texto desejado:

```plaintext
server {
    listen 80 default_server;
    listen [::]:80 default_server;

    root /var/www/html;
    index index.html index.htm;

    location / {
        try_files $uri $uri/ =404;
    }

    # Substitua este bloco com o texto desejado
    location / {
        return 200 "ADA + AdaTech + seu_nome = Sucesso!";
    }
}
```
![image](https://github.com/daviamarall/Vem-Ser-Tech---DevOps/assets/40430859/016869cb-d6af-46d3-ba43-d655fd9d23ea)

step 7. Salve as alterações no arquivo de configuração.

step 8. Teste a configuração do Nginx para verificar se não há erros:

```bash
sudo nginx -t
```
![image](https://github.com/daviamarall/Vem-Ser-Tech---DevOps/assets/40430859/f668e845-2206-4d08-bcf3-45257a0c13fc)

step 9. Se não houver erros, reinicie o serviço Nginx para aplicar as alterações:

```bash
sudo systemctl restart nginx
```
![image](https://github.com/daviamarall/Vem-Ser-Tech---DevOps/assets/40430859/f8df0f9e-1706-4f33-982d-5bcd8be77c2d)

step 10. Agora, abra um navegador da web e acesse

![image](https://github.com/daviamarall/Vem-Ser-Tech---DevOps/assets/40430859/e755312d-31e0-45d4-927f-e2aa4ce99c50)
