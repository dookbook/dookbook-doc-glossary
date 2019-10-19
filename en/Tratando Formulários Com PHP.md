TOPIC: Tratando Formulários Com PHP
AUTHORS: Jorge Clésio; jorgepebas@gmail.com; github:jorgeclesio

# Tratando Formulários Com PHP

One of the most powerful features of PHP is the way it handles HTML forms. The basic concept that is
important to understand is that any form element will automatically be available to your PHP scripts.
Please read the manual section on [Variables from external sources](https://www.php.net/manual/en/language.variables.external.php)
for more information and examples on using forms with PHP. Here is an example HTML form:

## Exemple

```html
<form action="arquivo.php" method="post">
 <p>Nome: <input type="text" name="nnome" /></p>
 <p>idade: <input type="text" name="idade" /></p>
 <p><input type="submit" /></p>
</form>
```
