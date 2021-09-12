<!DOCTYPE html>
<html lang="pt-BR">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>site basico com JS</title>
    <style>
        body {
            background-color: lightslategrey;
            background-image: url(data:image/jpeg;base64,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);
            background-position: center;
            background-repeat: no-repeat;
        }

        div {
            display: inline-grid;
            background-color: brown;
            width: 200px;
            height: 200px;
            line-height: 200px;
            text-align: center;
            margin: 17%;
        }

        p {
            font-size: larger;
            text-transform: uppercase;
        }
    </style>
</head>

<body>
    <div id="n1">

        <p>primeiro</p>
        <script>
            var divs = document.getElementById('n1')
            divs.addEventListener('click', primeiro)
            divs.addEventListener('mouseenter', segundo)
            divs.addEventListener('mouseout', terceiro)
            function primeiro() {
                divs.innerText = 'interagindo'
                divs.style.background = 'black'
            }
            function segundo() {
                divs.innerText = 'entrou'
                divs.style.color = 'white'


            }
            function terceiro() {
                divs.innerText = 'saiu'
                divs.style.fontFamily = 'Arial'
                divs.style.fontSize = '30px'

            }
        </script>
    </div>
    <div id="n2">
        <p>segundo</p>
        <script>
            var d = document.getElementById('n2')
            d.addEventListener('click', clicou)
            d.addEventListener('mouseenter', entrou)
            d.addEventListener('mouseout', saiu)
            function entrou() {
                d.innerText = ' segundo'
                d.style.color = 'white'
            }
            function clicou() {
                d.innerText = 'entrou'
                d.style.color = 'white'
                d.style.background = 'yellow'


            }
            function saiu() {
                d.innerText = 'saiu'
                d.style.fontFamily = 'Arial'
                d.style.fontSize = '30px'

            }
        </script>
    </div>
    <div id="n3">
        <p>terceiro</p>
        <script>
            var t = document.getElementById('n3')
            t.addEventListener('click', clicou)
            t.addEventListener('mouseenter', entrou)
            t.addEventListener('mouseout', saiu)
            function entrou() {
                t.innerText = ' entrou'
                t.style.color = 'white'
            }
            function clicou() {
                t.innerText = 'entrou'
                t.style.color = 'white'
                t.style.background = 'blue'


            }
            function saiu() {
                t.innerText = 'saiu'
                t.style.fontFamily = 'Arial'
                t.style.fontSize = '30px'

            }
        </script>
    </div>
    <div id="n4">
        <p>quarto</p>
        <script>
            var a = document.getElementById('n4')
            a.addEventListener('click', clicou)
            a.addEventListener('mouseenter', entrou)
            a.addEventListener('mouseout', saiu)
            function entrou() {
                a.innerText = ' entrou'
                a.style.color = 'white'
            }
            function clicou() {
                a.innerText = 'entrou'
                a.style.color = 'white'
                a.style.background = 'red'


            }
            function saiu() {
                a.innerText = 'saiu'
                a.style.fontFamily = 'Arial'
                a.style.fontSize = '30px'

            }
        </script>
    </div>

</body>

</html>
