# Riscado

**Gestão de encomendas para associações de bordadeiras do Seridó.**

O Riscado é um sistema web para associações e ateliês de bordado da região do Seridó (RN). Ele organiza o caminho de uma encomenda: o pedido do cliente é dividido em peças, as peças são distribuídas para as bordadeiras que trabalham em casa e o sistema acompanha prazos, materiais entregues e pagamentos por peça.

## Problema

Em muitas associações de bordado, o controle do trabalho é feito em cadernos: quem levou qual peça, que material recebeu, qual o prazo e quanto vai receber. Isso causa:

- atrasos percebidos só quando o cliente cobra;
- erros ou esquecimentos no pagamento por peça;
- falta de visão sobre a capacidade de produção da associação;
- material (linha, tecido) entregue sem registro.

## Solução

Um sistema simples, acessível pelo celular, no qual a coordenadora da associação:

- cadastra clientes, encomendas, modelos (riscos) e bordadeiras;
- divide cada encomenda em peças;
- distribui as peças para as bordadeiras, com prazo e material entregue;
- registra devoluções e pagamentos.

A bordadeira pode consultar as peças que estão com ela, os prazos e os valores a receber.

## Perfis de usuário

| Perfil | Descrição |
|---|---|
| Administrador | Gerencia usuários, grupos e configurações do sistema. |
| Coordenadora | Gerencia clientes, encomendas, peças, modelos e bordadeiras; distribui o trabalho e registra entregas e pagamentos. |
| Bordadeira | Consulta suas peças, prazos e pagamentos. |

## Tecnologias

| Camada | Tecnologia |
|---|---|
| Linguagem | Python 3.12 |
| Framework web | Django 5.2 (LTS) |
| Front-end | Templates do Django + Bootstrap 5 (layout responsivo) |
| Banco de dados | SQLite (desenvolvimento) / PostgreSQL (produção) |
| Controle de versão | Git + GitHub |
| Gestão do projeto | Scrum com GitHub Issues e GitHub Projects |
| Documentação e modelagem | Markdown + Mermaid |

## Como executar

```bash
# 1. Clonar o repositório
git clone https://github.com/SEU_USUARIO/riscado.git
cd riscado

# 2. Criar e ativar o ambiente virtual
python -m venv venv
source venv/bin/activate        # Linux/macOS
venv\Scripts\activate           # Windows

# 3. Instalar as dependências
pip install -r requirements.txt

# 4. Criar o banco de dados
python manage.py migrate

# 5. Criar um usuário administrador
python manage.py createsuperuser

# 6. Rodar o servidor
python manage.py runserver
```

Acesse em `http://127.0.0.1:8000/`.

## Documentação

Os documentos do projeto ficam no diretório [`docs`](docs/):

- [Documento de Visão](docs/doc-visao.md)
- [Documento de Modelos](docs/doc-modelos.md)

## Metodologia

O projeto segue o Scrum:

- **Backlog do produto:** registrado como issues no GitHub.
- **Sprints:** cada sprint tem um milestone com as issues planejadas.
- **Quadro:** acompanhamento no GitHub Projects (A Fazer, Em Andamento, Concluído).

## Autor

| Nome | Papel | E-mail |
|---|---|---|
| Ícaro Nonato de Freitas | Product Owner, Scrum Master e Desenvolvedor | icaro.freitas.113@ufrn.edu.br |

Projeto desenvolvido na disciplina de Engenharia de Software I, Sistemas de Informação, UFRN/CERES.