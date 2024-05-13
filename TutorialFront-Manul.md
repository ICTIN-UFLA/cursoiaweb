
### Criando um Site de Vendas com Bootstrap, CSS e HTML

#### Configuração Inicial

Antes de começarmos, você precisará de um editor de texto para escrever seu código.  No nosso caso, utilizaremos o Visual Studio Code.

**Estrutura de Arquivos:**

-   `index.html` - Página principal do site.
-   `menu.html` - Página do cardápio.
-   `delivery.html` - Página de informações sobre entrega.
-   `payment.html` - Página de opções de pagamento.
-   `styles.css` - Arquivo para estilização customizada.


#### Passo 2: Estrutura HTML Básica para Index.html

Crie um arquivo chamado `index.html`. Este será o arquivo principal do seu site. Copie e cole o código a seguir: 

````html
<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PizzaMania</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <div class="container-fluid">
            <a class="navbar-brand" href="#">Escolha sua Pizza</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav">
                    <li class="nav-item">
                        <a class="nav-link active" href="index.html">Cardápio</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="delivery.html">Entrega</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="payment.html">Pagamento</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- Carrossel de imagens -->
    <div id="carouselExampleIndicators" class="carousel slide" data-bs-ride="carousel" data-bs-interval="3000">
        <div class="carousel-indicators">
            <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
            <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1" aria-label="Slide 2"></button>
            <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="2" aria-label="Slide 3"></button>
        </div>
        <div class="carousel-inner">
            <div class="carousel-item active" data-bs-interval="3000">
                <img src="https://i.pinimg.com/originals/1f/df/0d/1fdf0d7aaaebcc093b8fc00ce384f50b.jpg" class="d-block w-100" alt="Pizza 1">
            </div>
            <div class="carousel-item" data-bs-interval="3000">
                <img src="https://www.anamariareceitas.com.br/wp-content/uploads/2022/11/Pizza-de-calabresa.jpg" class="d-block w-100" alt="Pizza 2">
            </div>
            <div class="carousel-item" data-bs-interval="3000">
                <img src="https://i0.wp.com/acheisuareceita.com.br/wp-content/uploads/2024/02/imagem_2024-02-16_081527287.png?fit=1920%2C1080&ssl=1" class="d-block w-100" alt="Pizza 3">
            </div>
        </div>
        <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Next</span>
        </button>
    </div>

    <!-- Conteúdo Principal -->
    <div class="container text-center mt-4">
        <h1>Delícias Quentes</h1>
        <p>Explore nosso cardápio recheado de sabores irresistíveis e faça seu pedido com apenas alguns cliques!</p>
        <a href="menu.html" class="btn btn-primary btn-lg">Peça Já</a>
    </div>

    <!-- Bootstrap JavaScript -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>

````

#### Passo 3: Criando as Outras Páginas

**menu.html**, **delivery.html**, e **payment.html**

-   Use uma estrutura similar ao `index.html`, mas altere o conteúdo para se adequar a cada página, como informações sobre os pratos disponíveis, detalhes de entrega, e opções de pagamento.

#### #### Passo 4: Criar a Página do Cardápio (menu.html)

Crie um arquivo chamado `menu.html`. Esta página irá listar as opções de pizzas disponíveis para compra.


````html
<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cardápio - PizzaMania</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <div class="container-fluid">
            <a class="navbar-brand" href="index.html">Escolha sua Pizza</a>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav">
                    <li class="nav-item">
                        <a class="nav-link active" href="menu.html">Cardápio</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="delivery.html">Entrega</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="payment.html">Pagamento</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <div class="container">
        <h1 class="text-center">Nosso Cardápio</h1>
        <div class="row">
            <!-- Adicione cards de produtos aqui -->
            <!-- Exemplo de um card -->
            <div class="col-md-4">
                <div class="card">
                    <img src="https://via.placeholder.com/300x300" class="card-img-top" alt="Pizza Margherita">
                    <div class="card-body">
                        <h5 class="card-title">Pizza Margherita</h5>
                        <p class="card-text">Molho de tomate fresco, mozzarella, manjericão fresco e azeite extra virgem.</p>
                        <a href="#" class="btn btn-primary">Peça Agora</a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</body>
</html>

````

#### Passo 5 Criar a Página de Informações sobre Entrega (delivery.html)

Este arquivo incluirá informações sobre como as pizzas são entregues.

```html
<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Entrega - PizzaMania</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <div class="container-fluid">
            <a class="navbar-brand" href="index.html">Escolha sua Pizza</a>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav">
                    <li class="nav-item">
                        <a class="nav-link" href="menu.html">Cardápio</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link active" href="delivery.html">Entrega</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="payment.html">Pagamento</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <div class="container">
        <h1 class="text-center">Informações de Entrega</h1>
        <p>Oferecemos entrega gratuita para pedidos acima de R$ 50,00 dentro de um raio de 10 km da nossa localização. Para distâncias maiores, uma taxa adicional será aplicada.</p>
    </div>
</body>
</html>
````


#### Passo 6 Criar a Página de Opções de Pagamento (payment.html)

Esta página irá detalhar as opções de pagamento disponíveis.

````html
<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pagamento - PizzaMania</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <div class="container-fluid">
            <a class="navbar-brand" href="index.html">Escolha sua Pizza</a>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav">
                    <li class="nav-item">
                        <a class="nav-link" href="menu.html">Cardápio</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="delivery.html">Entrega</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link active" href="payment.html">Pagamento</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <div class="container">
        <h1 class="text-center">Opções de Pagamento</h1>
        <p>Aceitamos os seguintes métodos de pagamento: cartões de crédito e débito, dinheiro e pagamento por app de celular.</p>
    </div>
</body>
</html>
````


#### Passo 7 Criar o Arquivo de Estilos (styles.css)

Primeiro, crie o arquivo `styles.css` com o conteúdo abaixo para definir os estilos básicos do seu site.

````css
body {
    background-color: #fff5e6;
    color: #333;
}

.navbar {
    margin-bottom: 20px;
    background-color: #fff;
    border-bottom: 2px solid #ccc;
}

.carousel-item img {
    height: 500px; /* Ajuste conforme necessário */
    object-fit: cover;
}

.container h1 {
    margin-top: 20px;
}

.btn-primary {
    color: #fff;
    background-color: #ff4500;
    border-color: #ff4500;
}

.btn-primary:hover {
    background-color: #e03c00;
    border-color: #c03200;
}

````


### Testando e Ajustando

Com essas páginas criadas e estilizadas, teste seu site para garantir que tudo está funcionando como esperado. Ajuste o HTML e CSS conforme necessário para melhorar a aparência e a funcionalidade do site.
