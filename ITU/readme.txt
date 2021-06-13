Webov� aplik�cia = Matrix Calc - roz��renie

Autor: Patrik Pricl (login: xpricl00)



Aplik�cia pracuje so vzorcami mat�c,ktor� n�sledne vypo��ta.

Pr�ca s klavesnicou: 
D + "+" || "-" || "*" - pridanie oper�cie medzi maticami (oper�cia sa prid� za akt�vnu maticu)

D + "��pky" - pohyb po bunk�ch akt�vnej matici

D + M - pridanie novej matice za akt�vnu maticu

D + Backspace - odstr�nenie oper�cie, ktor� nasleduje za akt�vnou maticou

D + Del - odstr�nenie akt�vnej matice spolu s oper�ciou, ktor� nasleduje za danou maticou 

Pr�ca pomocou my�i:
Kliknut�m na maticu sa matica aktivuje a pomocou tla��tkov�ho panelu sa vykanavaj� zmeny ([-] -> pridanie znamienka m�nus do bunky; "-" , "+", "*" -> pridanie/zmena operacie medzi maticami)

Panel aktivnej matice - akt�vna matica m� po aktiv�cii viditeln� panel oper�cii,kde je mo�n� modifikova� jej velkos�, "drop" maticu v textovej podobe (riadky s� oddelen� znakom konca riadku a st�pce s� oddelen� �iarkou), transponova� maticu, kopirova� maticu do clipboardu v textovej podobe (rovnak� ako pri "drop" matice ) alebo ju vymaza� (spolu s oper�torom, ktor� nasleduje po nej)

Spustenie aplik�cie:

Frontend:

	
$npx create-react-app <nazov> 
pridanie s�borov z prie�inku frontend do <nazov>
$cd frontend
$npm start

alebo

v prie�inku frontend zada� pr�kaz cez pr�kazov� riadok:  $npx serve -s build 	


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

Vygenerovanie s�borov pre backend a in�tal�cia potrebn�ch zavislost�:

$npx express-generator --view=pug <nazov> 
pridanie s�borov z prie�inku backend do <nazov>
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



Nedokon�en�:
Zobrazenie chyby pri zadan� zlej velikosti matice v r�mci oper�cie
Pri drope zlej formy matice dojde k p�du aplik�cie (nie v�etky riadky alebo v�etky st�pce maj� rovnak� velkos�)
Pridanie komentu k vzorcu mat�c
Ukladanie na lok�lne �lo�isko
Vkladanie novej matice cez klavesnicu aj ke� nie je �iadna matica akt�vna
Pri pohybe textov�ho kurzoru v bunke matici pomocou ��pok nedoch�dza k zmene polohy "carot" - nasledn� zad�vanie ��siel cez panel sa zad�vaj� na nezmenen� polohu "carot"

	