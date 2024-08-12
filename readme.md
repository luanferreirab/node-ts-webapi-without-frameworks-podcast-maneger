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

### Filtrar Episódios por Nome de Podcast

- **GET**: Retorna uma lista de episódios baseado em um parâmetro enviado pelo cliente com o nome do podcast.

### Estrutura de Código

O código principal é gerenciado pelo seguinte módulo:

```javascript
import * as http from "http";
import { getFilterEpisodes, getListEpisodes } from "./controllers/podscasts-controller";
import { Routes } from "./routes/routes";
import { HttpMethod } from "./utils/http-methods";

export const app = async (request: http.IncomingMessage, response: http.ServerResponse) => {
    const baseUrl = request.url?.split("?")[0];

    if(request.method === HttpMethod.GET && baseUrl === Routes.LIST) {
        await getListEpisodes(request, response);
    } 
    if (request.method === HttpMethod.GET && baseUrl === Routes.EPISODE) {
        await getFilterEpisodes(request, response);
    }
}
```

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
