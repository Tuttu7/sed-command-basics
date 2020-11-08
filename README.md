#### SED is a powerful text stream editor.

#### This command will read each line and print it out :
```
$ sed '' test1.txt 
I'm hoping to write a sample ltter
which contains the number of orders 
to be provisioned for the next week
a bunch of flowers for the shop
```
#### To leave the first line of the file :
```
$ sed '1d' test1.txt
which contains the number of orders 
to be provisioned for the next week
```
#### To print only the first line :
```
$ sed '1!d' test1.txt
I'm hoping to write a sample ltter
```
#### To leave every line with the word 'the' :
```
$ sed '/the/d' test1.txt
I'm hoping to write a sample ltter
```
#### To leave every line with multiple words 'the' and 'next' :
```
$ sed '/the/,/next/d' test1.txt
I'm hoping to write a sample ltter
```
#### To replace the words using sed command :
#### In this example the word 'to' is replaced with word 'with' but only the first line is replaced.
```
$ sed 's/to/with/' test1.txt
I'm hoping with write a sample ltter
which contains the number of orders 
with be provisioned for the next week
```
#### To replace all the matching words in each line :
```
$ sed 's/the/WITH/g' test1.txt
I'm hoping to write a sample ltter
which contains WITH number of orders 
to be provisioned for WITH next week
```
#### To replace the changes only in 2nd line :
```
$ sed '2s/the/WITH/g' test1.txt
I'm hoping to write a sample ltter
which contains WITH number of orders 
to be provisioned for the next week
```
#### Multiple comands with in a sed command sequene :
#### This command is to leave the first line and replace the word 'contains' with word 'WITH' in the second line.
```
$ sed '1d;2s/contains/WITH/g' test1.txt
which WITH the number of orders 
to be provisioned for the next week
```
#### To insert blank spaces between each lines

```
sed G clean.txt
```

#### To inset double blanks paces between each lines
`
```
sed 'G:G' clean.txt
```

#### To delete blank spaces between the lines 

```
sed '/^$/d' clean.txt > output.txt
```

