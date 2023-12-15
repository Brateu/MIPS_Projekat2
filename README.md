Koristi se mikrokontroler STM32F013C6TX LQFP48
Niz sa epruvetama je sledeci : Epruvete = {S,T,E,F,A,N,E,R,I,Ć}, redni broj slova u azbuci modul 5 => {1, 2, 2, 0, 1, 1, 2, 0, 0, 3}
Zeljena temperatura = Broj_Slova * 5 = 50
Tajmer je namesten da generise prekid na svaki minut pomocu podesavanja prescaler-a i frekvnecije clock-a da ne opterecujemo mikrokontroler u pretpostavci da za minut temperatura ne moze drasticno da se promeni.
Motor 1  i motor 2 su step motori i imaju opciju da se vrte u oba smera pa tako postavljamo pinove i koristimo u koju stranu cemo rotirati.
Motori su X5718-077-20-Y05-A0-A12F i velicine prema NEMA su 24. Imaju obrtni moment od 15 N/M sto ce biti dovoljno za ove uslove.
Senzor je MCP9700 koji radi od 2,2 do 5,5 volti ali na vecim naponima daje preciznija merenja zato je stavljen na vise.
Takodje imamo 2 drajvera pomocu kojih upravljamo motorima i to je Closed Loop Stepper Driver CL57T kod kojih inputi rade na 5 volti pa moramo pojacati signal iz mikrokontrolera.
Eksterni takt je 16MHZ Murata CSTCE16M0V53-R0:
