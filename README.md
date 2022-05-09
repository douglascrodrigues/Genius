# Top 10 Músicas mais tocadas por Artista
Integração com a API do Genius, top 10 músicas mais tocadas de um determinado artista.
Utilizado Flask RestFull, Redis e DynamoDB.

### Requisitos:
- Python 3+
- Redis Server 3.0
- DynamoDB Server (ou instância rodando na AWS)

### Como configurar o ambiente:

• Após configurar o arquivo "venv", você precisará instalar os requisitos do projeto com o seguinte comando:

```pip install -r requirements.txt```

• Pronto! Configurado. Se tudo deu certo nos passos anteriores, agora você só precisa abrir o "Command Prompt" ou "bash" e rodar o seguinte comando na pasta:
 *Windows
```python app.py```
ou simplesmente:
```python -m app.py```

### Como consultar os dados do Artista na API:
- Você precisa fazer uma requisição com o método "GET" para a url a seguir:
```http://127.0.0.1:5000/musicas/nome_do_artista```
Atenção: substitua nome_do_artista pelo nome do seu artista favorito

### Retorno dos dados da API:
- Se sua requisição funcionou corretamente, você receberá o seguinte retorno (exemplo):

```
{
    "lista_de_musica": [
        "HUMBLE. by Kendrick Lamar",
        "Fuckin' Problems by A$AP Rocky (Ft. 2 Chainz, Drake & Kendrick Lamar)",
        " m.A.A.d city by Kendrick Lamar (Ft. MC Eiht)",
        "Swimming Pools (Drank) by Kendrick Lamar",
        "DNA. by Kendrick Lamar",
        "Money Trees by Kendrick Lamar (Ft. Jay Rock)",
        "XXX. by Kendrick Lamar (Ft. U2)",
        " goosebumps by Travis Scott (Ft. Kendrick Lamar)",
        "Bitch, Don't Kill My Vibe by Kendrick Lamar",
        "Control by Big Sean (Ft. Jay Electronica & Kendrick Lamar)"
    ],
    "nome_artista": "Kendrick Lamar",
    "pesquisado": "Kendrick Lamar"
}
```

- Caso contrário, você receberá uma mensagem similar a esta com o campo "status" marcado como "error", exemplo:

```
{
  null
}
```

![image](https://user-images.githubusercontent.com/38405352/167323876-a4e91e33-4f43-451a-b0db-58bb5b191e0f.png)

