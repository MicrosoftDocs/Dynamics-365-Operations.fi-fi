---
title: Tarkastele ja suunnittele talousraportteja
description: "Tässä artikkelissa on harjoituksia, joissa selitetään, miten tarkastellaan ja luodaan raportteja Microsoft Dynamics 365 for Finance and Operationsissa."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 10814
ms.assetid: cd5f6483-c09b-4c2d-9336-d22eb6ab6e4f
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 0dc453ab56a2d381afa6e22d847f0b1eb7a16e7e
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017


---

# <a name="view-and-design-financial-reports"></a>Tarkastele ja suunnittele talousraportteja

[!include[banner](../includes/banner.md)]


Tässä artikkelissa on harjoituksia, joissa selitetään, miten tarkastellaan ja luodaan raportteja Microsoft Dynamics 365 for Finance and Operationsissa. Talousraportointi koostuu Finance and Operationsissa tapahtuvasta tarkastelusta ja yhden napsautuksen raporttisuunnitteluohjelmasta, jolla voit luoda ja muokata raportteja.  

<a name="exercise-1-generate-and-explore-a-default-financial-report"></a>Tehtävä 1: Luo ja tutki taloushallinnon oletusraportteja
-----------------------------------------------------------

Tässä harjoituksessa luodaan ja tutustutaan nykyiseen oletusraporttiin. Tämä raportti sisältää kaikki tilit ja se sisältää myös tiliominaisuudet (määritteet) näille tileille. Perehdyt tapahtumatietoihin, käytät dimensiosuodattimia, muutat raportin valuutan. Ensinnäkin päivitämme dimensioiden näyttöjärjestyksen talousraportointia varten. Voit valita dimensioiden näyttämistavan, ei ainoastaan suunniteltaessa ja tilinpäätöksiä tarkasteltaessa.

1.  Siirry **Kirjanpitodimension malli sovelluksien integrointiin** kohdassa **Tilikarttojen dimensiot** kirjanpidossa.
2.  Siirrä dimensioita niin, että ne ovat seuraavassa järjestyksessä:
    1.  Päätili
    2.  Liiketoimintayksikkö
    3.  Kustannuspaikka
    4.  Osasto

    Huomautus: Muut dimensiot voivat olla nykyisessä järjestyksessä.
3.  Tallenna dimensio konfigurointi. Seuraavaksi on raportin luominen ja raportin tietojen tutkiminen.
4.  Siirry **Tilinpäätökset** kohdassa **Kyselyitä ja raportit** kirjanpidossa.
5.  Valitse raportille rivi nimeltään **Kirjanpidon tiedot: oletusarvo.**
6.  Valitse **Muokkaa.** Huomautus: Järjestelmä kehottaa lataamaan kerran klikattavan raportin suunnittelijan ja kirjautumaan sisään. Kirjaudu sisään tunnistetietojesi avulla.
7.  Muuta perusvuodeksi 2012 ja valitse **Luo**. Kun raportti luodaan raportin suunnittelijalla, kun se avautuu uudessa selaimen välilehdessä. Voit joko tutkia raporttia selaimen uudessa välilehdessä tai mennä alkuperäiseen selaimen välilehteen ja avata raportin siellä valitsemalla sen **Tilinpäätökset**-luettelosta.
8.  Valitse yksi summista perehtyäksesi raportin tilitietoihin avatussa raportissa.
9.  Kun olet tilitiedoissa, valitse tili, jossa on tietoja, ja **perehdy raporttiin tapahtumatasolla**. Raportin tapahtumatasolla näet ominaisuudet (määritteet), jotka sisältyvät raportin rakenteeseen. Tapahtumasta ja tilistä riippuen voit nähdä vähintään yhden määritteen.
10. Sulje raportin tapahtumataso.
11. Valitse sama tai eri tili ja **avaa tositetapahtumat.** Tositetapahtumat suodatetaan jakson, vuoden ja tilin + valitun tilin dimensioiden yhdistelmän mukaan. Tositetapahtumissa, voit tutustua tapahtuman muihin tietoihin.
12. Sulje tositetapahtumat. Taloushallinnon raportissa voit tarkastella tietoja joko eri jaksoilta ja vuodelta, tai eri ominaisuuksia ja dimensioita käyttäen. Tämä tehdään käyttämällä **Raporttiasetuksia**.
13. Valitse **Raporttivaihtoehto**.
14. Valitse **Lisää dimensiosuodatin** ja valitse **Liiketoimintayksikkö**.
15. Kirjoita 001 kenttään ja valitse **OK**. Raportissa näkyy nyt vain 001 liiketoimintayksikön tiedot. Tämä on raportin mukautettu näkymä eivätkä muut voi tarkastella sitä.
16. Sulje suodatettu raportti. Raportit voidaan näyttää millä tahansa Finance and Operationsiin lisättynä valuuttana.
17. Valitse **Valuutta**, sitten valitse **EUR.** Raportti näkyy nyt euroina. Kaikki valuuttakoodit tai symbolit, jotka sisältyvät raportin rakenteeseen, näkyvät nyt sovelettuna valuuttana. Jos valuutalle ei ole määritetty valuuttatunnusta, valuuttasymbolia ei näytetä.
18. Sulje **Kirjanpidon tiedot** -raportti.
19. Sulje **Raportin suunnittelija**.

## <a name="exercise-2-add-additional-account-properties-to-a-report-design"></a>Harjoitus 2: Lisää muita tiliominaisuuksia raportin rakenteeseen
Tässä harjoituksessa muokataan nykyistä oletusraporttia. Päivität sekä rivimäärityksen sisältämään kaikki tilit, että sarakemäärityksen sisältämään tilin määritteet. Kun päivitykset ovat valmiit, luot juuri valmistuneen raportin ja tutkit raporttia. Aloitammme tilinpäätöksien luettelosta.

1.  Siirry **tilinpäätöksiin** "Kyselyt ja raportit" -kohdassa kirjanpidossa.
2.  Valitse raportille rivi nimeltään **Koetaseen yhteenveto: oletusarvo**
3.  Valitse **Muokkaa**. **Koetaseen yhteenveto – oletusarvo** avautuu raportin suunnittelussa.
4.  Valitse **Tiedosto**, sitten **Tallenna nimellä** ja anna raportille nimeksi "Saldoraportti ominaisuuksilla". Huomautus: Aina kun uusi raportti luodaan raportin suunnittelutoiminnossa, raporttiluettelo päivittyy Finance and Operationsissa.
5.  Valitse rivinmääritys kuvake oletusraportista, avataksesi **Pääkirja – oletusrivin määritys**.
6.  Tallenna rivimääritys nimellä **Saldoraportti ominaisuuksilla**
7.  Laita kohdistin riville 50, valitse **Muokkaa**, sitten **Lisää rivejä dimensioista**. "Lisää rivejä dimensioista" sallii sinun valita valita mitkä dimensiot haluat rivimääritykseesi. Tässä tapauksessa rakennamme rivimäärityksen päätilin avulla.
8.  Varmista, että **päätili** sisältää kaikki et-merkit (&) ja valitse **OK**. Rivimääritys sisältää nyt kaikki yrityksen (USMF) päätilit.
9.  Siirry alas riville 11110 ja poista rivin 11110.
10. Valitse rivin 11080 **---(alaviivasummat)**.
11. Kirjoita riville 11140 **Kaikkien tilien summa** sarakkeeseen B.
12. Sarakkeessa C, valitse **TOT** avattavasta luettelosta.
13. Kirjoita **50:11080** sarakkeeseen D.
14. **Tallenna** rivimääritys. Rivimääritys sisältää nyt kaikki tilit sekä "Yhteensä"-rivin, joille voidaan lisätä kaikkien tilien summa. Seuraavaksi päivitämme sarakemäärityksen sisällyttämään muita tilin määritteitä.
15. **Saldoraportti ominaisuuksilla** -raportin määrityksessä, valitse sarakkeen määrityskuvake avataksesi **Pääkirjan yhteenveto – oletusarvo** sarakemäärityksen.
16. Tallenna sarakemääritys nimellä **Saldoraportti ominaisuuksilla**. Sarakemääritys sisältää kirjanpitotietojen sarakkeet, kuvaussarakkeen ja laskentasarakkeet. Lisäämme määritesarakkeita sarakemääritykseen säätääksemme tilejä koskevia tarkempia lisätietoja.
17. Seuraavat määritteet lisätään sarakemääritykseen:
    -   Kirjauskansion numero:
    -   Kirjauskansion kuvaus
    -   Tapahtumapäivä
    -   Luonut
    -   Viimeksi muokannut

18. Sarakkeessa I, valitse **ATTR** saraketyypiksi. Sitten, valitse **Kirjauskansionumero** määriteluokaksi.
19. Jatka sarakkeiden lisäämistä jäljellä oleviin määritteisiin.
20. **Otsikko 2** -rivillä, lisää kuvaus jokaiselle uudelle sarakkeelle, jotka on lisätty.
21. Tallenna sarakemääritys. Nyt kun rivimääritys ja sarakemääritys on päivitetty, ne on lisättävä raporttimääritykseen.
22. **Saldoraportti ominaisuuksilla** -raportin määrityksessä, valitse "Saldoraportti ominaisuuksilla" sekä rivimääritykselle, että sarakemääritykselle.
23. Muuta perusvuodeksi **2012.**
24. **Tallenna** raporttimääritys ja **luo**. Kun raportti on valmis ja avautuu, voit tutkia raporttia samoin kuin ensimmäisessä harjoituksessa. Perehdy eri tileihin tarkastellaksesi, kuinka muut määritteet ovat näkyvillä.
25. Sulje **Saldoraportti ominaisuuksilla**-raportti.
26. Sulje **Raportin suunnittelija**.

## <a name="exercise-3-create-a-multidimensional-report-using-a-reporting-tree"></a>Harjoitus 3: Luo moniulotteinen raportti käyttämällä raportointipuuta
Tässä harjoituksessa muokkaat nykyistä oletusraporttia. Tulet luomaan raportointipuun ja lisäämään raporttimääritykseen tuottaaksesi kustannuspaikka / jaetun tuloslaskelman. Kun päivitykset ovat valmiita, tulet luomaan kustannuspaikka / jaetun tuloslaskelman ja tutkimaan raporttia käyttämällä raportointipuuta. Aloitammme tilinpäätöksien luettelosta.

1.  Siirry **tilinpäätöksiin** "Kyselyt ja raportit" -kohdassa kirjanpidossa.
2.  Valitse raportille rivi nimeltään **Tuloslaskelma: oletusarvo**
3.  Valitse **Muokkaa**. **Tuloslaskelma – oletusarvo** avautuu raportin suunnittelussa.
4.  **Tiedosto** -valikossa, osoita **Uusi** ja klikkaa sitten **Raportointipuun määritys**
5.  **Muokkaa** -valikossa, klikkaa **Lisää raportointiyksiköitä dimensioista**...
6.  Poista kaikkien dimensioiden valintaruutujen valinnat lukuun ottamatta **kustannuspaikkaa**.
7.  Valitse **Dimensio**-kenttä kustannuspaikan dimensiolle, kirjoita kenttään **007** ja paina sarkainta. **Dimensioon**-kentässä, kirjoita **018**.
8.  **Tallenna** tulospuu nimellä **Kustannuspaikat yksikön mukaan.** Nyt kun raportointipuu on luotu, muokkaat raportointipuuta sisältämään kolme uutta koonti yksikköä: markkinointi, toiminnot ja vähittäismyynti.
9.  **Ikkuna**-valikossa, klikkaa **Kustannuspaikat jaon mukaan**. (Jos raportointipuu on suljettu, valitse se raportointipuun määrityksistä siirtymisruudussa.)
10. Klikkaa yksikköä numero kaksi **Messut** ja klikkaa **Lisää raportoinnin yksikkö** -kuvaketta.
11. Kaksoisnapsauta uuden rivin yksikkö-saraketta ja valitse **USMF**.
12. Kirjoita **Markkinointi** sarakkeisiin B ja C.
13. Napsauta yksikköä numero viisi **Palvelutoiminnot** ja napsauta hiiren kakkospainikkeella. **Valitse Lisää raportoinnin yksikkö**.
14. Toista vaihe 11.
15. Kirjoita **Toiminnot** sarakkeisiin B ja C.
16. Napsauta numeroa 12 **Myyntipiste** ja napsauta hiiren kakkospainikkeella. Valitse **Lisää raportoinnin yksikkö**.
17. Toista vaihe 11.
18. Kirjoita **Vähittäismyynti** sarakkeisiin B ja C. Huomaa, että markkinoinnin, toimintojen ja vähittäismyynnin yksiköt näkyvät samalla tasolla, kuin nykyiset vyörytysyksiköt. Seuraavaksi järjestetään uudet yksiköt. Raportoinnin yksiköt on järjestetty kakkospainikkeen vaihtoehdoilla: edistämällä ja alentamalla, tai vetämällä ja pudottamalla.
19. Tarkista yksikkö kolme **Messut** on aktiivinen ja napsauta hiiren kakkospainikkeella.
20. Valitse **Alenna raportoinnin yksikkö**. Pane merkille, että yksikkö näkyy nyt **markkinoinnin** lapsiobjektina.
21. Klikkaa yksikköä neljä **Markkinointi** **Kampanja** ja napsauta hiiren kakkospainikkeella.
22. Valitse **Alenna raportoinnin yksikkö**.
23. Valitse **Palvelutoiminnot** graafisessa esityksessä. Pidä vasenta hiiripainiketta alhaalla ja vedä yksikön ylös **työvaiheisiin**. Vapauta vasen hiiri pudottamalla yksikkö toimintojen vyöryttämiseen. Toista **tuotannolle, laadunvalvonnalle, logistiikalle, hankinnalle ja hallinnalle**.
24. Tee **Lähtö**, **Super**, **Marketti** ja **Online** aliluokkia **Vähittäismyynti** joko alentamalla ne alemmalle tasolle tai vetämällä ja pudottamalla.
25. Tallenna tuloksena uudelleen organisaatio. Nyt kun raportointipuu on luotu ja järjestelty, se voidaan lisätä raportin määritykseen.
26. Valitse **Window** -valikosta **Tuloslaskelma – oletusarvo** avataksesi raportin määrityksen.
27. Valitse **Puutyyppi** -avattavan luettelon nuolta ja valitse **Raportointi puu**.
28. Klikkaa puun avattavan luettelon nuolta ja valitse **Kustannuspaikat yksikön mukaan**.
29. Vaihda perusvuodeksi **2012**, **tallenna** muutokset ja **luo** raportti. Kun raportti on luotu ja avautuu, voit tutkia raporttia.
30. Valitse **Raportointipuun** avattava valikko tarkastellaksesi raportointiyksiköitä. Vaihtoehtoisesti voit perehtyä raportin sarakkeeseen nähdäksesi kaikki saldot kaikille yksiköille raportointipuussa.
31. Sulje **Tuloslaskelma - oletus**.
32. Sulje **Raportin suunnittelija**.

## <a name="exercise-4-create-a-consolidated-report-using-an-organization-hierarchy"></a>Harjoitus 4: Luo konsolidoitu raportti käyttämällä organisaatiohierarkiaa
Tässä harjoituksessa muokkaat nykyistä oletusraporttia. Tulet lisäämään organisaatiohierarkian raporttimääritykseen tuottaaksesi konsolidoidun tuloslaskelman ja taseen. Kun päivitykset ovat valmiita, tulet luomaan konsolidoidun raportin ja tutkimaan raporttia käyttämällä raportointipuuta. Aloitammme tilinpäätöksien luettelosta.

1.  Siirry **tilinpäätöksiin** "Kyselyt ja raportit" -kohdassa kirjanpidossa.
2.  Valitse raportin rivi nimeltään **Tase ja tuloslaskelma rinnakkain: oletusarvo**
3.  Valitse **Muokkaa**. **Tase ja tuloslaskelma rinnakkain: oletusarvo** aukaisee raportin suunnittelijan.
4.  Valitse **Tiedosto** &gt; **Tallenna nimellä** ja anna raportille nimeksi **Konsolidoitu tase ja tuloslaskelma rinnakkain**.
5.  Muuta perusvuodeksi 2012.
6.  Klikkaa puutyypin avattavaa nuolta ja valitse **Organisaatiohierarkiat**.
7.  Klikkaa puun avattavaa nuolta ja valitse **Contoso Holdings.**
8.  Tallenna muutokset ja luo raportti. Valitse tarvittaessa kaikki raportointiin yksiköt. Kun raportti on luotu ja avautuu, voit tutkia raporttia.
9.  Valitse **Raporttivaihtoehto**.
10. Valitse **Lisää dimensiosuodatin** ja valitse **Osasto**
11. Kirjoita **022** kenttään ja valitse **OK**.
12. Sulje suodatettu raportti.
13. Valitse Raportointipuu **e** avattava valikko tarkastellaksesi raportointiyksiköitä. Vaihtoehtoisesti voit perehtyä raportin sarakkeeseen nähdäksesi kaikki saldot kaikille yksiköille raportointipuussa.
14. Sulje **Konsolidoitu tase ja tuloslaskelma rinnakkain**.
15. Sulje **Raportin suunnittelija**.

## <a name="exercise-5-create-a-sidebyside-departmental-report"></a>Harjoitus 5: Luo rinnakkainen osastojen raportti
Tässä harjoituksessa luot uuden raportin. Raportti on rinnakkainen osastojen tuloslaskelmaan. Käytät aiemmin luotua rivimääritystä, mutta luo uusi raporttimääritys ja uusi sarakemääritys, joka käyttää dimensiosuodattimia. Aloitammme tilinpäätöksien luettelosta.

1.  Siirry **tilinpäätöksiin** "Kyselyt ja raportit" -kohdassa kirjanpidossa.
2.  Valitse **Uusi**. Raportin suunnittelija avautuu tyhjän raportin määrityksen kanssa. Ensimmäinen tehtäväsi on luoda sarakkeen määritys.
3.  Luo uusi sarakkeen määritys valitsemalla **Tiedosto**, sitten **Uusi** ja sen jälkeen **Sarakemääritys**.
4.  **Sarake A:ssa**, valitse **DESC** saraketyypiksi.
5.  **Sarakkeessa B**, valitse **FD** saraketyypiksi.
6.  Valitse kaksoisnapsauttamalla **Dimensiosuodatus**-kenttä.
7.  **Dimensio**-ikkunassa, kaksoisnapsauta **Osasto**-saraketta.
8.  Valintaikkunan yksittäisellä osalla tai alueosalla, valitse **ellipsi** **Mistä**-kenttään nähdäksesi osastoluettelon.
9.  Valitse osasto **022**, **Myynti ja Markkinointi** ja sitten klikkaa **OK**.
10. Toista vaiheet 5-8 osastoille 23-25.
11. **Otsikko 2** -rivissä, jokaiselle FD-sarakkeelle, kirjoita seuraavat osaston kuvaukset:
    -   Sarake B – Myynti ja markkinointi
    -   Sarake C – toiminnot
    -   Sarake D – Taloushallinto
    -   Sarake E – IT

12. Tallenna sarakkeen määritys rinnakkaisina osastoina. Koska käytämme aiemmin luotua rivimääritystä, raporttimääritys voidaan muokata nyt käyttämään on juuri luotua sarakemääritystä ja olemassa olevaa rivimääritystä.
13. Valitse **Window** -valikosta **Uusi raportin määritys** avataksesi raportin määrityksen.
14. Valitse **Tuloslaskelma – oletusarvo** rivimäärityksenä ja **Rinnakkaisosastot** sarakkeen määrityksenä.
15. Tallenna raportin määritys nimellä **Rinnakkainen osastojen tuloslaskelma**.
16. Muuta perusvuodeksi **2012**.
17. Muuta yksityiskohtatasoksi **Rahoitus, tili ja tapahtuma**.
18. **Tallenna** muutokset ja **luo**. Kun raportti on luotu ja avautuu, voit tutkia raporttia.

## <a name="additional-resources"></a>Lisäresurssit
[Talousraportointi](/dynamics365/unified-operations/financials/general-ledger/financial-reporting-getting-started)  
[Tarkastele tilinpäätöksiä](/dynamics365/unified-operations/financials/general-ledger/view-financial-reports) 
[Dynamicsin taloushallinnon raportoinnin blogi](http://blogs.msdn.com/b/dynamics_financial_reporting/)



