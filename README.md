# minicurso-git
*link da aula:*
https://bald-quicksand-e2e.notion.site/Roteiro-de-pr-tica-bf601afe683e4ab9bdfd204f266aa1fe


### comandos utilizados 

Crie um diretório chamado “pratica_git” e entre nele.

```bash
    $ mkdir pratica_git 

    $ cd pratica_git
```

--------------------------------------------------------------------------------------------------
Estando dentro do repositório, inicialize um repositório git.
```bash
    $ git init

    $ git branch -M main
```

--------------------------------------------------------------------------------------------------
Agora, adicione o arquivo “index.html” e realize um commit.

```bash
    $ touch index.html

    $ git add index.html

    $ git commit -m "Commit inicial"
```

--------------------------------------------------------------------------------------------------
Verifique o status do repositório criado.
```bash
    $ git status

    On branch main

    nothing to commit, working tree clean
```

Como não há nenhuma mudança ou arquivo novo/deletado, não há nada para commitar.

--------------------------------------------------------------------------------------------------

- Depois de ter criado o arquivo “index.html”, é hora de modificá-lo. Para isso, abra-o em um editor de texto (Visual Studio Code por exemplo) e cole o seguinte trecho de código nele.
    
    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <link rel="stylesheet" href="styles.css">
        <title>Git is awesome!</title>
    </head>
    <body>
        <main>
            <h1>Minha página</h1>
            <article>
                <header>
                    <h2>Minhas boas vindas</h2>
                    <time>19/10/2023</time>
                </header>
                <p>Fale alguma coisa sobre você aqui neste parágrafo ou deixe o texto como está.</p>
                <footer>
                    <p>Este texto foi escrito por {seu_nome_aqui}</p>
                    <p>
                        Algum outro texto <em>"em itálico"</em>
                    </p>
                </footer>
            </article>
        </main>
    </body>
    </html>
    ```
    
  --------------------------------------------------------------------------------------------------  
- Depois de adicionar o trecho de código acima, veja o estado do repositório.
    
    ```bash
   $ git status
    
    On branch main
    Changes not staged for commit:
      (use "git add <file>..." to update what will be committed)
      (use "git restore <file>..." to discard changes in working directory)
    	modified:   index.html
    
    no changes added to commit (use "git add" and/or "git commit -a")
    ```
    
- Perceba que agora que há mudanças sendo mostradas na saída do comando `git status`. Tais mudanças foram identificadas no arquivo “index.html”.

--------------------------------------------------------------------------------------------------

- Para dizer ao Git para adicionar à área de transferência as mudanças, você pode usar o seguinte comando:
    
    ```bash
    $ git add <nome_do_arquivo>
    ```
    
- Para verificar o status do Git você pode usar o comando
    
    ```bash
    $ git status
    
    On branch main
    Changes to be committed:
      (use "git restore --staged <file>..." to unstage)
    	modified:   index.html
    ```
    
- Isso permite que você acompanhe as mudanças no seu projeto antes de confirmar as alterações com um commit.

--------------------------------------------------------------------------------------------------

- Agora, é hora de adicionar mais um arquivo. Para isso, crie um arquivo conforme o comando abaixo.
    ```bash
    $ touch styles.css
    ```
​
- Feito isso, abra o arquivo criado anteriormente no Visual Studio Code e insira a folha de estilos abaixo dentro dele.
  ```
    :root {
        --footer-font-size: 0.925em;
        --footer-text-color: #5F5F5F;
        --random-color: #FF0000;
    }
    
    body {
        font-family: Arial, Helvetica, sans-serif;
        padding: 10px;
    }
    
    p {
        width: max(300px, 20%);
        text-align: justify;
        text-justify: inter-word;
    }
    
    h2 {
        color: var(--random-color);
    }
    
    footer > p {
        font-size: var(--footer-font-size);
        color: var(--footer-text-color);
    }
    ```
- Agora, adicione o arquivo “styles.css” para que ele saia de untracked (não rastreado pelo Git) e possa ser adicionado ao Git.
  ```bash
    *$ git add styles.css*
  ```
​
- Por fim, realize um commit com uma mensagem que descreva bem as alterações introduzidas por ele.
  ```bash
    $ git commit -m "Adicionando a estrutura do index.html e colocando uma folha de estilo por meio do styles.css"
  ```
​
- Desse modo, se você rodar um comando git status novamente, não haverá alterações.
  ```bash
    *$ git status*

    On branch main
    nothing to commit, working tree clean
  ```

--------------------------------------------------------------------------------------------------
