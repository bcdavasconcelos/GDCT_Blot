tags: Scripts, Bookends, Tinderbox
permalink: /tbx-be

# Movendo referências do Bookends para o Tinderbox

<script src="prism.js"></script>

Esse script move as referências selecionadas no Bookends para o Tinderbox. A vantagem desse script com relação ao método tradicional (clicando e arrastando a referência do Bookends segurando ⌘⌥ para o Tinderbox) é que o script não ignora campos como "Tradutor", "Editor", "Bibkey" e "Short Title". É importante observar que é preciso criar antes um *prototype* com esses campos no Tbx.   


```language-applescript
use AppleScript version "2.4" -- Yosemite (10.10) or later
use scripting additions

-- Bcdav (2021-02-26-16-48)


tell application "Bookends"
	tell front library window
		
		-- Get selected publication 
		set theRefs to selected publication items
		set theRefsNo to count of theRefs
		
		repeat with theRef in theRefs
			
			
			-- Get properties of selected reference
			set theType to type of theRef as text
			set theID to id of theRef
			set theAbstract to abstract of theRef
			set theAuthors to authors of theRef
			set theEditor to editors of theRef
			set theTitle to title of theRef
			set theAbstract to abstract of theRef
			set thePublisher to publisher of theRef
			set theLocation to location of theRef
			set theVolume to volume of theRef
			set theKeywords to keyword names of theRef
			set theKeywords2 to keywords of theRef
			set theDate2 to publication date string of theRef
			set theURL2 to url of theRef
			-- set theUUID to my replacetext(theURL2, "x-devonthink-item://", "")
			set theISBN to isbn of theRef
			set theDOI to doi of theRef
			set theTranslator to user3 of theRef
			set theBibkey to user1 of theRef
			set thePages to pages of theRef
			set theIssue to volume of theRef
			set theNotes to notes of theRef
			set theLanguage to language of theRef
			set theAttachments to attachments of theRef
			set theJournal to journal of theRef
			set theShortTitle to short title of theRef
			set theFormattedReference to format theRef using "ABNT.fmt"
			-- set theShortTitle to format theRef using "Rename.fmt"
			--set theNameRec to theAuthors & " " & theDate2 & " " & theTitle
			
			if theType is "1" then set theType to "Artwork"
			if theType is "2" then set theType to "Book"
			if theType is "3" then set theType to "Book Chapter"
			if theType is "4" then set theType to "Conference Proceedings"
			if theType is "5" then set theType to "Dissertation"
			if theType is "6" then set theType to "Edited Book"
			if theType is "7" then set theType to "Editorial"
			if theType is "8" then set theType to "In Press"
			if theType is "9" then set theType to "Journal Article"
			if theType is "10" then set theType to "Letter"
			if theType is "11" then set theType to "Map"
			if theType is "12" then set theType to "Newspaper Article"
			if theType is "13" then set theType to "Patent"
			if theType is "14" then set theType to "Personal communication"
			if theType is "15" then set theType to "Review"
			if theType is "16" then set theType to "Internet"
			if theType is "17" then set theType to "Ed. Crítica"
			if theType is "18" then set theType to "Trans Book"
			if theType is "19" then set theType to "Ed. Crítica"
			if theType is "20" then set theType to "Bekker"
			if theType is "21" then set theType to ""
			
			
			try
				set {od, AppleScript's text item delimiters} to {AppleScript's text item delimiters, ", "}
				set theTags to keyword names of theRef
				set theTags to (theTags as string)
			end try
			
			set theFormattedReference to format theRef using "ABNT.fmt"
			
			tell application "Tinderbox 8"
				tell front document
					if not (exists) then error "No Tinderbox document open."
					
					set newNote to make new note
					
					tell newNote
						
						set value of attribute "Prototype" to "Reference"
						-- set value of attribute "Name" to "@" & theCitation
						set value of attribute "Text" to theFormattedReference & linefeed & theAbstract & linefeed & theNotes
						set value of attribute "Authors" to theAuthors
						set value of attribute "Editor" to theEditor
						set value of attribute "Translator" to theTranslator
						set value of attribute "PublicationCity" to theLocation
						set value of attribute "Publisher" to thePublisher
						set value of attribute "PublicationYear" to theDate2
						set value of attribute "Journal" to theJournal
						set value of attribute "RefKeywords" to theTags
						set value of attribute "URL" to "bookends://sonnysoftware.com/" & theID
						set value of attribute "Abstract" to theAbstract
						set value of attribute "BibTexKey" to theBibkey
						set value of attribute "ReferenceShortTitle" to theShortTitle
						set value of attribute "Type" to theType
						set value of attribute "Language" to theLanguage
						
						
						if theType is "Edited Book" then
							set value of attribute "BookTitle" to theTitle
						end if
						
						if theType is "Ed. Crítica" then
							set value of attribute "BookTitle" to theTitle
						end if
						
						if theType is "Trans Book" then
							set value of attribute "BookTitle" to theTitle
						end if
						
						if theType is "Book" then
							set value of attribute "BookTitle" to theTitle
						end if
						
						if theType is "Journal Article" then
							set value of attribute "ArticleTitle" to theTitle
						end if
						
						if theType is "Book Chapter" then
							set value of attribute "ArticleTitle" to theTitle
							set value of attribute "BookTitle" to theVolume
						end if
						
						if theType is "Bekker" then
							set value of attribute "ArticleTitle" to theTitle
							set value of attribute "BookTitle" to theVolume
						end if
						
						set NoteURL to value of attribute "NoteURL"
						
					end tell
				end tell
			end tell
			
			set user8 of publication item id theID to NoteURL
			
		end repeat
	end tell
end tell
```