# basson
Development
from flask import Flask, render_template

app = Flask(__name__)

# Rota para a página inicial
@app.route("/")
def homepage():
    return render_template("homepage.html")

# Rota para a página de contatos
@app.route("/contatos")
def contatos():
    return render_template("contatos.html")

# Rota para uma página personalizada
@app.route("/usuarios/<nome_usuario>")
def usuarios(nome_usuario):
    return render_template("usuarios.html", nome_usuario=nome_usuario)

# Executar o servidor
if __name__ == "__main__":
    app.run(debug=True)
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Página com Fundo Branco</title>
    <style>
        body {
            background-color: #FFFFFF; /* Cor do fundo: Branco */
            font-family: Arial, sans-serif; /* Fonte padrão */
        }
    </style>
</head>
<body>
    <h1>Bem-vindo à minha página!</h1>
    <p>Esta página tem um fundo branco.</p>
</body>
</html>
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Caixa de Seleção e Botão Enviar</title>
    <style>
        body {
            background-color: #FFFFFF; /* Cor do fundo: Branco */
            font-family: Arial, sans-serif; /* Fonte padrão */
        }
        
        /* Estilos para a caixa de seleção e o botão */
        .form-container {
            width: 300px;
            margin: 50px auto;
            padding: 20px;
            border: 1px solid #ddd;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        
        label {
            display: block;
            margin-bottom: 10px;
        }
        
        input[type="checkbox"] {
            margin-right: 10px;
        }
        
        button[type="submit"] {
            padding: 10px 20px;
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        
        button[type="submit"]:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <div class="form-container">
        <h2>Formulário de Contato</h2>
        <form action="#" method="post">
            <label>
                <input type="checkbox" id="aceito" name="aceito">
                Aceito os termos de uso.
            </label>
            <button type="submit">Enviar Mensagem</button>
        </form>
    </div>
</body>
</html>
