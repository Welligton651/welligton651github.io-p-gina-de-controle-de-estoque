# Sistema de Controle de Estoque

Sistema web completo para gerenciamento de estoque baseado na planilha fornecida, com interface moderna e funcionalidades avançadas.

## 🚀 Funcionalidades

### Dashboard
- **Visão geral do estoque**: Total de produtos, produtos OK, estoque baixo e esgotados
- **Interface moderna**: Design responsivo com gradientes e animações suaves
- **Cards informativos**: Indicadores visuais do status do estoque

### Gerenciamento de Produtos
- **Listagem completa**: Tabela paginada com todos os produtos
- **Busca em tempo real**: Filtro por descrição do produto
- **Status visual**: Badges coloridos indicando status do estoque (OK, BAIXO, ESGOTADO)
- **Paginação**: Navegação eficiente entre páginas

### Controle de Estoque
- **Dar baixa**: Reduzir quantidade em estoque com registro de movimentação
- **Entrada**: Adicionar produtos ao estoque
- **Histórico**: Registro completo de todas as movimentações
- **Validações**: Controle de estoque negativo e quantidades inválidas

### Exportação
- **Exportar XLSX**: Download da planilha atual no formato Excel
- **Formato original**: Mantém a estrutura da planilha original
- **Dados atualizados**: Sempre com as informações mais recentes

## 🛠️ Tecnologias Utilizadas

### Backend
- **Flask**: Framework web Python
- **SQLAlchemy**: ORM para banco de dados
- **SQLite**: Banco de dados local
- **Pandas**: Manipulação de dados
- **OpenPyXL**: Geração de arquivos Excel
- **Flask-CORS**: Suporte a requisições cross-origin

### Frontend
- **HTML5/CSS3**: Estrutura e estilo moderno
- **JavaScript**: Funcionalidades interativas
- **Font Awesome**: Ícones profissionais
- **Design Responsivo**: Compatível com desktop e mobile

### Recursos Visuais
- **Gradientes modernos**: Background atrativo
- **Backdrop filter**: Efeitos de vidro fosco
- **Animações suaves**: Transições e hover effects
- **Cards flutuantes**: Design moderno com sombras
- **Cores semânticas**: Verde para OK, amarelo para baixo, vermelho para esgotado

## 📊 Estrutura do Banco de Dados

### Tabela: Produto
- `id`: Identificador único
- `descricao`: Descrição do produto
- `unidade`: Unidade de medida (ex: UNIDADE, KG, etc.)
- `fornecimento`: Quantidade de fornecimento
- `estoque`: Quantidade atual em estoque
- `estoque_minimo`: Limite mínimo para alerta
- `created_at`: Data de criação
- `updated_at`: Data da última atualização

### Tabela: MovimentacaoEstoque
- `id`: Identificador único
- `produto_id`: Referência ao produto
- `tipo`: ENTRADA ou SAIDA
- `quantidade`: Quantidade movimentada
- `observacao`: Observações da movimentação
- `data_movimentacao`: Data e hora da movimentação

## 🚀 Como Executar

### Pré-requisitos
- Python 3.11+
- pip (gerenciador de pacotes Python)

### Instalação
1. Clone ou baixe o projeto
2. Navegue até a pasta do projeto
3. Ative o ambiente virtual:
   ```bash
   source venv/bin/activate
   ```
4. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```

### Execução
1. Execute o servidor:
   ```bash
   python src/main.py
   ```
2. Acesse no navegador: `http://localhost:5000`

## 📋 API Endpoints

### Produtos
- `GET /api/produtos` - Listar produtos (com paginação e busca)
- `POST /api/produtos` - Criar novo produto
- `GET /api/produtos/{id}` - Obter produto específico
- `PUT /api/produtos/{id}` - Atualizar produto
- `DELETE /api/produtos/{id}` - Deletar produto

### Movimentações
- `POST /api/produtos/{id}/baixa` - Dar baixa no estoque
- `POST /api/produtos/{id}/entrada` - Adicionar ao estoque
- `GET /api/movimentacoes` - Listar movimentações

### Dashboard e Relatórios
- `GET /api/dashboard` - Dados do dashboard
- `GET /api/exportar-xlsx` - Exportar planilha Excel

## 📱 Interface Responsiva

O sistema foi desenvolvido com design responsivo, adaptando-se automaticamente a diferentes tamanhos de tela:

- **Desktop**: Layout completo com todas as funcionalidades
- **Tablet**: Adaptação dos cards e tabelas
- **Mobile**: Interface otimizada para toque, com botões maiores e layout vertical

## 🔒 Recursos de Segurança

- **Validação de dados**: Verificação de tipos e valores
- **Controle de estoque**: Impede estoque negativo
- **Sanitização**: Proteção contra injeção de dados
- **CORS configurado**: Controle de acesso entre domínios

## 📈 Dados Importados

O sistema foi inicializado com **215 produtos** da planilha original, incluindo:
- Adaptadores e conexões
- Ferramentas elétricas
- Material de construção
- Produtos químicos
- Equipamentos diversos

Todos os produtos mantêm a estrutura original da planilha com descrição, unidade, fornecimento e estoque atual.

## 🎨 Design System

### Cores
- **Primária**: Gradiente azul/roxo (#667eea → #764ba2)
- **Sucesso**: Verde (#27ae60)
- **Atenção**: Amarelo/laranja (#f39c12)
- **Erro**: Vermelho (#e74c3c)
- **Neutro**: Cinzas diversos para textos e bordas

### Tipografia
- **Fonte**: Segoe UI (sistema)
- **Hierarquia**: Títulos grandes, subtítulos e texto corpo
- **Peso**: Regular (400) e Bold (700)

### Componentes
- **Cards**: Fundo branco translúcido com blur
- **Botões**: Gradientes com hover effects
- **Tabelas**: Zebra striping e hover states
- **Modais**: Animação de entrada suave
- **Formulários**: Campos com focus states

## 📞 Suporte

Sistema desenvolvido para controle eficiente de estoque com interface moderna e funcionalidades completas. Para dúvidas ou sugestões, consulte a documentação da API ou entre em contato.

