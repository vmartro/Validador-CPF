# Validador de CPF — C#

Aplicação de console em C# que valida números de CPF seguindo as regras oficiais da Receita Federal brasileira.

---

## Funcionalidades

- Aceita CPFs formatados (`123.456.789-09`) ou apenas numéricos (`12345678909`)
- Valida o comprimento e os caracteres da entrada
- Rejeita CPFs com todos os dígitos iguais (ex: `111.111.111-11`)
- Calcula e verifica os dois dígitos verificadores pelo algoritmo oficial

---

## Como usar

### Pré-requisitos

- [.NET SDK](https://dotnet.microsoft.com/download) 6.0 ou superior

### Executando

```bash
dotnet run
```

O programa solicitará que você digite um CPF e informará se ele é válido ou inválido.

```
Digite o CPF a ser validado:
123.456.789-09
O CPF 123.456.789-09 é válido!
```

---

## Como funciona

A validação segue o algoritmo oficial da Receita Federal:

1. Remove pontos e traços da entrada
2. Verifica se o CPF possui exatamente 11 dígitos
3. Rejeita sequências com todos os dígitos iguais
4. Calcula o **primeiro dígito verificador** multiplicando os 9 primeiros dígitos pelos pesos de 10 a 2 e aplicando a regra do módulo 11
5. Calcula o **segundo dígito verificador** multiplicando os 10 primeiros dígitos pelos pesos de 11 a 2 e aplicando a mesma regra
6. Compara os dígitos calculados com os dígitos presentes no CPF

---

## Estrutura do projeto

```
ValidadorCPFCSharp/
├── ValidadorCPFCSharp.cs   # Código-fonte principal
└── README.md               # Leia-me
└── LICENSE                 # Licença MIT
```

---

## Licença

*Distribuído livremente para fins educacionais.*
