import customtkinter

customtkinter.set_appearance_mode("dark")
customtkinter.set_default_color_theme("blue")

janela = customtkinter.CTk()
janela.geometry("600x600")
janela.title("SE Sistemas e Tecnologia")
janela.configure(fg_color="#050B16")

logo = customtkinter.CTkLabel(
    janela,
    text="S E",
    font=("Arial", 85, "bold"),
    text_color="#00BFFF"
)
logo.pack(pady=(30, 0))

titulo = customtkinter.CTkLabel(
    janela,
    text="SISTEMAS E",
    font=("Arial", 32, "bold"),
    text_color="white"
)
titulo.pack(pady=0)

subtitulo = customtkinter.CTkLabel(
    janela,
    text="TECNOLOGIA QUE CONECTA",
    font=("Arial", 16),
    text_color="#00BFFF"
)
subtitulo.pack(pady=5)

frase = customtkinter.CTkLabel(
    janela,
    text="SOLUÇÕES",
    font=("Arial", 15),
    text_color="#CCCCCC"
)
frase.pack(pady=(0, 25))

conteudo = customtkinter.CTkLabel(
    janela,
    text="Bem-vindo à SE Sistemas!",
    font=("Arial", 20, "bold"),
    text_color="white"
)
conteudo.pack(pady=15)


def abrir_sistema():
    conteudo.configure(
        text="Sistema aberto! Bem-vindo ao painel da empresa."
    )


def abrir_suporte():
    conteudo.configure(
        text="SUPORTE TÉCNICO. Entre em contato com nossa equipe."
    )


def sobre_empresa():
    conteudo.configure(
        text="SE Sistemas. Tecnologia que conecta soluções."
    )


botao_sistema = customtkinter.CTkButton(
    janela,
    text="ACESSAR SISTEMA",
    width=280,
    height=45,
    fg_color="#007BFF",
    hover_color="#0056B3",
    font=("Arial", 15, "bold"),
    command=abrir_sistema
)
botao_sistema.pack(pady=10)

botao_suporte = customtkinter.CTkButton(
    janela,
    text="SUPORTE TÉCNICO",
    width=280,
    height=45,
    fg_color="#111D30",
    hover_color="#173B65",
    border_width=2,
    border_color="#00BFFF",
    font=("Arial", 15, "bold"),
    command=abrir_suporte
)
botao_suporte.pack(pady=10)

botao_sobre = customtkinter.CTkButton(
    janela,
    text="SOBRE A EMPRESA",
    width=280,
    height=45,
    fg_color="#111D30",
    hover_color="#173B65",
    border_width=2,
    border_color="#00BFFF",
    font=("Arial", 15, "bold"),
    command=sobre_empresa
)
botao_sobre.pack(pady=10)

rodape = customtkinter.CTkLabel(
    janela,
    text="© SE Sistemas e Tecnologia",
    font=("Arial", 12),
    text_color="#777777"
)
rodape.pack(side="bottom", pady=15)

janela.mainloop()
