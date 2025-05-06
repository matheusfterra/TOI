# 🧾 PRD – Plataforma TOI

## 🎯 Objetivo do Produto

A plataforma TOI tem como objetivo gamificar a participação de ciradores de conteúdo em campanhas de divulgação nas redes sociais (Instagram e facebook), permitindo o acompanhamento de performance por métricas, ranqueamento dos participantes e gerenciamento administrativo completo de campanhas e conteúdos gerados.

---

## 👥 Perfis de Usuário

### 1. Usuário Comum (Criador de conteúdo)

- Login via Instagram (simulação de login OAuth – acesso direto ao painel após clique).
- Acesso a um marketplace de campanhas disponíveis.
- Pode se candidatar a campanhas específicas.
- Acompanhamento de ranking por campanha.
- Visualização das próprias posições e métricas.
- Recebe notificações de novidades.

### 2. Administrador (Equipe Interna)

- Login padrão: usuário: admin / senha: admin
- Acesso total ao painel administrativo com recursos para:
  - Criar, editar e encerrar campanhas.
  - Definir hashtag da campanha.
  - Escolher imagem, prêmios, datas (início e término).
  - Selecionar métricas a serem avaliadas:
    - Visualizações de vídeos
    - Curtidas
    - Compartilhamentos
    - Salvamentos
    - Comentários
  - Exportar dados da campanha em CSV ou PDF.
  - Acompanhar ranking e comentários com análise de IA.
  - Gerenciar galeria de conteúdos.

---

## 📦 Funcionalidades da Plataforma

### A. Login

- Tela com duas opções:
  - Login como admin (usuário/senha padrão).
  - Login com Instagram.
- Exibe logo da empresa.
- Interface clean, moderna, com modo escuro.
- Paleta principal: #FF6C0E

### B. Marketplace de Campanhas

- Exibe campanhas disponíveis com:
  - Imagem
  - Título
  - Hashtag
  - Datas
  - Botão para se candidatar
- Modal de candidatura com descrição e confirmação.

### C. Ranking

- Seleção de campanha para visualizar ranking.
- Destaque para o Top 3 (estilo pódio com ícones).
- Tabela com:
  - Nome de usuário
  - Foto de perfil
  - Métricas da campanha
  - Filtros e ordenações

### D. Painel de Métricas do Admin

- A plataforma coleta automaticamente todas as publicações do perfil do usuário autenticado.
- Os descritivos (legendas) das publicações são avaliados para identificar o uso da hashtag oficial da campanha.
- Somente publicações com a hashtag válida são consideradas nas métricas e rankings.
- Para essas publicações, são coletadas as métricas de performance (curtidas, comentários, visualizações, etc.).
- Também são coletadas métricas de perfil (como localização e faixa etária do público) para avaliar o alcance qualitativo da campanha.

- Exibe:
  - Top 10 usuários com melhor desempenho
  - Tabela completa de métricas individuais:
    - Visualizações
    - Curtidas
    - Compartilhamentos
    - Salvamentos
    - Comentários
- Cada linha com botão “Visualizar Post” (modal).

### E. Análise de Comentários (via IA)

- Sentimento: Positivo, Negativo, Neutro, Misto
- Categoria: Elogio, Reclamação, Dúvida, Sugestão
- Gráficos: pizza ou barras
- Modal com conteúdo completo dos comentários e análises

### F. Galeria de Conteúdos do Admin

- Item de menu: Galeria de Conteúdos
- Exibe conteúdos gerados nas campanhas (via hashtag)
- Grade com thumbnails
- Modal com preview completo, legenda e métricas
- Ações:
  - Marcar com ícone
  - Adicionar/remover da galeria
  - Atribuir etiquetas (ex: “Contato futuro”, “Premiar”)
  - Filtros por etiquetas e campanha

### G. Agendamento de Publicações no Instagram

- Usuário pode agendar conteúdo para publicação futura
- Sistema realiza postagem automática no horário definido

### H. Gerenciamento de DMs do Instagram

- Plataforma exibe DMs recebidas
- Possibilidade de responder diretamente via plataforma

### I. Gerenciamento de Comentários em Publicações

- Plataforma exibe comentários recebidos nas publicações marcadas com a hashtag da campanha
- Comentários são listados com autor, data e conteúdo
- Possibilidade de moderar (ocultar, excluir ou marcar) comentários
- Permite responder aos comentários diretamente pela plataforma
- Modal de visualização para cada comentário com contexto da publicação
- Comentários também alimentam o módulo de Análise de Sentimento via IA

---

## 🔐 Permissões Necessárias e Uso

| Permissão                   | Finalidade                                                               |
| --------------------------- | ------------------------------------------------------------------------ |
| `email`                     | Obter e-mail do usuário (identificação básica)                           |
| `public_profile`            | Obter nome, foto e informações públicas do perfil                        |
| `pages_show_list`           | Listar páginas do Facebook associadas ao usuário                         |
| `pages_read_engagement`     | Coletar métricas de engajamento de páginas e conectar Instagram Business |
| `pages_read_user_content`   | Ler conteúdo gerado por usuários nas páginas (comentários/posts)         |
| `pages_messaging`           | Enviar/ler mensagens via Messenger das páginas do Facebook               |
| `business_management`       | Gerenciar conexões entre páginas e contas comerciais                     |
| `instagram_basic`           | Acessar dados do perfil e mídias públicas do Instagram                   |
| `instagram_manage_insights` | Coletar métricas de performance (alcance, engajamento, demografia)       |
| `instagram_manage_comments` | Ler/moderar comentários em publicações                                   |
| `instagram_messaging`       | Acesso a DMs via webhook do Instagram                                    |
| `instagram_manage_messages` | Gerenciamento completo de threads de mensagens diretas                   |
| `instagram_content_publish` | Publicar conteúdo/agendar posts diretamente via plataforma               |

---

Este PRD é base para construção, integração e submissão do app para aprovação junto à Meta, conforme exigências da plataforma e política de uso da API do Instagram e Facebook.
