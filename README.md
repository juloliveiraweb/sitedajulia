# sitedajulia 
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SHEIN Style - Moda Online</title>

    <style>
        /* Reset básico */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
        }

        body {
            background-color: #f8f8f8;
            color: #222;
        }

        /* --- CABEÇALHO --- */
        header {
            background-color: #ffffff;
            border-bottom: 1px solid #e5e5e5;
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .top-bar {
            background-color: #000;
            color: #fff;
            text-align: center;
            padding: 6px;
            font-size: 12px;
            font-weight: bold;
            letter-spacing: 1px;
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 40px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .logo {
            font-size: 28px;
            font-weight: 900;
            letter-spacing: 2px;
            color: #000;
            text-decoration: none;
        }

        .cart-status {
            position: relative;
            font-size: 14px;
            font-weight: bold;
            background: #f0f0f0;
            padding: 8px 16px;
            border-radius: 20px;
            cursor: pointer;
        }

        .cart-count {
            background-color: #ff4757;
            color: white;
            border-radius: 50%;
            padding: 2px 7px;
            font-size: 12px;
            margin-left: 5px;
        }

        /* --- GALERIA DE PRODUTOS --- */
        .catalog-title {
            text-align: center;
            margin: 30px 0 10px;
            font-size: 22px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .gallery-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            padding: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }

        /* Card do Produto */
        .card {
            background-color: #ffffff;
            border-radius: 8px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.06);
            overflow: hidden;
            width: 240px;
            transition: transform 0.2s, box-shadow 0.2s;
            position: relative;
            display: flex;
            flex-direction: column;
        }

        .card:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.12);
        }

        /* Tag de Desconto */
        .badge-discount {
            position: absolute;
            top: 10px;
            left: 10px;
            background-color: #000;
            color: #fff;
            font-size: 11px;
            font-weight: bold;
            padding: 4px 8px;
            border-radius: 3px;
        }

        .card img {
            width: 100%;
            height: 300px;
            object-fit: cover;
        }

        .card-content {
            padding: 15px;
            display: flex;
            flex-direction: column;
            flex-grow: 1;
            justify-content: space-between;
        }

        .card-content h3 {
            font-size: 14px;
            font-weight: 500;
            color: #333;
            margin-bottom: 6px;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

        .price-container {
            margin-bottom: 12px;
        }

        .price-current {
            font-size: 16px;
            font-weight: bold;
            color: #ff4757;
            margin-right: 6px;
        }

        .price-old {
            font-size: 12px;
            color: #aaa;
            text-decoration: line-through;
        }

        /* Botão do Carrinho */
        .cart-btn {
            background-color: #000000;
            color: white;
            border: none;
            padding: 10px;
            border-radius: 4px;
            cursor: pointer;
            font-weight: bold;
            font-size: 13px;
            width: 100%;
            transition: background 0.2s;
        }

        .cart-btn:hover {
            background-color: #333333;
        }

        /* Estado quando o item está no carrinho */
        .cart-btn.added {
            background-color: #2ed573;
        }
    </style>
</head>
<body>

    <header>
        <div class="top-bar">
            FRETE GRÁTIS EM COMPRAS ACIMA DE R$ 99 | CUPOM: PRIMEIRACOMPRA
        </div>
        <div class="nav-container">
            <a href="#" class="logo">SHEIN</a>
            <div class="cart-status">
                🛒 Carrinho: <span id="cart-counter" class="cart-count">0</span>
            </div>
        </div>
    </header>

    <h2 class="catalog-title">Lançamentos da Semana</h2>

    <main class="gallery-container">

        <!-- Produto 1 -->
        <div class="card">
            <span class="badge-discount">-30%</span>
            <img src="https://picsum.photos/id/64/300/400" alt="Vestido Casual">
            <div class="card-content">
                <div>
                    <h3>Vestido Elegante de Verão</h3>
                    <div class="price-container">
                        <span class="price-current">R$ 69,90</span>
                        <span class="price-old">R$ 99,90</span>
                    </div>
                </div>
                <button class="cart-btn">Adicionar ao Carrinho</button>
            </div>
        </div>

        <!-- Produto 2 -->
        <div class="card">
            <span class="badge-discount">-15%</span>
            <img src="https://picsum.photos/id/338/300/400" alt="Jaqueta Jeans">
            <div class="card-content">
                <div>
                    <h3>Jaqueta Jeans Oversized</h3>
                    <div class="price-container">
                        <span class="price-current">R$ 119,90</span>
                        <span class="price-old">R$ 139,90</span>
                    </div>
                </div>
                <button class="cart-btn">Adicionar ao Carrinho</button>
            </div>
        </div>

        <!-- Produto 3 -->
        <div class="card">
            <span class="badge-discount">-50%</span>
            <img src="https://picsum.photos/id/823/300/400" alt="Camiseta Minimalista">
            <div class="card-content">
                <div>
                    <h3>Camiseta Algodão Premium</h3>
                    <div class="price-container">
                        <span class="price-current">R$ 39,90</span>
                        <span class="price-old">R$ 79,90</span>
                    </div>
                </div>
                <button class="cart-btn">Adicionar ao Carrinho</button>
            </div>
        </div>

        <!-- Produto 4 -->
        <div class="card">
            <span class="badge-discount">-20%</span>
            <img src="https://picsum.photos/id/1005/300/400" alt="Conjunto Esportivo">
            <div class="card-content">
                <div>
                    <h3>Conjunto Moletom Style</h3>
                    <div class="price-container">
                        <span class="price-current">R$ 89,90</span>
                        <span class="price-old">R$ 109,90</span>
                    </div>
                </div>
                <button class="cart-btn">Adicionar ao Carrinho</button>
            </div>
        </div>

    </main>

    <script>
        // 1. Seleciona todos os botões de compra e o contador global no topo da página
        const botoesCarrinho = document.querySelectorAll('.cart-btn');
        const contadorGlobal = document.getElementById('cart-counter');
        
        // Variável controladora do número total de itens no carrinho
        let totalNoCarrinho = 0;

        // 2. Percorre cada botão aplicando a mesma lógica aprendida na aula
        botoesCarrinho.forEach(function(botao) {
            
            botao.addEventListener('click', function() {
                
                // Lógica de alternância (Adicionar / Remover do carrinho)
                if (botao.classList.contains('added')) {
                    // Se já estava adicionado, remove do carrinho
                    botao.classList.remove('added');
                    botao.textContent = 'Adicionar ao Carrinho';
                    totalNoCarrinho--;
                } else {
                    // Se não estava adicionado, inclui no carrinho
                    botao.classList.add('added');
                    botao.textContent = '✓ No Carrinho';
                    totalNoCarrinho++;
                }
                
                // Atualiza o contador geral no cabeçalho
                contadorGlobal.textContent = totalNoCarrinho;
            });
            
        });
    </script>
</body>
</html>