# Podcast Flow

## Descrição
Podcast Flow é um aplicativo inspirado no estilo Netflix, projetado para centralizar diferentes episódios de podcasts organizados por categoria. É voltado para podcasts em vídeo.

## Funcionalidades

- **Listar episódios por categoria**: Saúde, fitness, mentalidade, humor.
- **Filtrar episódios por nome de podcast**.

## Como Funciona

O projeto utiliza o módulo `http` do Node.js para lidar com requisições e respostas HTTP. Os episódios de podcast podem ser listados ou filtrados através de duas rotas principais.

### Listar Episódios por Categoria

- **GET**: Retorna uma lista de episódios.
  
  **Resposta**:
  ```json
  [
      {
          "podcastName": "flow",
          "episode": "CBUM - Flow #319",
          "videoId": "sachJnl9ofs&pp=ygUHcG9kY2FzdA%3D%3D",
          "cover": "https://img.freepik.com/fotos-gratis/microfone-retro-isolado-no-fundo-da-cor_1387-912.jpg",
          "link": "https://www.youtube.com/watch?v=sachJnl9ofs&pp=ygUHcG9kY2FzdA%3D%3D",
          "category": ["saúde", "esporte", "fitness"]
      },
      {
          "podcastName": "flow",
          "episode": "Rubens Barrichelo - Flow #339",
          "videoId": "sachJnl9ofs&pp=ygUHcG9kY2FzdA%3D%3D",
          "cover": "https://img.freepik.com/fotos-gratis/microfone-retro-isolado-no-fundo-da-cor_1387-912.jpg",
          "link": "https://www.youtube.com/watch?v=sachJnl9ofs&pp=ygUHcG9kY2FzdA%3D%3D",
          "category": ["esporte", "corrida"]
      }
  ]
  ```

Claro, aqui estão as tecnologias utilizadas com hiperlinks em Markdown para suas respectivas documentações:

---

## Tecnologias Utilizadas

Este projeto utiliza as seguintes tecnologias:

- **[Node.js](https://nodejs.org/)**: Ambiente de execução para JavaScript que permite executar código fora de um navegador.
- **[TypeScript](https://www.typescriptlang.org/)**: Uma linguagem de programação desenvolvida e mantida pela Microsoft que adiciona tipagem estática opcional ao JavaScript.
- **[TSX](https://github.com/esbuild-kit/tsx)**: Uma ferramenta para executar scripts TypeScript sem precisar de um build step.
- **[Tsup](https://github.com/egoist/tsup)**: Um empacotador zero-configuração que ajuda a compilar TypeScript e JavaScript para vários formatos, otimizando o processo de distribuição.

### Dependências de Desenvolvimento

- **[@types/node](https://www.npmjs.com/package/@types/node)**: Tipos TypeScript para Node.js, fornecendo definições de tipo para o ambiente Node.
- **[typescript](https://www.npmjs.com/package/typescript)**: Utilizado para compilar e verificar tipos de código TypeScript.

Estas tecnologias foram escolhidas para fornecer uma base sólida para o desenvolvimento, teste e implantação da aplicação de podcast.

---

Sinta-se à vontade para ajustar as descrições ou adicionar mais informações conforme necessário para melhor refletir o seu projeto.

- **GET**: Retorna uma lista de episódios baseado em um parâmetro enviado pelo cliente com o nome do podcast.


## Instalação

1. Clone o repositório:
   ```bash
   git clone https://github.com/seuusuario/podcast-flow.git
   ```

2. Navegue para o diretório do projeto:
   ```bash
   cd podcast-flow
   ```

3. Instale as dependências:
   ```bash
   npm install
   ```

4. Inicie o aplicativo:
   ```bash
   npm start
   ```

## Contribuição

Contribuições são bem-vindas! Por favor, siga as etapas abaixo para contribuir:

1. Faça um fork do projeto.
2. Crie uma branch para a sua funcionalidade (`git checkout -b feature/nova-funcionalidade`).
3. Faça commit das suas alterações (`git commit -m 'Adiciona nova funcionalidade'`).
4. Faça push para a branch (`git push origin feature/nova-funcionalidade`).
5. Abra um Pull Request.

## Licença

Este projeto está sob a licença [MIT](LICENSE).
