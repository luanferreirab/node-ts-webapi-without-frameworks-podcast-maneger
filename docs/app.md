# Podcast Flow

### Descrição 

 Um app ao estilo netflix, aonde eu possa centralizar diferentes episódios podcasts separados por categoria

### Dominio

 PodCasts feitos em video

### Features

- Listar os episódios podcasts em sessões de categorias
    - [saúde, fitness, mentalidade, humor]
- Filtrar episódios por nome de podcast 

## Como 

#### Feature: 
- Listar os episódios podcasts em sessões de categorias

#### Como vou implementar:
 
 GET: retorna lista de episódios


response: 

```js
[
{
    podcastName: "flow",
    episode: "CBUM - Flow #319",
    videoId: "sachJnl9ofs&pp=ygUHcG9kY2FzdA%3D%3D",
    cover: "https://img.freepik.com/fotos-gratis/microfone-retro-isolado-no-fundo-da-cor_1387-912.jpg",
    link: "https://www.youtube.com/watch?v=sachJnl9ofs&pp=ygUHcG9kY2FzdA%3D%3D",
    category: ["saúde", "esporte" , "fitness"]
},
{
    podcastName: "flow",
    episode: "Rubens Barrichelo - Flow #339",
    videoId: "sachJnl9ofs&pp=ygUHcG9kY2FzdA%3D%3D",
    cover: "https://img.freepik.com/fotos-gratis/microfone-retro-isolado-no-fundo-da-cor_1387-912.jpg",
    link: "https://www.youtube.com/watch?v=sachJnl9ofs&pp=ygUHcG9kY2FzdA%3D%3D",
    category: ["esporte" , "corrida"]
},
]
```


 GET: retorna lista de episódios baseado em um parametro enviado pelo cliente do nome do podcast