**Sistemas Operacionais Linux**

Baseado em todo o conhecimento adquirido durante o módulo, realize as práticas sugeridas e em seguida, documente todo o processo realizado usando printscreens sempre que possível. Ao final, gere um PDF e envie para o e-mail do instrutor.

**Nota:** O arquivo deve ser enviado com o seu nome e sobrenome, exemplo: nome-sobrenome.pdf

**Assuntos que serão abordados:**

**Problema 1:**

Imagine que a Vanessa é uma administradora de sistemas em uma empresa de tecnologia. Ela recebeu a tarefa de criar uma nova conta de usuário para um novo membro da equipe. Vanessa precisa demonstrar seu conhecimento ao explicar o processo para seus colegas de trabalho.

**Descreva o processo para criar um novo usuário no Linux, incluindo os comandos e opções utilizadas de forma mais detalhada possível.**

1. Abra um terminal navegando atraves do sistema ou pelo atalho **ctrl+alt+t**
![image](https://github.com/daviamarall/Vem-Ser-Tech---DevOps/assets/40430859/57957e1f-af93-4548-9fb5-6c754a852718)

2. Use o comando `sudo adduser` para criar um novo usuário. Substitua "nome_de_usuário" pelo nome que você deseja atribuir ao novo usuário:
   
   ```bash
   sudo adduser nome_de_usuário
   ```

3. Pressione Enter e siga as instruções para definir uma senha para o novo usuário.

4. Forneça informações adicionais sobre o novo usuário, como Nome completo, Número da sala, Número de telefone, etc., ou deixe em branco pressionando Enter.

5. Confirme se as informações estão corretas, pressionando "Y" para aceitar ou "N" para rejeitar.

6. O novo usuário foi criado com sucesso.

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

- Para definir permissões "400" recursivamente (leitura somente para o proprietário), use o seguinte comando:

```bash
chmod -R 400 minha_pasta
```

Agora, explique que as permissões de arquivo no Linux são representadas por três grupos de símbolos: `r` (leitura), `w` (escrita) e `x` (execução), e que esses símbolos são atribuídos a três grupos: o proprietário, o grupo e outros. No exemplo, "400" significa que o proprietário tem permissão de leitura (r) e os outros não têm permissão (---) para todos os arquivos e a pasta.

**Problema 3:**

Em uma cidade futurística chamada Adalandia, existe uma equipe de jovens DevOps liderada pela Andreza. Eles estão trabalhando em um novo projeto e precisam configurar um servidor web para hospedar sua aplicação. Andreza, como líder do time, guia seus colegas pelo processo de instalação e configuração do servidor Nginx, compartilhando suas experiências passadas com a ferramenta e fornecendo orientações detalhadas para garantir uma configuração correta.

**Descreva o processo para instalar e configurar o servidor Web Nginx no Linux. O Objetivo é alterar a página Default do Nginx para os seguintes caracteres:**

```
ADA + AdaTech + seu_nome = Sucesso!
```

**Apenas esse texto deve ser renderizado na página padrão do servidor. Não esqueça de tirar um print e documentar tudo que foi feito até chegar a esse resultado.**

1. Abra um terminal.

2. Use o seguinte comando para instalar o servidor Nginx:

```bash
sudo apt-get install nginx
```

3. Após a instalação, inicie o serviço Nginx com o comando:

```bash
sudo systemctl start nginx
```

4. Para habilitar o Nginx para iniciar automaticamente com o sistema, use o comando:

```bash
sudo systemctl enable nginx
```

5. Agora, edite o arquivo de configuração padrão do Nginx usando um editor de texto. Vamos usar o nano neste exemplo:

```bash
sudo nano /etc/nginx/sites-available/default
```

6. No arquivo de configuração, encontre a seção que define a página padrão e substitua o conteúdo pelo texto desejado:

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

7. Salve as alterações no arquivo de configuração.

8. Teste a configuração do Nginx para verificar se não há erros:

```bash
sudo nginx -t
```

9. Se não houver erros, reinicie o serviço Nginx para aplicar as alterações:

```bash
sudo systemctl restart nginx
```

10. Agora, abra um navegador da web e acesse
