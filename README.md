# Regex-Awesome

* [Formatting](#formatting)
  * [CPF](#cpf)

# Formatting

### CPF
  ("99999999999").replace(/(\d{3})(\d{3})(\d{3})(\d{2})/g, "\$1.\$2.\$3\-\$4").
  > 999.999.999-99
