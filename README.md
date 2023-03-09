# App-musica
Este é um repositório com o projeto final do módulo Lógica de Programação II da formação em Python e Dados da Ada Tech.

Você pode acessar o projeto aqui: [Projeto_Final.ipynb](/Projeto_Final.ipynb)

# Sobre o aplicativo
Este aplicativo consiste em um programa simulando um aplicativo de streaming. Ele tem uma base de dados de músicas, artistas, álbuns e playlists. Um administrador pode salvar novos artistas, músicas e álbuns, enquanto um usuário comum pode criar playlists. Segue uma breve descrição das funcionalidades.

## Fluxos
Ao abrir o programa, ele oferece um menu com exatamente 3 opções: logar como administrador, logar como usuário ou sair.

**Admin** - O menu de admin oferece 2 opções:
- Registrar artista
- Registrar álbum
- Sair

No primeiro caso, o admin digita o nome de um novo artista. Caso o nome ainda não exista na base, ele será criado.
No segundo caso, o admin deve digitar primeiramente o artista - o artista precisa já existir. Em seguida o programa pergunta quantas músicas o álbum terá e pergunta o nome de cada uma. O álbum é criado e a estrutura do artista é atualizada para contabilizar o álbum novo.

**Usuário** - O menu de usuário também oferece 2 opções:
- Buscar playlist
- Criar playlist
- Sair

Caso o usuário opte por buscar uma playlist, mais um menu é exibido:
- Buscar por música
- Buscar por artista
- Buscar por nome

Caso o usuário escolha a primeira opção, é pedido para ele digitar uma música e são exibidas todas as playlists contendo músicas com aquele nome. Um procedimento análogo é adotado para a busca de artista e para a busca pelo nome da playlist. Se a playlist for encontrada, as informações dela são exibidas.

Caso o usuário opte por criar uma playlist, ele deve primeiro digitar o nome da playlist. Em seguida, o usuário deve buscar - necessariamente nessa ordem - o artista, o álbum e a música. Sendo encontrada, a música será adicionada à playlist. Se em qualquer um dos níveis a música não for encontrada, o programa torna a perguntar o artista. Quando o usuário sinalizar que finalizou, o programa retorna para o menu inicial de usuário.

## Dados
Todos os dados são salvos no formato JSON. Dois arquivos são gerados: uma base de artistas e álbuns e uma base de playlists. 
As duas base de dados iniciais são fornecidas, assim como o código para salvá-las.

## Conceitos do projeto
Neste projeto, tentei utilizar modularização de funções, algumas técnicas de programação funcional e tratamento de exceções.
