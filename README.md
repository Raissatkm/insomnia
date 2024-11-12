## Documentação para Uso do Insomnia

**Insomnia** é uma ferramenta para testar APIs de forma fácil e intuitiva, permitindo realizar requisições HTTP e visualizar as respostas. 

### 1. Instalação

1. Acesse o [site oficial do Insomnia](https://insomnia.rest/) e baixe o programa para o seu sistema operacional.
2. Após o download, instale o Insomnia seguindo as instruções do instalador.

### 2. Interface e Conceitos Básicos

- **Workspace**: Área onde você organiza seus projetos e requisições.
- **Collections**: Conjunto de requisições agrupadas, como uma pasta.
- **Requests**: Cada requisição individual com informações como URL, método e parâmetros.
- **Environment**: Variáveis de ambiente que permitem configurar dados como URLs base ou tokens de autenticação.

### 3. Criando um Workspace e uma Collection

1. Abra o Insomnia e clique em **New Workspace** para criar um novo espaço de trabalho.
2. Dê um nome ao workspace e escolha a opção **Design** (para APIs REST) ou **Debug** (para testar requisições).
3. Clique em **New Collection** para organizar suas requisições.

### 4. Realizando uma Requisição HTTP Básica

1. Dentro da sua collection, clique em **New Request**.
2. Nomeie a requisição e selecione o método HTTP (GET, POST, PUT, DELETE, etc.).
3. Insira a URL da API no campo de endereço.
4. Se a requisição precisar de parâmetros, configure-os nas abas:
   - **Query**: Para parâmetros na URL (como `?key=value`).
   - **Body**: Para o conteúdo enviado em requisições POST, PUT, PATCH.
   - **Headers**: Para adicionar cabeçalhos, como `Authorization` para autenticação.
5. Clique em **Send** para enviar a requisição.

### 5. Adicionando Autenticação

1. No menu da requisição, vá até **Auth**.
2. Escolha o tipo de autenticação necessário (por exemplo, **Bearer Token** para APIs que utilizam tokens).
3. Insira o valor do token no campo correspondente.
4. Salve as configurações e envie a requisição.

### 6. Gerenciando Variáveis de Ambiente

1. Clique em **Manage Environments** (ícone de engrenagem).
2. Clique em **Add Environment** e defina variáveis como:
   ```json
   {
     "baseURL": "https://api.exemplo.com",
     "token": "seu_token_aqui"
   }
   ```
3. Ao configurar a URL ou cabeçalhos, use as variáveis:
   ```
   {{ baseURL }}/endpoint
   ```
   Isso facilita atualizações, bastando alterar o valor na configuração de ambiente.

### 7. Testando e Analisando Respostas

- Após enviar a requisição, visualize a resposta na área inferior da tela.
- Insomnia exibe informações da resposta como status HTTP, tempo de resposta, e o corpo da resposta (JSON, XML, etc.).
- Você pode copiar partes da resposta para reutilizar em outras requisições.

### 8. Organizando com Pastas e Sub-Collections

- No painel da coleção, clique com o botão direito e selecione **New Folder** para criar uma pasta dentro da sua coleção, útil para agrupar requisições similares.
  
### 9. Exportando e Importando Collections

- Para exportar uma coleção, clique com o botão direito sobre ela e escolha **Export**. 
- Para importar, clique em **Import/Export** no canto superior direito e selecione o arquivo de exportação (.json).

### 10. Dicas Extras

- **Snapshots**: Use **Request Snapshots** para armazenar a resposta de uma requisição específica.
- **Plugins**: O Insomnia possui suporte para plugins que estendem suas funcionalidades, como autenticação automática.
