# Plano de testes para o método "obterToken" do controller [ApiController](https://gitlab.devops.ifrn.edu.br/gametime/webservice/blob/master/app/Http/Controllers/ApiController.php) da api do GameTime

Esse método deve ser executado sempre na primeira vez que o usuário se logar no sistema ou quando seu api_token expirar

## Plano de testes

<table>
    <tr>
        <td>Entrada</td>
        <td>Condição</td>
        <td>Classe válida</td>
        <td>Classe inválida</td>
    </tr>
    <tr>
        <td>A entrada é um objeto Request</td>
        <td>O método da Request deve ser POST com os campos [email, password]</td>
        <td>Método da Request é POST</td>
        <td>Método da Request não é POST</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Campo email da Request é preenchido</td>
        <td>Campo email da Request é vazio</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Campo email possui texto na formatação padrão de email</td>
        <td>Campo email não segue a regra de formatação de textos para email</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Campo senha da Request é preenchido</td>
        <td>Campo senha da Request é vazio</td>
    </tr>
</table>

# Plano de testes para o método "buscar" do controller [GameController](https://gitlab.devops.ifrn.edu.br/gametime/webservice/blob/master/app/Http/Controllers/GameController.php) da api do GameTime

Esse método serve para o usuário fazer buscas de jogos dentro da plataforma.

## Plano de testes

<table>
    <tr>
        <td>Entrada</td>
        <td>Condição</td>
        <td>Classe válida</td>
        <td>Classe inválida</td>
    </tr>
    <tr>
        <td>A entrada é um objeto Request</td>
        <td>O método da Request deve ser GET, obrigatoriamente com o campo [api_token] com um token válido e podendo ter os campos [titulo, data_lancamento, genero, plataformas]</td>
        <td>O método da Request é GET</td>
        <td>O método da Request não é GET</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>O campo api_token não é vazio</td>
        <td>O campo api_token é vazio</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>O api_token é um token válido</td>
        <td>O api_token é um token inválido</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>O campo título não é vazio</td>
        <td></td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>O campo data_lancamento não é vazio</td>
        <td>O campo data_lancamento não está no formato Y-m-d</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>O campo genero não é vazio</td>
        <td></td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>O campo plataformas não é vazio</td>
        <td></td>
    </tr>
</table>
