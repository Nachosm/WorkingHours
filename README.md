# WorkingHours



Projekt futtatása Eclipse-ben
1. Git
Először is szükségünk lesz az alkalmazás kódjára, amit a GitHub repository-ból tölthetünk le. 
Ezt a WorkingHours repository-ból érhető el. (Clone or download -> letöltési link)

2. Drive
Hozzunk létre egy "dev" mappát, majd ebben egy "sources" és egy "workspaces" mappát.
A Workspaces mappába hozzuk létre a WorkingHours mappát.
Indítsuk el az Eclips-t, majd válasszuk ki ezt a mappát workspace-nek.

3. Eclipse
Indulás után navigáljuk a Window/Perspectives/Open Perspective/Others menübe.
A listában válasszuk a ’Git’ perspektívát.
A bal oldalon megjelenő új alrészben van egy ’Clone a Git Repository’ feliratú link. 
Kattintsunk rá. 
Most kell megadnunk a GitHub-ról előzetesen megszerzett Repository linket,
Nyomjunk kétszer a Next gombra, amíg el nem jutunk a letöltési hely kiválasztásához, ezt mindenképp változtassuk meg és irányítsuk az általunk létrehozot „sources” könyvtárra.
Ha minden jól ment, van egy új repository-nk az Eclipse-ben.

Navigáljuk a Window/Perspectives/Open Perspective/Others menübe.
A listában válasszuk a ’Java’ perspektívát.
Utána a Window/Show view/Others-ben keressük meg a Server fület, és adjuk hozzá.

4. Tomcat
Most adjuk hozzá a Tomcat szervert. Server tab, klikk a linkre, válasszuk ki az Apache/Tomcat 9.0 szervert majd adjuk meg az Apache Tomcat telepítési könyvtárát (<drive>:\apps\apache-tomcat-9.0.12), és állítsuk át a használt JRE-t a telepítettre. (jdk1.8.0_xx)
Miután hozzáadtuk a szervert, a Package Explorer-ben egy jobb klikkel nyissuk meg a context menüt, és válasszuk az Import projects, azon belül az existing Maven repository-t:
Válasszuk ki a sources könyvtárban lévő WorkingHours mappát.
Most nyomjuk jobb klikket a Tomcat-en a Server fülön, majd válasszuk ki az ’Add and Remove’ menüpontot. 
A pop-up-ban válasszuk ki a ’days-of-calendar’ projektet és adjuk hozzá a szerverhez. 
Ha ez sikeres volt, a Server fülön a Tomcat alatt a nyilat lenyitva látnunk kell a saját WorkingHours projektünket.

Eclipse-be, jobb klikk a Tomcat server-en, publish. 
Várjuk meg, míg lefut a folyamat. 
Nyomjunk egy jobb klikk, Start-ot. 
Ha minden jól ment, nem lesz benne exception. 
Kis szerencsével nincs is, ekkor fut a Tomcat. 
Chrome-ban nyissuk meg az alábbi linket:
http://localhost:8080/days-off-calendar/
Az alkalmazás futásra kész, remélhetőleg. :ˇ)
