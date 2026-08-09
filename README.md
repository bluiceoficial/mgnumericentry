# MGNumericEntry

[![License](https://img.shields.io/badge/license-PolyForm%20Perimeter%201.0.1-5351FB)](LICENSE.md)

Um componente customizado para **Fyne (Go)** que fornece um **campo de entrada numérica** com validação, limites (min/max), incremento/decremento e **botões de spin com auto-repeat** (pressionar e segurar).

Ideal para formulários, configurações e interfaces desktop que precisam de controle numérico preciso.

---

## ✨ Recursos

* 🔢 Entrada **somente numérica**
* ➕➖ Incremento e decremento com passo configurável
* ⏫⏬ Botões de spin (▲ / ▼) com **auto-repeat**
* 🔒 Respeita valores mínimos e máximos
* 🔄 Callback `OnChanged` ao alterar valor
* 🖱️ Suporte a mouse, teclado e foco

---

## 📦 Instalação

```bash
go get github.com/profmugomes/mgnumericentry
```

---

## 🚀 Uso básico

### Numeric Entry simples

```go
entry := mgnumericentry.NewMGNumericEntry(0, 100, 10)

entry.OnChanged = func(v int) {
	fmt.Println("Valor alterado:", v)
}
```

---

### Numeric Entry com botões de incremento/decremento

```go
box, entry := mgnumericentry.NewMGNumericEntryWithButtons(0, 100, 5)

entry.OnChanged = func(v int) {
	fmt.Println("Novo valor:", v)
}

w.SetContent(box)
```

---

## ⚙️ Propriedades principais

### `MGNumericEntry`

| Campo       | Tipo        | Descrição                      |
| ----------- | ----------- | ------------------------------ |
| `Min`       | `int`       | Valor mínimo permitido         |
| `Max`       | `int`       | Valor máximo permitido         |
| `Value`     | `int`       | Valor atual                    |
| `OnChanged` | `func(int)` | Callback ao alterar o valor    |

---

## 🧠 Métodos úteis

```go
entry.GetValue()
entry.SetValue(42)
```

---

## 🧩 Compatibilidade

* Go 1.26.5+
* Fyne 2.8.0

---

## 👤 Autor

**Murilo Gomes Julio**

🔗 [https://www.profmugomes.com.br](https://www.profmugomes.com.br)

📺 [https://youtube.com/@profmugomes](https://youtube.com/@profmugomes)

---

## License

Copyright (c) 2025-2026 Murilo Gomes Julio. All Rights Reserved.

This project is licensed under the PolyForm Perimeter License 1.0.1.

### Summary

This software is available for commercial and noncommercial use, subject to the terms of the PolyForm Perimeter License 1.0.1.

You may:

* ✔ Use the software for commercial and noncommercial purposes.
* ✔ Inspect and study the source code.
* ✔ Modify the software.
* ✔ Create derivative works based on the software.
* ✔ Redistribute the software and permitted modifications.

You may not:

* ✖ Provide a product that competes with the software.

See the full license terms at LICENSE.md.

This summary is provided for convenience only and does not replace or modify the full license terms.
