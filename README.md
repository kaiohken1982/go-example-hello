## Go basic example

Hello world con GO.
Inoltre è presente l'utilizzo di una lib locale ( https://github.com/kaiohken1982/go-example-lib-greetings ), 
che deve esistere prima di lanciare i seguenti comandi ( effettua il checkout )

Struttura cartelle

```
greetings-dir
hello-dir
```

Esegui tidy

```
go mod tidy
```

Aggiungi il riferimento al modulo esterno locale

```
replace example.com/greetings => ../greetings
```

Lancia tidy 

```
go mod tidy
```

Nel file mod sarà inserito questo contenuto

```
[...]
require example.com/greetings v0.0.0-00010101000000-000000000000

replace example.com/greetings => ../greetings
```

Compila con 

```
go build
```

esegui con 

```
go .
```