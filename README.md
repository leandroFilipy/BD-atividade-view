# 🏨 Sistema de Reserva de Hotel – Casos de Uso

Este projeto apresenta o **Diagrama de Casos de Uso** de um sistema para gerenciamento de reservas em um hotel. Seu objetivo é mapear as funcionalidades principais e as interações entre os diferentes perfis de usuário e componentes do sistema.

---

## 📋 Descrição Geral

O sistema permite que clientes realizem **pesquisas de quartos, reservas e pagamentos**, enquanto **recepcionistas** e **administradores** cuidam da parte operacional e administrativa do hotel. O diagrama segue os padrões UML para organizar esses fluxos.

---

## 👥 Atores Envolvidos

### 🎭 Atores Primários

#### 🧑‍💻 Usuário *(ator genérico)*
- Ponto de herança para: Cliente, Recepcionista e Administrador.
- Permissão: Login no sistema.

#### 👤 Cliente
- Pesquisar quartos
- Realizar reserva (`<<extend>>` da pesquisa)
- Efetuar pagamento (`<<include>>` na reserva)
- Cancelar reserva se não houver pagamento (`<<extend>>`)

#### 🧑‍💼 Administrador
- Configurar o sistema
- Gerenciar cadastros
- Acessar relatórios
- Gerenciar quartos

#### 🛎️ Recepcionista
- Gerenciar reservas:
  - Fazer check-in *(especialização)*
  - Fazer check-out *(especialização)*
  - Cancelar reservas *(especialização)*

### 🔌 Atores Secundários

- **📦 Banco de Dados**: Armazena relatórios, registros e cadastros.
- **💳 API de Pagamentos**: Responsável pelo processamento financeiro das reservas.

---

## 🔗 Relações Entre Casos de Uso

- `<<include>>` → Representa ações **obrigatórias** (ex: pagamento é parte da reserva).
- `<<extend>>` → Representa ações **opcionais ou condicionais** (ex: cancelamento por falta de pagamento).
- **Herança entre Atores** → Usuário é base para Cliente, Administrador e Recepcionista.
- **Generalização de Casos** → Gerenciar reservas se desdobra em check-in, check-out e cancelamento.

---

## 🧭 Estrutura do Diagrama

- Baseado nos padrões da **UML (Unified Modeling Language)**.
- Identificação clara dos fluxos e permissões.
- Separação entre usuários humanos e sistemas externos.

---

## 👨‍💻 Autores

- Daniel Vinicius Rios Sismer  
- Leandro Filipy de Lima  
- José Azarías Pérez Torres  

---

## 📄 Licença

Este projeto foi desenvolvido com fins **educacionais**, podendo ser reutilizado e adaptado livremente para estudos e protótipos de sistemas similares.

---

