------------------------------------------------------------------------------------
Giselle Barbosa
Data: 18/12/2021
------------------------------------------------------------------------------------
TABUADA DE MULTIPLICAÇÃO
------------------------------------------------------------------------------------
Calcula as tabuadas e exibe seus resultados na página. Foi feito com html/css e Javascript. 

Esta página foi um exercício aprendido durante realização de aula do Curso em Video do Professor Gustavo Guanabara. 
------------------------------------------------------------------------------------
https://gisellebarbosa.github.io/Tabuada-de-Multiplica-o/
------------------------------------------------------------------------------------
CÓDIGOS
------------------------------------------------------------------------------------
<!DOCTYPE html>
<html lang="pt-br">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="author" content="Giselle Barbosa">
    <title>Tabuada de Multiplicação</title>

    <link rel="stylesheet" href="style.css">

</head>

<body>

    <header>
        <h1 class="titulo">Tabuada de Multiplicação</h1>
    </header>

    <section>
        <div>
            <h3 class="titulo2">Digite um número e veja a sua tabuada: </h3>
            <p>Número: <input title="Informe um número" type="number" name="num" id="txtn">
                <input type="button" title="Clique para calcular" value="Gerar Tabuada" onclick="tabuada()">
            </p>
        </div>

        <div class="txt">
            <select  name="tabuada" id="seltab" size="10" style="width:360px" ></select>
            <p>Informe um número acima para visualizar sua tabuada </option>
            </p>
            <option>
        </div>

    </section>

    <footer>
        <p>Giselle Barbosa - Baseado em &copy; Curso em Video</p>

    </footer>
    <script src="script.js"></script>

</body>

</html>
------------------------------------------------------------------------------------
function tabuada() {
    let num = document.getElementById('txtn')
    let tab = document.getElementById('seltab')

    if (num.value.length == 0) {
        window.alert('[ALERTA] Informe um número')

    } else {

        let n = Number(num.value)
        let c = 1

        tab.innerHTML = ''

        while (c <= 10) {
            let item = document.createElement('option')
            item.text = `${n} x ${c} = ${n * c}`
            item.value = `tab${c}`
            tab.appendChild(item)
            c++
        }
    }
} 
-----------------------------------------------------------------------------------body {
    background:#7a6a91;
    font: normal 14pt arial;
}

header {
    color: white;
    text-align: center;
}

section {
    background: #ffffff;
    border-radius: 10px;
    padding: 15px;
    width: 500px;
    margin: auto;
    box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.534);
}
.txt {
    font-size: 12pt;
}
.txt p {
    font-size: 13pt;
    text-align: center;
}

footer {
    color: white;
    font: normal 12px arial;
    text-align: center;
}
.titulo{
    font-family: montserrat;
    font-weight: 500;
}
.titulo2{
    font-size: 18pt;
    font-weight: 500;
}
