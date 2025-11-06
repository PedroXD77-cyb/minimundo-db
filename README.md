# minimundo-db
🐾 Sistema de Gerenciamento de Clínica Veterinária

Este projeto apresenta o planejamento e modelagem de um banco de dados relacional para uma clínica veterinária, com o objetivo de organizar e armazenar informações sobre clientes, pets, consultas, veterinários e medicamentos.

🎯 Objetivo do Projeto

O banco de dados foi projetado para permitir o controle completo das operações da clínica, registrando os atendimentos realizados, os profissionais responsáveis e os medicamentos utilizados em cada consulta.

🧩 Minimundo

A clínica veterinária realiza atendimentos a diversos clientes, que podem possuir um ou mais pets.
Cada pet pode passar por diferentes consultas, nas quais um veterinário é responsável pelo atendimento e pela prescrição de medicamentos.
Cada medicamento pode ser utilizado em várias consultas, e cada consulta pode envolver mais de um medicamento — por isso, foi criada a tabela associativa Medicamento_consulta para representar essa relação N:N entre consultas, medicamentos e veterinários.

🗂️ Estrutura das Tabelas

Cliente: Armazena dados pessoais dos tutores dos pets (nome, telefone).

Pet: Contém informações sobre os animais (nome, espécie, idade) e referência ao cliente dono.

Consulta: Registra cada atendimento, incluindo data, tipo de serviço e o pet atendido.

Veterinario: Guarda dados dos profissionais (nome, CRMV) e relaciona-se com as consultas realizadas.

Medicamento: Armazena nome, validade e quantidade disponível.

Medicamento_consulta: Faz o relacionamento entre medicamentos, consultas e veterinários.

🧠 Relacionamentos Principais

Cliente 1:N Pet — um cliente pode ter vários pets.

Pet 1:N Consulta — um pet pode ter várias consultas.

Consulta N:1 Veterinario — cada consulta é realizada por um veterinário.

Consulta N:N Medicamento — representado pela tabela intermediária Medicamento_consulta.
