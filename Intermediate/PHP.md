# PHP Developer

## (PT-BR) Cursos relevantes Alura
Formação Desenvolvedor PHP
Formação voltada para quem deseja se tornar um desenvolvedor PHP completo, abordando desde os conceitos básicos até tópicos avançados. Inclui:
- **PHP Básico:** Conceitos iniciais, loops e manipulação de dados.
- **Orientação a Objetos:** Classes, métodos, herança e polimorfismo.
- **Banco de dados:** Integração com MySQL e PDO.
- **Frameworks:** Introdução ao Laravel e Symfony.
> https://cursos.alura.com.br/formacao-desenvolvedor-php-felipemoreno-1559341630327-p1815

Formação Avançado em PHP
Esta formação é ideal para quem deseja aprofundar seus conhecimentos no ecossistema PHP moderno. Ela abrange:
- **PHP Moderno:** Introdução ao PHP moderno e boas práticas de desenvolvimento.
- **PHP com Banco de Dados:** Utilização do PDO para acessar bancos de dados.
- **PHP para a Web:** Criação de serviços MVC e REST com frameworks populares.
> https://cursos.alura.com.br/formacao-avancando-php

Plano de Estudo PHP completo
Oferece uma sequência de 6 cursos, abrangendo:
- **PHP básico e Avançado:** Desde loops até programação funcional.
- **Orientação a Objetos:** Classes, interfaces e SOLID.
- **Frameworks:** Laravel, Symfony 

# notes

📄 Sintaxe básica:
Todo código PHP fica dentro de:
```
<?php
// seu código aqui
?>

```

📥 Variáveis:
Sempre começam com $
```
<?php
$nome = "Lorran";
$idade = 28;
?>
```

Estruturas de Controle:
```
<?php
if ($idade > 18) {
  echo "Maior de idade";
} else {
  echo "Menor de idade";
}

for ($i = 0; $i < 10; $i++) {
  echo $i;
}

while ($idade < 30) {
  $idade++;
}
?>

```

Funções:
```
<?php
function soma($a, $b) {
  return $a + $b;
}
echo soma(5, 10);
?>

```

Programação Orientada a Objetos (POO):
```
<?php
class Pessoa {
  public $nome;
  
  function __construct($nome) {
    $this->nome = $nome;
  }
  
  function apresentar() {
    echo "Meu nome é $this->nome";
  }
}

$pessoa = new Pessoa("Lorran");
$pessoa->apresentar();
?>
```

Trabalhando com Banco de Dados (MySQLi):
```
<?php
$conn = new mysqli("localhost", "usuario", "senha", "banco");

if ($conn->connect_error) {
  die("Falha: " . $conn->connect_error);
}

$sql = "SELECT nome FROM clientes";
$result = $conn->query($sql);

while($row = $result->fetch_assoc()) {
  echo $row["nome"];
}

$conn->close();
?>
```

Segurança:

Sempre usar prepared statements para evitar SQL Injection.
Validar e sanitizar dados de entrada.
Cuidar com XSS e CSRF.

Manipulação de Arquivos:
```
<?php
$file = fopen("arquivo.txt", "r");
echo fread($file, filesize("arquivo.txt"));
fclose($file);
?>
```

Sessões e Cookies:
```
<?php
session_start();
$_SESSION["usuario"] = "Lorran";

setcookie("visita", "hoje", time() + 3600);
?>
```

Principais ferramentas/frameworks PHP:
Laravel (framework MVC)
Symfony
Composer (gerenciador de dependências)
PHPUnit (testes)
Slim (microframework)

Práticas modernas:
Sempre usar PHP 8.x+
Trabalhar com namespaces e autoload (Composer).
Separar lógica de apresentação (MVC).
Escrever testes automatizados.
Usar ORM (ex.: Eloquent no Laravel).


