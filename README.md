# Project-PO
## Network Communication Manager - prr
This project aims to develop an application that functions as a network communication terminal manager, named prr. The program allows for the management and querying of clients, terminals, and communications. The application provides various services to its users, including:

Registering client information
Registering terminal information
Registering communication data
Searching for past communications
Calculating the balance associated with terminals

## Entities
The application manages several entities:

### 1. Client
Each client has a unique key, name (string), and fiscal identification number (integer). Clients can be associated with multiple terminals. They maintain information about payments made for past communications and current outstanding debts.

Clients are categorized into three types: Normal, Gold, and Platinum. The client type influences the cost of their communications based on tariff plans. The client type evolves according to specific conditions.

### 2. Terminal
Each terminal is identified by a unique 6-digit numeric code (string) and is associated with a single client. Terminals can perform different types of communications, depending on whether they are basic or sophisticated.

Terminals keep their own accounting of payments and debts for communications. A terminal can also have a list of friend terminals, and communications between friend terminals are cheaper than communications between non-friend terminals.

Terminals have several states: Off, Silent, Wait, and Busy.

### 3. Communication
Each communication has a unique identifier (integer) and contains information about the source and destination terminals and the communication status (ongoing or terminated). Communications can be of different types: text, voice, or video.

The cost of a communication depends on its type and duration, calculated according to the client's tariff plan.

### 4. Tariff Plans
Tariff plans define the costs for each type of communication based on the client's type and communication type.

The cost of a communication is calculated based on the tariff plan applicable to the client and the communication type and duration.

## Menus and functionalities

### Main Menu (Menu Principal):
```
Open (Abrir): Load data from a previously saved session.
Save (Guardar): Save the current state of the application.
Client Management (Gestão de clientes): Open the client management menu.
Terminal Management (Gestão de terminais): Open the terminal management menu.
Queries (Consultas): Open the queries menu.
Show Global Payments and Debts (Mostrar informação global sobre pagamentos e dívidas): Display global payment and debt information.
```
### Client Management Menu (Menu de Gestão de Clientes):
```
View Client (Visualizar cliente): View information about a specific client.
View All Clients (Visualizar todos os clientes): View information about all registered clients.
Register Client (Registar cliente): Register a new client.
Enable Client Notifications (Activar recepção de contactos falhados): Activate failed contact notifications for a client.
Disable Client Notifications (Desactivar recepção de contactos falhados): Deactivate failed contact notifications for a client.
Show Client Payments and Debts (Mostrar informação sobre pagamentos e dívidas de cliente): Display payment and debt information for a specific client.
```
### Terminal Management Menu (Menu de Gestão de Terminais):
```
Show All Terminals (Mostrar todos os terminais): Display information about all registered terminals.
Register Terminal (Registar terminal): Register a new terminal.
Terminal Console Menu (Menu da consola de um terminal): Open the console menu for a specific terminal.
```
### Consult Menu (Menu de Consultas):
```
Show All Communications (Mostrar todas as comunicações): Display information about all communications.
Show Communications From Client (Mostrar comunicações feitas por um cliente): Display communications initiated by a specific client.
Show Communications To Client (Mostrar comunicações recebidas por um cliente): Display communications received by a specific client.
Show Clients Without Debts (Mostrar clientes sem dívidas): Display clients with no debts.
Show Clients With Debts (Mostrar clientes com dívidas): Display clients with debts.
Show Unused Terminals (Mostrar terminais sem atividade): Display terminals that have not performed or received any communications.
Show Terminals With Positive Balance (Mostrar terminais com saldo positivo): Display terminals with a positive balance.
```
### Terminal Console Menu (Menu da consola de um terminal):
```
Turn On Terminal (Ligar terminal): Turn on a specific terminal.
Turn Off Terminal (Desligar terminal): Turn off a specific terminal.
Silence Terminal (Silenciar terminal): Put a specific terminal in silent mode.
Add Friend (Adicionar amigo): Add a friend terminal to the current terminal.
Remove Friend (Retirar amigo): Remove a friend terminal from the current terminal.
Perform Payment (Efetuar pagamento): Make a payment for a specific terminal.
Show Terminal Balance (Mostrar informação sobre pagamentos e dívidas): Display payment and debt information for the current terminal.
Send Text Communication (Enviar comunicação de texto): Send a text communication from the current terminal.
Start Interactive Communication (Iniciar comunicação interativa): Start an interactive communication from the current terminal.
End Interactive Communication (Terminar comunicação interativa): End an ongoing interactive communication from the current terminal.
Show Ongoing Communications (Mostrar comunicações em curso): Display information about ongoing communications for the current terminal.
```

More information available in "Problem Description.pdf"
