# 🎵 Graph-Based Music Recommendation System

Sistema de recomendação de músicas baseado em grafos, utilizando Neo4j e Cypher, com suporte à aplicação de algoritmos de Graph Data Science (GDS) para descoberta de padrões de escuta e recomendação personalizada.

## 📌 Visão Geral

Este projeto modela um domínio musical por meio de um grafo semântico, onde usuários, músicas, artistas, gêneros e playlists são representados como nós, e suas interações como arestas rotuladas.

O objetivo é demonstrar como bancos de dados orientados a grafos podem ser utilizados para:

Representar relações complexas

Identificar similaridade entre usuários e conteúdos

Apoiar sistemas de recomendação modernos

## 🧠 Tecnologias Utilizadas

Neo4j (Banco de Dados em Grafo)

Cypher Query Language

Neo4j Graph Data Science (GDS)

Modelagem conceitual orientada a grafos

## 🧩 Modelagem do Grafo
### Tipos de Nós
| Nó         | Descrição                    |
| ---------- | ---------------------------- |
| `User`     | Usuário da plataforma        |
| `Music`    | Faixa musical                |
| `Artist`   | Artista                      |
| `Genre`    | Gênero musical               |
| `Playlist` | Playlist criada por usuários |

### Tipos de Relacionamentos
| Relacionamento     | Origem → Destino | Significado           |
| ------------------ | ---------------- | --------------------- |
| `LISTENED`         | User → Music     | Interação de escuta   |
| `LIKED`            | User → Music     | Preferência explícita |
| `FOLLOW_ARTIST`    | User → Artist    | Afinidade             |
| `CREATED`          | Artist → Music   | Autoria               |
| `BELONGS_TO`       | Music → Genre    | Classificação         |
| `CREATED_PLAYLIST` | User → Playlist  | Criação               |
| `HAS_MUSIC`        | Playlist → Music | Curadoria             |
