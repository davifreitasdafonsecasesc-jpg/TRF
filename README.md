
import customtkinter

customtkinter.set_appearance_mode("dark")
customtkinter.set_default_color_theme("blue")

janela = customtkinter.CTk()
janela.geometry("600x600")
janela.title("Neuro+")
janela.configure(fg_color="#071426")

# Título
titulo = customtkinter.CTkLabel(
    janela,
    text="🧠 Neuro+",
    font=("Arial", 40, "bold"),
    text_color="#00BFFF"
)
titulo.pack(pady=(25, 5))

subtitulo = customtkinter.CTkLabel(
    janela,
    text="Mais foco. Mais calma. Mais você.",
    font=("Arial", 16),
    text_color="white"
)
subtitulo.pack(pady=5)

# Abas
abas = customtkinter.CTkTabview(janela)
abas.pack(padx=20, pady=20, fill="both", expand=True)

inicio = abas.add("Início")
rotina = abas.add("Rotina")
tarefas = abas.add("Tarefas")
relaxar = abas.add("Relaxar")

# Tela inicial
customtkinter.CTkLabel(
    inicio,
    text="Olá! Que bom ter você aqui! 💙",
    font=("Arial", 22, "bold")
).pack(pady=30)

customtkinter.CTkLabel(
    inicio,
    text="Você consegue!\nUm passo de cada vez.",
    font=("Arial", 18),
    text_color="#00BFFF"
).pack(pady=15)

# Rotina
customtkinter.CTkLabel(
    rotina,
    text="Minha rotina diária",
    font=("Arial", 22, "bold")
).pack(pady=20)

customtkinter.CTkCheckBox(
    rotina, text="Acordar"
).pack(pady=10)

customtkinter.CTkCheckBox(
    rotina, text="Tomar café"
).pack(pady=10)

customtkinter.CTkCheckBox(
    rotina, text="Estudar"
).pack(pady=10)

customtkinter.CTkCheckBox(
    rotina, text="Fazer uma pausa"
).pack(pady=10)

# Tarefas
customtkinter.CTkLabel(
    tarefas,
    text="Minhas tarefas",
    font=("Arial", 22, "bold")
).pack(pady=20)

campo = customtkinter.CTkEntry(
    tarefas,
    placeholder_text="Digite uma tarefa"
)
campo.pack(pady=10)

def adicionar():
    texto = campo.get()

    if texto != "":
        customtkinter.CTkLabel(
            lista,
            text="• " + texto,
            font=("Arial", 15)
        ).pack(anchor="w", pady=5)

        campo.delete(0, "end")

customtkinter.CTkButton(
    tarefas,
    text="Adicionar tarefa",
    command=adicionar
).pack(pady=10)

lista = customtkinter.CTkFrame(tarefas)
lista.pack(fill="both", expand=True, padx=15, pady=10)

# Relaxamento
customtkinter.CTkLabel(
    relaxar,
    text="Respire e relaxe 🌿",
    font=("Arial", 22, "bold")
).pack(pady=30)

customtkinter.CTkLabel(
    relaxar,
    text="Inspire devagar...\nSolte o ar com calma.\nFaça tudo no seu ritmo.",
    font=("Arial", 18),
    text_color="#00BFFF"
).pack(pady=20)

customtkinter.CTkButton(
    relaxar,
    text="Estou pronto!",
    command=lambda: customtkinter.CTkLabel(
        relaxar,
        text="Muito bem! Continue no seu ritmo 💙"
    ).pack(pady=10)
).pack(pady=10)

janela.mainloop()
