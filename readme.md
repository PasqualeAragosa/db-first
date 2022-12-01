Modellizzare la struttura di una tabella per memorizzare tutti i dati riguardanti delle auto usate messe in vendita da un concessionario


Table name: cars

id                  | BIGINT | NOTNULL, UNIQUE, AUTO_INCREMENT
brand               | VARCHAR(30) | NOTNULL |
model               | VARCHAR(30) | NOTNULL |
supply              | VARCHAR(30) | NULL |
color               | VARCHAR(30) | DEFAULT(white) |
vin                 | VARCHAR(30) | NOTNULL, UNIQUE
price               | DECIMAL(9, 2) | NOTNULL |
registration        | YEAR | NOTNULL |
kilometers          | MEDIUMINT | NULL |
plate               | VARCHAR(30) | NOTNULL, UNIQUE |
description         | TEXT | NULL |




NUMERI INTERI:

TINYINT             =>  1 byte     da -128 a 127                        
SMALL               =>  2 bytes    da -65.536 a 65.535
MEDIUMINT           =>  3 bytes    da -8.388.608 a -8.388.607            
INT                 =>  4 bytes    da -2.147.483.648 e 2.147.483.647     
BIGINT              =>  8 bytes    da ...



NUMERI CON VIRGOLA:

FLOAT(I, D)         =>  4 bytes
DOUBLE(I, D)        =>  8 bytes
DECIMAL(I, D)       =>  gestisce arrotondamenti di numeri financial pov
I <=> numero di cifre totali
D <=> quante delle cifre totali da dedicare alla parte decimale



STRINGHE:

VARCHAR(numero)*    =>  1 byte
TEXT                =>  2 bytes
MEDIUMTET           =>  16 mb
LONGTEXT            =>  4,2 gb
*tra le parentesi va specificato il numero di caratteri limite da inserire che non può comunque superare i 255



DATE:

DATETIME            =>  permette di memorizzare data e ora (YYYY-MM-GG HH:II:SS)
DATE                =>  contiene solo la data (YYYY-MM-GG)
TIME                =>  contiene solo l’orario (HH:II:SS)
YEAR                =>  contiene solo l’anno (YYYY)
TIMESTAMP           =>  può avere diversi formati



ATTRIBUTI:

NULL                =>  una colonna può o non può contenere NULL
NOTNULL             =>  una colonna non può contenere NULL
DEFAULT(numero)     =>  se non è presente alcun valore allora gliene viene assegnato uno di default
AUTO_INCREMENT      =>  ad ogni nuovo record il valore viene incrementato di +1
UNIQUE              =>  i valori di quella colonna devono essere unici