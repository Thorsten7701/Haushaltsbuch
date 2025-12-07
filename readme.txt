## Haushaltsbuch 
Household budget (see below for english version)
Cloudless. Anti bloat. Portable. Intuitive. Your data stays on your disk.

## LiveDemo: https://thorsten7701.github.io/Haushaltsbuch/Haushaltsbuch.html
play with it: dummy.json

Bei meiner Suche nach einer Haushaltsbuch App musste ich enttäuscht feststellen, dass keine meinen Anforderungen entsprach.
Teils waren sie mehrere hundert Megabyte groß und die meisten unterstützten keinen Datenexport, sondern nur eine proprietäre Speicherdatei. Ein paar packten die Daten gleich ganz in irgendeine anonyme Cloud.
Ich wollte diese Daten nicht unerreichbar irgendeinem Hersteller ausgeliefert sehen. Auch waren fast alle Produkte Closed Source, erlaubten also nicht die offene, gemeinschaftliche Weiterentwicklung des Programmcodes.

Als Lösung dafür startete ich "Haushaltsbuch". 

Entwicklungsziele dabei sind: 
	einfache Verständlichkeit,
	Internationalisierung (trans.js),
	Kompatibilität mit libreoffice & excel,
	Im- und Exportierbarkeit der Daten (CSV und json), 
	sehr gute Auswertungsfunktionen,  
	komplett lokaler Betrieb ohne Installation sowie
Offener, strukturierter und dokumentierter Quellcode.

Das war 2024 und mittlerweile hat das Projekt einen zufriedenstellenden Stand erreicht.
Dies ist also die erste öffentliche Version Beta45. Lizenz ist die freie GPLv3.

Haushaltsbuch.html kann auch von einem usb stick gestartet werden.

Enjoy!
Thorsten

![Data Visualisation](https://github.com/Thorsten7701/Haushaltsbuch/blob/home/screenshots/3pie_chart.PNG)

Wenn euch die App gefällt, überlegt euch doch mir ein schönes Foto mit einem Spruch von euch zu schicken. Später wird es dafür einen Instagram oä account für das tool geben.
vielen Dank!  arjunae@nurfuerspam.de  



----------------------
## Household budget
---------------------

In my search for a household budget app, I was disappointed to find that none met my requirements.
Most didn't support data export, only a proprietary save file; some were several hundred megabytes large.
A few stored the data entirely in some anonymous cloud. All of these were exclusion criteria,
because who wants to be at the mercy of some manufacturer. Also, almost all products were closed source,
thus not allowing open, collaborative development of the program code.

So I started "Haushaltsbuch". The development goals are:
 Open, documented source code, 
 easy to understand,
 internationalization (trans.js), 
 compatibility with LibreOffice & Excel, 
 import and exportability of data (CSV and JSON), 
 good analysis functions, 
and complete local operation without installation.

That was in 2024, and in the meantime, the project has reached a satisfactory state. This is therefore the first public version, Beta45. The license is the free GPLv3.
The entire logic is implemented in JavaScript.
Haushaltsbuch.html can also be run from a USB stick.

Enjoy! Thorsten

If you like the app, please consider sending me a nice photo with a quote from you.
Later, there will be an Instagram or similar account for the tool. Thank you! arjunae@nurfuerspam.de


-----------
## Tech
----------


The JavaScript logic is organized into the following modules:

DOM: Holds references to all important elements and some helper functions
Store: States (transaction data, rules) It uses a publish-subscribe logik.
MainController: Controls page visibility.	
ImportModule: CSV and JSON file imports. 
CategorizeModule: The main data table and the rule creation UI.	
VisualizeModule: Al charts and detailed tables on the visualization page.
Internationalization: Translations and Currency settings support via trans.js ( data-i18n attr).
IconLoader.js: A lightweight, zero-dependency solution for rendering eg FontAwesome SVG icons locally. 

Most functions are JSDoc annotated.

Libraries:

Tailwind CSS:  CSS framework
Tabulator.js:  data grids
Chart.js: pie charts and line charts
PapaParse.js: parse CSV files
Font Awesome: UI icons
