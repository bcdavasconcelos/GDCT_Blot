tags: Apps, macOS
permalink: /bbedit

# BBEdit

O [BBEdit](https://www.barebones.com/products/bbedit/) (apenas macOS) é o processador que passo mais tempo utilizando. É mais rápido do que o bloco de notas, abre praticamente qualquer tipo de arquivo contendo texto (incluindo até mesmo imagens de disco, i.e. arquivos **.dmg**), é capaz de fazer buscas e substituições em pastas inteiras sem a necessidade de abrir qualquer arquivo e possui uma ferramenta especial, o *text factory*, que é muito útil para automatizar certos processos com texto. Além disso, é o que está melhor integrado ao macOS e pode ser utilizado indefinidamente com as funções mais importantes sem a necessidade de uma licença (mas para acessar tudo que o aplicativo oferece é preciso adquirir uma).

## Algumas utilidades

### Tornar markdown o formato padrão para novos arquivos

```bash
defaults write com.barebones.bbedit DefaultLanguageNameForNewDocuments -string "Markdown"
```


### Comparar dois arquivos de texto selecionados no DEVONthink

```applescript
property err : " is not a plain text file." -- Just a default error message as a convenience

tell application id "DNtp"
	
	set theRecords to the selection
	if (count selection) = 2 then -- Verify only two files are selected

-- Check Record 1
set theRecord1 to item 1 of theRecords
set recType to type of theRecord1 -- Get the type
if (recType as string) = "text" then -- If it's plain text, proceed
	set thePath1 to the path of theRecord1 -- Get the file path
else
	display alert "Record 1 " & err -- If it's not plain text, alert and stop.
	return
end if

-- Check Record 2, if 1 passes…
set theRecord2 to item 2 of theRecords
set recType to type of theRecord2
if (recType as string) = "text" then
	set thePath2 to the path of theRecord2
else
	display alert "Record 2" & err
	return
end if

	else -- If two files aren't selected, alert and stop.
display alert "Please select two plain text files to compare."
return
	end if
end tell

tell application "BBEdit"
	set theResult to compare file (thePath1 as POSIX file) against file (thePath2 as POSIX file)
	activate
end tell

```


### Comparar dois arquivos de texto selecionados no Finder

```
tell application "Finder" to set sel to the selection

if (count of sel) is 2 then

tell application "BBEdit"
compare (item 1 of sel as alias) against (item 2 of sel as alias)
end tell

end if
```