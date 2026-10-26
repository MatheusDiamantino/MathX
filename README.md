# MathX 🧮

Gerador de exercícios de matemática feito em Laravel: você escolhe as operações, o intervalo de números e a quantidade, e o app monta a lista com as soluções.

## Contexto

Projeto de estudo para praticar Laravel 11 (rotas, controllers, validação de formulários, sessão e views Blade).

## Funcionalidades

- Escolha das operações: **soma, subtração, multiplicação e divisão** (pelo menos uma).
- Intervalo de números configurável (mínimo e máximo entre 0 e 999).
- De **5 a 50 exercícios** por geração, com operações sorteadas.
- Soluções calculadas automaticamente (divisões arredondadas para 2 casas).
- Validação do formulário com mensagens de erro.
- **Impressão** da lista de exercícios e soluções.
- **Exportação** das soluções em arquivo `.txt`.

## Stack

- PHP 8.2+ e Laravel 11
- Blade e Bootstrap 5
- Vite (configuração padrão do Laravel)

Não usa banco de dados: os exercícios gerados ficam na sessão.

## Como rodar localmente

```bash
git clone https://github.com/MatheusDiamantino/MathX.git
cd MathX
composer install
cp .env.example .env
php artisan key:generate
php artisan serve
```

Acesse `http://localhost:8000`.

## Rotas

| Método | Rota | Descrição |
| --- | --- | --- |
| GET | `/` | Formulário de configuração |
| POST | `/generate-exercises` | Gera os exercícios |
| GET | `/print-exercises` | Versão para impressão |
| GET | `/export-exercises` | Download em `.txt` |
