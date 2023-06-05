- 👋 Hi, I’m @Bastamainti11
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Bastamainti11/Bastamainti11 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
class Tavolo:
    def __init__(self, numero, capacita):
        self.numero = numero
        self.capacita = capacita

class Dipendente:
    def __init__(self, nome, ruolo, turno):
        self.nome = nome
        self.ruolo = ruolo
        self.turno = turno

class Menu:
    def __init__(self, nome, descrizione, prezzo):
        self.nome = nome
        self.descrizione = descrizione
        self.prezzo = prezzo

class Ingrediente:
    def __init__(self, nome, data_scadenza):
        self.nome = nome
        self.data_scadenza = data_scadenza

class Cliente:
    def __init__(self, nome, email):
        self.nome = nome
        self.email = email

class Prenotazione:
    def __init__(self, cliente, data, ora, numero_persone):
        self.cliente = cliente
        self.data = data
        self.ora = ora
        self.numero_persone = numero_persone

class GestioneTavoli:
    def __init__(self):
        self.tavoli = []

    def aggiungi_tavolo(self, tavolo):
        self.tavoli.append(tavolo)

    def rimuovi_tavolo(self, numero_tavolo):
        for tavolo in self.tavoli:
            if tavolo.numero == numero_tavolo:
                self.tavoli.remove(tavolo)
                break

    def elenco_tavoli(self):
        for tavolo in self.tavoli:
            print(f"Tavolo {tavolo.numero} - Capacità: {tavolo.capacita}")

class GestionePersonale:
    def __init__(self):
        self.dipendenti = []

    def aggiungi_dipendente(self, dipendente):
        self.dipendenti.append(dipendente)

    def rimuovi_dipendente(self, nome_dipendente):
        for dipendente in self.dipendenti:
            if dipendente.nome == nome_dipendente:
                self.dipendenti.remove(dipendente)
                break

    def elenco_dipendenti(self):
        for dipendente in self.dipendenti:
            print(f"{dipendente.nome} - Ruolo: {dipendente.ruolo} - Turno: {dipendente.turno}")

class GestioneMenu:
    def __init__(self):
        self.menu = []

    def aggiungi_piatto(self, piatto):
        self.menu.append(piatto)

    def rimuovi_piatto(self, nome_piatto):
        for piatto in self.menu:
            if piatto.nome == nome_piatto:
                self.menu.remove(piatto)
                break

    def elenco_menu(self):
        for piatto in self.menu:
            print(f"{piatto.nome} - {piatto.descrizione} - Prezzo: {piatto.prezzo}€")

class GestioneIngredienti:
    def __init__(self):
        self.ingredienti = []

    def aggiungi_ingrediente(self, ingrediente):
        self.ingredienti.append(ingrediente)

    def rimuovi_ingrediente(self, nome_ingrediente):
        for ingrediente in self.ingredienti:
            if ingrediente.nome == nome_ingrediente:
                self.ingredient
 self.ingredienti.remove(ingrediente)
                break

    def elenco_ingredienti(self):
        for ingrediente in self.ingredienti:
            print(f"{ingrediente.nome} - Data scadenza: {ingrediente.data_scadenza}")


class GestioneClienti:
    def __init__(self):
        self.clienti = []

    def aggiungi_cliente(self, cliente):
        self.clienti.append(cliente)

    def rimuovi_cliente(self, nome_cliente):
        for cliente in self.clienti:
            if cliente.nome == nome_cliente:
                self.clienti.remove(cliente)
                break

    def elenco_clienti(self):
        for cliente in self.clienti:
            print(f"{cliente.nome} - Email: {cliente.email}")


class GestionePrenotazioni:
    def __init__(self):
        self.prenotazioni = []

    def aggiungi_prenotazione(self, prenotazione):
        self.prenotazioni.append(prenotazione)

    def rimuovi_prenotazione(self, cliente, data, ora):
        for prenotazione in self.prenotazioni:
            if prenotazione.cliente == cliente and prenotazione.data == data and prenotazione.ora == ora:
                self.prenotazioni.remove(prenotazione)
                break

    def elenco_prenotazioni(self):
        for prenotazione in self.prenotazioni:
            print(f"Cliente: {prenotazione.cliente.nome} - Data: {prenotazione.data} - Ora: {prenotazione.ora} - Numero persone: {prenotazione.numero_persone}")


# Esempio di utilizzo del programma

gestione_tavoli = GestioneTavoli()
gestione_personale = GestionePersonale()
gestione_menu = GestioneMenu()
gestione_ingredienti = GestioneIngredienti()
gestione_clienti = GestioneClienti()
gestione_prenotazioni = GestionePrenotazioni()

# Aggiunta di tavoli
tavolo1 = Tavolo(1, 4)
gestione_tavoli.aggiungi_tavolo(tavolo1)

tavolo2 = Tavolo(2, 6)
gestione_tavoli.aggiungi_tavolo(tavolo2)

# Aggiunta di dipendenti
dipendente1 = Dipendente("Mario Rossi", "Chef", "Mattina")
gestione_personale.aggiungi_dipendente(dipendente1)

dipendente2 = Dipendente("Luigi Verdi", "Cameriere", "Sera")
gestione_personale.aggiungi_dipendente(dipendente2)

# Aggiunta di piatti al menu
piatto1 = Menu("Pizza Margherita", "Pomodoro, mozzarella, basilico", 8.5)
gestione_menu.aggiungi_piatto(piatto1)

piatto2 = Menu("Tagliatelle al ragù", "Tagliatelle fatte in casa con ragù di carne", 12.0)
gestione_menu.aggiungi_piatto(piatto2)

# Aggiunta di ingredienti
ingrediente1 = Ingrediente("Pomodori", "2023-06-30")
gestione_ingredienti.aggiungi_ingrediente(ingrediente1)

ingrediente2 = Ingrediente("Pasta fresca", "2023-07-15")
gestione_ingredienti.aggiungi_ingrediente(ingrediente2)

# Aggiunta di clienti
cliente1 = Cliente("Giuseppe Bianchi", "giuseppe@example.com")
gestione_clienti.aggiungi_cliente(cliente1)

cliente2 = Cliente("Maria Rossi", "maria@example.com")
gestione_clienti.aggiungi_cliente(cliente2)

# Aggiunta di prenotazioni
prenotazione1 = Prenotazione(cliente1, "2023-05-25", "20:00", 4)
gestione_prenotazioni.aggiungi_prenotazione(prenotazione1)

prenotazione2 = Prenotazione(cliente2, "2023-05-28", "19:30", 6)
gestione_prenotazioni.aggiungi_prenotazione(prenotazione2)

# Esempi di utilizzo delle funzioni
print("Elenco tavoli:")
gestione_tavoli.elenco_tavoli()

print("\nElenco dipendenti:")
gestione_personale.elenco_dipendenti()

print("\nElenco piatti nel menu:")
gestione_menu.elenco_menu()

print("\nElenco ingredienti:")
gestione_ingredienti.elenco_ingredienti()

print("\nElenco clienti:")
gestione_clienti.elenco_clienti()

print("\nElenco prenotazioni:")
gestione_prenotazioni.elenco_prenotazioni()
