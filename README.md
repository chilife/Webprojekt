## Readme

### Einführung:
Unser Webprojekt soll dazu dienen, ein WG Abrechnungstool abzubilden, um den Finanzhaushalt von Wohngemeinschaften zu vereinfachen.
Dazu lassen sich User anlegen, die dann entweder eine WG erstellen oder einer bereits vorhandenen WG beitreten können. Jeder User darf maximal eine WG haben. 

##### Rollen: 
In jeder WG gibt es einen User mit der Rolle 'Owner', der Mitglieder akzeptieren oder ablehnen kann.
Zusätzlich kann er Einstellungen an einer WG vornehmen und Kategorien für Einkaufsquittungen anlegen.
Die anderen WG-Mitglieder haben die Rolle "Member". Diese können, wie auch der 'Owner', Belege anlegen, die Ausgaben von allen Mitgliedern kommentieren und ihre eigenen Belege bearbeiten oder löschen. Es lassen sich Monatsabrechnungen aufrufen sowohl textuell als auch grafisch.
##### WG löschen/User löschen/WG verlassen
###### Admin: 
* Account löschen: Löscht ein Admin seinen Account, werden alle seine Userdaten gelöscht. 		Er verlässt die WG. Dort werden alle seine Belege und deren Kommentare gelöscht. Die Admin Rechte werden an den nächsten Nutzer abgegeben(falls vorhanden), sonst wird die gesamte WG gelöscht.
* WG löschen: Alle WG Daten werden gelöscht. Die Rollen der User ändern sich auf die eines neu registrierten Users.
* Als Admin ernennen und in der WG bleiben: ein ausgewählter Nutzer wird zum Admin ernannt, der aktuelle Admin wird Member
* Als Admin ernenne und WG verlassen: Admin erhält Rolle Registered, die gemeinsamen WG Belege werden gelöscht, die eigenen Belege bleiben erhalten.

###### Member: 
* WG verlassen: Alle gemeinsamen Belege und deren Kommentare werden gelöscht. Der User erhält die Rolle registered.
* Account löschen: Alle Userdaten werden gelöscht. Die privaten WG Belege der restlichen WG-Mitglieder bleiben erhalten.

## Installationshinweise
Ruby:	ruby 1.9.3p327

##### git clone "https://www.github.com/dep87/wg.git"
###### Linux: 
	* apt-get install wkhtmltopdf
	* apt-get install imagemagick
###### Mac: 
	* brew install wkhtmltopdf
	* brew install imagemagick
##### bundle install
##### rake db:migrate
##### rake db:seed

## Testdaten
Folgende Testdaten können verwendet werden:
* Active Admin: "admin@pay.de" PW: "admin123"

##### WG: PlaceToBe
* Owner: email: "lily@pay.de" 
* Member: email: "marshall@pay.de", "barkeeper@pay.de"
* Applicant: email: "baby@pay.de"
* Declined: email: "barney@pay.de"
* Registered: email: "ted@pay.de", "robin@pay.de"
* Das Passwort lautet "hackme", falls nicht anders angegeben.

##### WG: Capitol
* Owner: email: "bernd@pay.de" 
* Member: email: "ulf@pay.de", "ernie@pay.de"
* Applicant: email: "tanja@pay.de", "erika@pay.de"
* Declined: email: "lars@pay.de", "frank@pay.de"
* Registered: email: "jennifer@pay.de", "sabbel@pay.de"
* Das Passwort lautet "hackme", falls nicht anders angegeben.

##### WG: Simpsons
* Owner: email: "homer@pay.de" 
* Member: email: "marge@pay.de", "bart@pay.de"
* Applicant: email: "lisa@pay.de", "maggie@pay.de"
* Declined: email: "krusty@pay.de", "grampa@pay.de"
* Registered: email: "ned@pay.de", "milhouse@pay.de"
* Das Passwort lautet "hackme", falls nicht anders angegeben.

##Gems
Folgende Gems wurden benutzt:
* gem 'rails', '3.2.9'
* gem 'jquery-rails'
* gem 'devise'
* gem 'cancan'
* gem 'therubyracer', '0.10.2'
* gem 'twitter-bootstrap-rails'
* gem 'paperclip'
* gem 'paperclip-dropbox'
* gem "googlecharts", :require => "gchart"
* gem "dynamic_form"
* gem 'bootstrap-datepicker-rails'
* gem 'wicked_pdf'
* gem 'wkhtmltopdf-binary'
* gem 'activeadmin'
* gem 'rspec-rails'
* gem 'factory_girl_rails'
* gem 'capybara'
* gem 'guard-rspec'
* gem 'faker'
* gem 'sqlite3'
* gem 'libv8'
* gem 'pg'
* gem 'sass-rails', '~> 3.2.3'
* gem 'coffee-rails', '~> 3.2.1'
* gem 'uglifier', '>= 1.0.3'
* gem 'less-rails'

## Bei Fragen oder Anregungen
##### Stephan Depenwisch
* stephan@depenwisch.de
##### Sven Tewes
* sven_tewes@gmx.de
##### Christian Schmidt
* christian.schmidt@fh-muenster.de