# BarberShop - Aplicativo de Agendamento de Barbearia

## Descrição
O **BarberShop** é um aplicativo Android desenvolvido para facilitar o agendamento de serviços em barbearias. Com ele, os clientes podem escolher o barbeiro, definir a data e o horário do atendimento e confirmar a reserva diretamente pelo app. O sistema utiliza o **Firebase Firestore** para armazenar e gerenciar os agendamentos de forma segura e eficiente.

## Tecnologias Utilizadas
- **Linguagem de Programação:** Kotlin
- **Framework de Desenvolvimento:** Android SDK
- **Gerenciamento de Interface:** XML com View Binding
- **Banco de Dados:** Firebase Firestore
- **Componentes Utilizados:**
  - RecyclerView para exibição de serviços
  - DatePicker e TimePicker para seleção de data e horário
  - Snackbar para mensagens de feedback ao usuário

## Funcionalidades
### Tela de Login
- Permite ao usuário acessar o sistema.
- Validação de credenciais.

### Tela Home
- Exibe uma lista de serviços oferecidos pela barbearia.
- Usa um **RecyclerView** para organização dos serviços.
- Possui um botão para iniciar o agendamento de um serviço.

### Tela de Agendamento
- Permite ao usuário selecionar:
  - **Data do atendimento** (**DatePicker**).
  - **Horário** (**TimePicker**, com suporte a formato 24 horas).
  - **Barbeiro desejado** (opções predefinidas).
- Valida se o agendamento está dentro do horário de funcionamento (08:00 - 19:00).
- Exibe mensagens de erro ou sucesso através do **Snackbar**.
- Salva os agendamentos no **Firebase Firestore**.

## Integração com Firebase Firestore
### Armazenamento de Dados
- O aplicativo utiliza o **Firebase Firestore** para armazenar e recuperar os agendamentos.
- Cada agendamento é salvo como um documento dentro da coleção **"agendamento"**.
- Os dados armazenados incluem:
  - Nome do cliente
  - Nome do barbeiro
  - Data do agendamento
  - Horário selecionado

### Recuperação de Dados
- O aplicativo pode recuperar os agendamentos salvos para exibição ao usuário.
- Implementação de consultas para verificar disponibilidade de horários e evitar conflitos.

### Validações e Segurança
- Uso de regras de segurança do Firestore para restringir acessos indevidos.
- Validação de entradas antes de enviar dados ao banco de dados.
- Tratamento de erros para garantir que falhas na conexão com o Firestore sejam adequadamente gerenciadas.

## Como Rodar o Projeto
### Pré-requisitos
Antes de iniciar, certifique-se de ter instalado:
- **Android Studio** (versão mais recente)
- **Conta no Firebase** (para configuração do Firestore)
- **Emulador Android ou dispositivo físico conectado**

### Passos para Execução
1. Clone este repositório:
   ```bash
   git clone https://github.com/seu-usuario/BarberShop.git
   ```
2. Abra o projeto no **Android Studio**.
3. Configure o **Firebase Firestore** no projeto.
   - Adicione o **google-services.json** na pasta **app/**.
   - Configure as regras de segurança no **Firestore**.
4. Construa e execute o aplicativo em um emulador ou dispositivo físico.


---

Desenvolvido por Edmilson Alves ✨

