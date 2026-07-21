# Arenduse töövoog ja kvaliteedireeglid

See fail kirjeldab, kuidas projekti turvaliselt ja kvaliteetselt arendada. Siia ei kuulu mängu sisulised reeglid ega uute funktsioonide nõuded.

## 1. Enne töö alustamist

- Loe kasutaja soov tervikuna läbi ja sõnasta konkreetne oodatud tulemus.
- Enne iga uue muudatuse alustamist peab olema olemas vastav GitHubi probleemikirje.
- Enne koodi, konfiguratsiooni või dokumentatsiooni muutmist kuva kasutajale selle GitHubi issue otselink.
- Issue lingi juures esita lühidalt issue vastuvõtukriteeriumid ja kirjelda, mida agent nende põhjal tegema hakkab.
- Oota kasutaja kinnitust, et issue kirjeldus ja vastuvõtukriteeriumid on õigesti mõistetud; enne kinnitust ära muuda faile ega avalda midagi.
- Kui sobivat issue’t ei ole, peatu ja palu kasutajal kinnitada uue issue loomine või anda olemasoleva issue number.
- Vaata enne muutmist üle asjakohane olemasolev kood.
- Kontrolli, kas töökataloogis on kasutaja pooleliolevaid muudatusi, ja säilita need.
- Ära muuda ülesandega mitteseotud funktsioone, kujundust ega teksti.
- Kui nõue on ebaselge, eelista väikest ja tagasipööratavat muudatust.

## 2. Muudatuste tegemine

- Tee võimalikult väike muudatus, mis lahendab probleemi täielikult.
- Väldi sama loogika kopeerimist mitmesse kohta; kasuta selgelt nimetatud abifunktsioone.
- Hoia olemasolev koodistiil, keel ja visuaalne kujundus ühtlane.
- Ära lisa sõltuvusi, kui sama tulemus on mõistlikult saavutatav olemasolevate vahenditega.
- Säilita tagasiühilduvus nii arvuti- kui ka mobiilivaatega.
- Ära peida vigu tühjade `catch`-plokkide või vaikivate varulahendustega.
- Kasutajale kuvatavad veateated peavad olema lühikesed, arusaadavad ja eestikeelsed.

## 3. Kasutajaliidese kvaliteet

- Kõik olulised toimingud peavad töötama hiire, klaviatuuri ja puuteekraaniga.
- Interaktiivsetel elementidel peab olema selge vajutatav olek ja piisavalt suur puuteala.
- Kasutaja peab alati nägema, mis olekus mäng on ja mida saab järgmisena teha.
- Ära kasuta ainult värvi info edastamiseks; lisa vajadusel kuju, tekst või ikoon.
- Väldi horisontaalset kerimist, kattuvaid elemente ja liiga väikest teksti.
- Animatsioon ei tohi blokeerida mängimist ega muuta juhtimist aeglaseks.
- Austa võimalusel süsteemi `prefers-reduced-motion` seadistust.

## 4. Kontroll pärast iga muudatust

Kontrolli vähemalt:

1. Leht avaneb ilma JavaScripti vigadeta.
2. Muudetud funktsioon töötab tavakasutuse korral.
3. Vigane või ebatavaline sisend ei lõhu mängu.
4. Uus muudatus ei riku olemasolevaid põhifunktsioone.
5. Paigutus töötab kitsas telefonivaates ja laias arvutivaates.
6. Nupud ja muud juhtnupud on klaviatuuri ning puutega kasutatavad.
7. Tekstid, loendurid ja olekud uuenevad õigel ajal.

Kui automaatteste ei ole, tee sihitud käsitsi kontroll ja kirjelda lõppvastuses, mida kontrolliti.

## 5. Regressioonide vältimine

- Paranduse korral tuvasta kõigepealt vea põhjus, mitte ainult nähtav sümptom.
- Kontrolli parandusega seotud eelmist ja järgmist kasutaja tegevust.
- Testi piirjuhtumeid: esimene käik, viimane käik, korduv vajutus, uus mäng ja mängu lõpp.
- Ära kustuta töötavat käitumist selleks, et uut funktsiooni lihtsamalt lisada.
- Kui muudatus puudutab jagatud olekut, kontrolli kõiki kohti, kus seda olekut loetakse või muudetakse.

## 6. Jõudlus ja töökindlus

- Väldi tarbetut kogu mängulaua või lehe korduvat ümberjoonistamist.
- Ära jäta vanu taimereid, sündmusekuulajaid ega animatsioonielemente pärast uut mängu alles.
- Hoia animatsioonid sujuvad ja eelista CSS-i transformatsioone ning läbipaistvust.
- Väldi lõputuid tsükleid ja kontrollimatut DOM-elementide lisamist.
- Ära salvesta ega avalda paroole, võtmeid, isikuandmeid või muid tundlikke väärtusi.

## 7. GitHubi töövoog

- Ära avalda muudatusi enne, kui kohalik versioon on kontrollitud.
- Commit peab sisaldama ainult ühe loogilise muudatuse jaoks vajalikke faile.
- Kasuta lühikest ja täpset commit-sõnumit, mis kirjeldab tulemust.
- Commit-sõnumi esimene rida peab alati lõppema vastava issue numbriga, näiteks `Paranda mobiilne paigutamine #1`.
- Kui commit lahendab issue, peab sõnumi viimasel real olema GitHubi sulgemiskäsk kujul `Closes #1`.
- Kui üks commit sulgeb mitu issue’t, lisa iga sulgemiskäsk eraldi reale, näiteks `Closes #1` ja `Closes #2`.
- Commit-sõnumi vorm:

  ```text
  Lühike muudatuse kirjeldus #1

  Vajadusel täpsem selgitus.

  Closes #1
  ```

- Ära kirjuta üle kasutaja või teiste arendajate mitteseotud muudatusi.
- Pärast avaldamist kontrolli, et GitHubis on õige failiversioon.
- GitHub Pagesi kasutamisel arvesta, et avalik leht võib uueneda mõneminutilise viivitusega.

## 8. Issue’de käsitlemine

- Üks issue peab kirjeldama ühte probleemi või funktsioonisoovi.
- Pealkiri peab kirjeldama nähtavat probleemi või soovitud tulemust.
- Kirjelduses erista tegelik käitumine ja oodatud käitumine.
- Ära lisa samasse issue’sse eraldiseisvat funktsioonisoovi.
- Sulge issue alles pärast paranduse avaldamist ja kontrollimist.
- Vajadusel lisa issue’sse lühike märkus paranduse või kontrolli kohta.

## 9. Töö lõpetamise kriteeriumid

Ülesanne on valmis ainult siis, kui:

- kasutaja soovitud tulemus on täielikult rakendatud;
- muudatus on kontrollitud sobivates vaadetes ja kasutusviisides;
- teadaolevaid JavaScripti või paigutusvigu ei ole;
- mitteseotud käitumine on säilinud;
- dokumentatsioon või issue on vajadusel uuendatud;
- kasutajale on selgelt öeldud, mida muudeti, mida kontrolliti ja kas muudatus avaldati.
