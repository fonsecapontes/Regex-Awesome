# Regex-Awesome

* [Formatting](#formatting)
  * [CEP](#cep)
  * [CNPJ](#cnpj)
  * [CPF](#cpf)
* [Validation](#validation) 
  * [Date dd/MM/yyyy](#date-ddmmyyyy)
  * [Integer Negative](#integer-negative)
  * [Integer Positive](#integer-positive)
  * [Integer Positive or Negative](#integer-positive-or-negative)
  * [IP](#ipv4)  
  * [Mail](#mail)  
  * [Time](#time)
  * [URL](#url)  

# Formatting
Regex used for string formatting

### CEP
  `("99999999").replace(/(\d{5})(\d{3})/g, "$1-$2")`
  > 99999-999

### CNPJ
  `("99999999999999").replace(/(\d{2})(\d{3})(\d{3})(\d{4})(\d{2})/g, "$1.$2.$3/$4-$5")`
  > 99.999.999/9999-99
  
### CPF
  `("99999999999").replace(/(\d{3})(\d{3})(\d{3})(\d{2})/g, "\$1.\$2.\$3\-\$4")`
  > 999.999.999-99 

# Validation
Regex used for validations

### Date dd/MM/yyyy
  `^(?:(?:31(\/|-|\.)(?:0?[13578]|1[02]))\1|(?:(?:29|30)(\/|-|\.)(?:0?[1,3-9]|1[0-2])\2))(?:(?:1[6-9]|[2-9]\d)?\d{2})$|^(?:29(\/|-|\.)0?2\3(?:(?:(?:1[6-9]|[2-9]\d)?(?:0[48]|[2468][048]|[13579][26])|(?:(?:16|[2468][048]|[3579][26])00))))$|^(?:0?[1-9]|1\d|2[0-8])(\/|-|\.)(?:(?:0?[1-9])|(?:1[0-2]))\4(?:(?:1[6-9]|[2-9]\d)?\d{2})$`
  > 31/01/2017 => true <br />
  > 31/02/2017 => false
  
### Integer Negative
  `^-\d+$`
  > -10 => true <br />
  > 100 => false  
  
### Integer Positive
  `^\d+$`
  > 100 => true <br />
  > -10 => false
  
### Integer Positive or Negative
  `^-?\d+$`
  > 100 => true <br />
  > -10 => true <br />
  > AAA => false
  
### IPv4
  `^(([0-9]|[1-9][0-9]|1[0-9]{2}|2[0-4][0-9]|25[0-5])\.){3}([0-9]|[1-9][0-9]|1[0-9]{2}|2[0-4][0-9]|25[0-5])$`
  > 192.168.0.1 => true

### Mail
  `^([a-zA-Z0-9_\-\.]+)@([a-zA-Z0-9_\-\.]+)\.([a-zA-Z]{2,5})$`
  > mail@domain.com => true
  
### Time
  `^([0-9]|0[0-9]|1[0-9]|2[0-3]):[0-5][0-9]$`
  > 18:56 => true

### URL
  `(http|ftp|https)://([\w_-]+(?:(?:\.[\w_-]+)+))([\w.,@?^=%&:/~+#-]*[\w@?^=%&/~+#-])?`
  > https://www.domain.com => true

