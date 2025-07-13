🏭 Sistema de Gerenciamento de Dados – Views, Procedures e Triggers em SQL
Este projeto documenta a criação de views (visões personalizadas de tabelas), stored procedures (procedimentos armazenados) e triggers (gatilhos automáticos) em um banco de dados simulado chamado factory. O objetivo é garantir uma melhor visualização, organização e integridade dos dados em uma empresa fictícia.

📄 Descrição Geral
O sistema simula a base de dados de uma empresa industrial com múltiplas tabelas relacionadas: SALES, SUPPLIERS, CLIENTS, PRODUCTS e FUNCIONARIOS.

Para otimizar o uso dessas tabelas, foram implementadas:

Views para facilitar consultas específicas

Stored Procedures para padronizar inserções

Triggers para garantir a integridade dos dados entre tabelas relacionadas

👁️ Views Criadas
🔹 view_sales_informations
📌 Mostra sales_date, sales_total e who_bought da tabela SALES

🎯 Filtra apenas vendas com SALE_ID > 4

📈 Útil para análises de vendas mais recentes

🔹 visualização_suppliers
📌 Exibe namee e address da tabela SUPPLIERS

🎯 Mostra apenas fornecedores com SUPPLIERS_ID <= 5

🧾 Facilita a listagem de fornecedores fixos

🔹 visualização_clientes
📌 Mostra CLIENTS_ID e CLIENTS_NAME

🎯 Exibe apenas clientes com CLIENTS_ID > 3

👤 Ideal para consultas de clientes mais recentes

🔹 visualização_produtos
📌 Apresenta name_products e price da tabela PRODUCTS

🎯 Considera apenas produtos com ID_PRODUCTS >= 3

🛒 Permite rápida visualização dos produtos principais

⚙️ Stored Procedures Criadas
✅ Manipulação_Funcionarios
🏢 Insere dados na tabela FUNCIONARIOS

🧾 Campos utilizados: nome_funcionario, cargo, data_contratação

💡 Útil para cadastrar novos funcionários de forma padronizada

✅ Inserção_de_Produtos
📦 Insere dados na tabela PRODUCTS

🧾 Campos utilizados: name_products, description_product, price, size

🚀 Agiliza o cadastro de novos produtos no sistema

🚨 Trigger Implementada
🔁 adicionar_supplier
🧩 Executada antes da exclusão de um registro em SUPPLIERS

❗ Deleta todos os produtos relacionados ao fornecedor excluído

🔒 Garante integridade referencial entre SUPPLIERS e PRODUCTS

🧠 Organização Técnica
As operações seguem princípios de boas práticas SQL:

🔐 Chaves estrangeiras e relacionamentos

✅ Auto incremento em chaves primárias

🔄 Atualizações em cascata para integridade

📊 Criação de views com critérios de filtro

📌 Procedimentos reutilizáveis para inserções padrão

⚠️ Triggers para consistência entre registros vinculados

👨‍💻 Desenvolvido por
🧑‍💻 Leandro Filipy de Lima



📋 Licença
Este projeto foi desenvolvido com fins educacionais, podendo ser reutilizado e adaptado para portfólios, exercícios acadêmicos ou simulações de sistemas reais.
