Webová aplikácia = Matrix Calc - rozšírenie

Autor: Patrik Pricl (login: xpricl00)



Aplikácia pracuje so vzorcami matíc,ktoré následne vypoèíta.

Práca s klavesnicou: 
D + "+" || "-" || "*" - pridanie operácie medzi maticami (operácia sa pridá za aktívnu maticu)

D + "šípky" - pohyb po bunkách aktívnej matici

D + M - pridanie novej matice za aktívnu maticu

D + Backspace - odstránenie operácie, ktorá nasleduje za aktívnou maticou

D + Del - odstránenie aktívnej matice spolu s operáciou, ktorá nasleduje za danou maticou 

Práca pomocou myši:
Kliknutím na maticu sa matica aktivuje a pomocou tlaèítkového panelu sa vykanavajú zmeny ([-] -> pridanie znamienka mínus do bunky; "-" , "+", "*" -> pridanie/zmena operacie medzi maticami)

Panel aktivnej matice - aktívna matica má po aktivácii viditelnı panel operácii,kde je moné modifikova jej velkos, "drop" maticu v textovej podobe (riadky sú oddelené znakom konca riadku a ståpce sú oddelené èiarkou), transponova maticu, kopirova maticu do clipboardu v textovej podobe (rovnaké ako pri "drop" matice ) alebo ju vymaza (spolu s operátorom, ktorı nasleduje po nej)

Spustenie aplikácie:

Frontend:

	
$npx create-react-app <nazov> 
pridanie súborov z prieèinku frontend do <nazov>
$cd frontend
$npm start

alebo

v prieèinku frontend zada príkaz cez príkazovı riadok:  $npx serve -s build 	


dependences:
"@testing-library/jest-dom": "^5.11.6",
"@testing-library/react": "^11.1.2",
"@testing-library/user-event": "^12.2.2",
"prop-types": "^15.7.2",
"react": "^17.0.1",
"react-dom": "^17.0.1",
"react-scripts": "4.0.0",
"web-vitals": "^0.2.4"

Backend:

Vygenerovanie súborov pre backend a inštalácia potrebnıch zavislostí:

$npx express-generator --view=pug <nazov> 
pridanie súborov z prieèinku backend do <nazov>
$cd backend
$npm install

Spustenie (spustenie backend-u na port 9000):
$npm start


"dependencies": {
  "cookie-parser": "~1.4.4",
  "cors": "^2.8.5",
  "debug": "~2.6.9",
  "express": "~4.16.1",
  "http-errors": "~1.6.3",
  "mathjs": "^9.4.2",
  "morgan": "~1.9.1",
  "pug": "^3.0.2"
}



Nedokonèené:
Zobrazenie chyby pri zadaní zlej velikosti matice v rámci operácie
Pri drope zlej formy matice dojde k pádu aplikácie (nie všetky riadky alebo všetky ståpce majú rovnakú velkos)
Pridanie komentu k vzorcu matíc
Ukladanie na lokálne úloisko
Vkladanie novej matice cez klavesnicu aj keï nie je iadna matica aktívna
Pri pohybe textového kurzoru v bunke matici pomocou šípok nedochádza k zmene polohy "carot" - nasledné zadávanie èísiel cez panel sa zadávajú na nezmenenú polohu "carot"

	