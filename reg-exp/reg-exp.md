## basic composition

`expresson` + `quantifiers` + `assertions`

## some example 

`[ABC]`                 A or B or C
`[A-C]`                 A or B or C

`x{1,1}`                x
`x{1,5}`                x ,xx, xxx, xxxx, xxxxx

`[0-9]{1,1}`            0 - 9
`[0-9]{1,2}`            the string has `0 - 99`
`^[0-9]{1,2}$`          0 - 99

`^\d{1,2}$`             0 - 99
`^\d\d{0,1}$`           0 - 99
`^\d\d? $`              0 - 99

`\b(mail|letter)\b`     mail or letter
`\b(Eric|Eirik)\b`      Eric or Eirik 

`[^abc]`                no a , no b, no c
`0+`                    0, 00, 000, 0000 
