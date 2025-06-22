📚 Sistema de Recomendação Educacional
Este projeto implementa um sistema de recomendação híbrido de materiais educacionais utilizando FastAPI e Docker. O sistema utiliza dados dos alunos, suas áreas de interesse e histórico de interações para recomendar conteúdos personalizados.

🛠️ Tecnologias Utilizadas
Python 3.11

FastAPI

Scikit-learn

Pandas e NumPy

Docker & Docker Compose

Testes com Pytest

🚀 Como Executar
Pré-requisitos
Docker e Docker Compose instalados

Passo a passo
Clone o repositório:

bash

git clone <url-do-repo>
cd <nome-da-pasta>
Inicie o serviço com Docker:

bash

docker-compose up --build
Acesse a API via navegador:

bash
http://localhost:8000/docs

🧠 Modelos de Recomendação
Filtragem baseada em conteúdo: compara os interesses dos alunos com a descrição dos materiais.

Filtragem colaborativa: recomenda com base em padrões de interação de outros alunos com materiais semelhantes.

Recomendação híbrida: combinação das duas abordagens para gerar sugestões mais robustas.

🔗 Endpoints Disponíveis
Método	Endpoint	Descrição
POST	/recomendacao/conteudo	Recomendação baseada em conteúdo textual
POST	/recomendacao/colaborativa	Recomendação com base no histórico
POST	/recomendacao/hibrida	Combina conteúdo e colaboração
POST	/alunos	Adiciona um novo aluno
PUT	/alunos/{id_aluno}	Atualiza interesses de um aluno

📄 Exemplo de Requisição
json
POST /recomendacao/hibrida

{
  "id_aluno": 1,
  "limite": 5
}
📁 Estrutura Esperada dos Arquivos CSV
dados_alunos.csv:
Contém os dados dos alunos com as colunas id_aluno, nome, disciplinas_cursadas, areas_interesse.

interacoes.csv:
Histórico de interações dos alunos com os materiais, contendo id_aluno, id_material, avaliacao.

materiais_didaticos.csv:
Descrição dos materiais didáticos, com id_material, area, nivel, tipo, descricao.

✅ Testes
O projeto inclui testes automatizados com pytest. Para executá-los:

bash
pytest test_main.py
👨‍💻 Autor / Equipe
Nome: João Pedro Borges ; 22253262

📦 Licença
Este projeto foi desenvolvido para fins educacionais e acadêmicos.

