```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>STREETLAB | Streetwear</title>

<link href="https://fonts.googleapis.com/css2?family=Oswald:wght@400;500;600;700&family=DM+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

:root {
    --preto: #101010;
    --cinza: #191919;
    --branco: #f7f5f0;
    --vermelho: #e62b38;
    --azul: #244cff;
}

html {
    scroll-behavior: smooth;
}

body {
    background: var(--branco);
    color: var(--preto);
    font-family: 'DM Sans', sans-serif;
}

a {
    text-decoration: none;
    color: inherit;
}

button {
    cursor: pointer;
    font-family: inherit;
}

/* BARRA SUPERIOR */

.aviso {
    background: var(--vermelho);
    color: white;
    text-align: center;
    padding: 10px;
    font-size: 10px;
    font-weight: 800;
    letter-spacing: 2px;
}

/* CABEÇALHO */

header {
    height: 80px;
    padding: 0 7%;
    background: var(--preto);
    color: white;
    display: flex;
    align-items: center;
    justify-content: space-between;
    position: sticky;
    top: 0;
    z-index: 100;
}

.logo {
    font-family: 'Oswald', sans-serif;
    font-size: 30px;
    font-weight: 700;
    letter-spacing: -1px;
}

.logo span {
    color: var(--vermelho);
}

nav {
    display: flex;
    gap: 30px;
}

nav a {
    font-size: 11px;
    font-weight: 800;
    letter-spacing: 1px;
    transition: .3s;
}

nav a:hover {
    color: var(--vermelho);
}

.carrinho-btn {
    background: transparent;
    border: 1px solid #555;
    color: white;
    padding: 12px 16px;
    font-size: 11px;
    font-weight: 800;
}

#quantidade {
    color: var(--vermelho);
    margin-left: 8px;
}

/* CAPA */

.hero {
    min-height: 620px;
    background: var(--preto);
    color: white;
    display: grid;
    grid-template-columns: 1fr 1fr;
    align-items: center;
    padding: 60px 8%;
    gap: 40px;
    overflow: hidden;
}

.etiqueta {
    color: var(--vermelho);
    font-size: 11px;
    font-weight: 800;
    letter-spacing: 4px;
    margin-bottom: 25px;
}

.hero h1 {
    font-family: 'Oswald', sans-serif;
    font-size: clamp(65px, 9vw, 115px);
    line-height: .9;
    text-transform: uppercase;
    letter-spacing: -3px;
}

.hero h1 span {
    color: var(--vermelho);
}

.hero p.descricao {
    color: #bdbdbd;
    max-width: 390px;
    line-height: 1.9;
    font-size: 13px;
    margin: 28px 0;
}

.botao {
    display: inline-block;
    background: var(--vermelho);
    color: white;
    padding: 17px 23px;
    border: none;
    font-size: 10px;
    font-weight: 800;
    letter-spacing: 1.5px;
    transition: .3s;
}

.botao:hover {
    background: var(--azul);
    transform: translateY(-3px);
}

.hero-imagem {
    height: 470px;
    position: relative;
}

.hero-imagem img {
    height: 100%;
    width: 100%;
    object-fit: cover;
    filter: grayscale(100%);
}

.selo {
    position: absolute;
    bottom: 25px;
    left: -25px;
    background: var(--vermelho);
    color: white;
    padding: 25px;
    font-family: 'Oswald', sans-serif;
    font-size: 22px;
    font-weight: 700;
    transform: rotate(-8deg);
}

/* FAIXA */

.faixa {
    background: var(--azul);
    color: white;
    overflow: hidden;
    padding: 17px;
    text-align: center;
    font-family: 'Oswald', sans-serif;
    font-size: 17px;
    letter-spacing: 3px;
}

/* COLEÇÃO */

.colecao {
    padding: 100px 8%;
}

.titulo-secao {
    display: flex;
    justify-content: space-between;
    align-items: end;
    margin-bottom: 35px;
}

.titulo-secao small {
    color: var(--vermelho);
    font-size: 10px;
    font-weight: 800;
    letter-spacing: 3px;
}

.titulo-secao h2 {
    font-family: 'Oswald', sans-serif;
    font-size: 55px;
    line-height: 1;
    margin-top: 10px;
}

.titulo-secao p {
    font-size: 12px;
    line-height: 1.8;
    color: #777;
}

.filtros {
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
    margin-bottom: 30px;
}

.filtro {
    padding: 12px 16px;
    border: 1px solid #ddd;
    background: transparent;
    font-size: 10px;
    font-weight: 800;
    transition: .3s;
}

.filtro.ativo,
.filtro:hover {
    background: var(--preto);
    color: white;
}

.produtos {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 30px 20px;
}

.produto {
    position: relative;
}

.foto-produto {
    height: 350px;
    background: #e8e8e8;
    overflow: hidden;
    position: relative;
}

.foto-produto img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: .5s;
}

.produto:hover .foto-produto img {
    transform: scale(1.06);
}

.tag-produto {
    position: absolute;
    top: 12px;
    left: 12px;
    background: var(--vermelho);
    color: white;
    padding: 8px 10px;
    font-size: 9px;
    font-weight: 800;
}

.adicionar {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    border: none;
    background: var(--preto);
    color: white;
    padding: 15px;
    font-size: 10px;
    font-weight: 800;
    letter-spacing: 
