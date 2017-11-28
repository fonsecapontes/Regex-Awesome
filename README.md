# Regex-Awesome

* [Formatting](#formatting)
  * [CPF](#cpf)
  * [CNPJ](#cnpj)
* [Validation](#validation) 
 

# Formatting
Regex used for string formatting

### CPF
  ("99999999999").replace(/(\d{3})(\d{3})(\d{3})(\d{2})/g, "\$1.\$2.\$3\-\$4").
  > 999.999.999-99

### CNPJ
  ("99999999999999").replace(/(\d{2})(\d{3})(\d{3})(\d{4})(\d{2})/g, "$1.$2.$3/$4-$5")
  > 99.999.999/9999-99

# Validation
Regex used for validations
