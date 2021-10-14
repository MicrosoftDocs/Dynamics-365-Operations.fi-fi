---
title: Yksikön tietojen näyttäminen ja päivittäminen Excelissä
description: Tässä aiheessa käsitellään yksikkötietojen avaamista Microsoft Excelissä sekä tietojen näyttämistä, päivittämistä ja muokkaamista Microsoft Dynamicsin Excel-apuohjelmalla.
author: jasongre
ms.date: 10/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1902e80313c5460ac38896bc2f46d83897e3a58
ms.sourcegitcommit: 49f29aaa553eb105ddd5d9b42529f15b8e64007e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2021
ms.locfileid: "7592662"
---
# <a name="view-and-update-entity-data-with-excel"></a>Yksikön tietojen näyttäminen ja päivittäminen Excelissä 

[!include [applies to](../includes/applies-to-commerce-finance-scm.md)]

[!include [banner](../includes/banner.md)]


Tässä aiheessa käsitellään yksikkötietojen avaamista Microsoft Excelissä sekä tietojen näyttämistä, päivittämistä ja muokkaamista Microsoft Dynamicsin Excel-apuohjelmalla. Voit aloittaa yksikkötietojen avaamisen joko Excelissä tai Finance and Operations -sovelluksissa.

Kun avaat yksikkötietoja Excelissä, voit tarkastella ja muokata nopeasti tietoja Excel-lisäosalla. Apuohjelman käyttö edellyttää vähintään versiota Microsoft Excel 2016.

> [!NOTE]
> Jos Microsoft Azure Active Directory (Azure AD) -vuokraaja on määritetty käyttämään Active Directory Federation Servicesiä (AD FS), varmista, että Officen toukokuun 2016 päivitys on asennettu, jotta Excel-lisäosa pystyy kirjaamaan sinut sisään.

Lisätietoja Excel-apuohjelman käyttämisestä lyhyessä videossa [Excel-mallin luominen otsikolle ja rivimalleille](https://youtu.be/RTicLb-6dbI).

## <a name="open-entity-data-in-excel-when-you-start-from-a-finance-and-operations-app"></a>Yksikön tietojen avaaminen Excelissä Finance and Operations -sovelluksesta aloitettaessa
1. Valitse Finance and Operations -sovelluksen sivulla **Avaa kohteessa Microsoft Office**.

    Jos sivun juuritietolähde (taulukko) on sama kuin minkä tahansa yksikön juuritietolähde, sivulle muodostetaan oletusasetuksena **Avaa Excelissä**. **Avaa Excelissä** -vaihtoehto löytyy usein käytetyillä sivuilla, kuten **Kaikki toimittajat** ja **Kaikki asiakkaat**.
 
2. Valitse **Avaa Excelissä** -vaihtoehto ja avaa luotu työkirja. Tämä työkirja sisältää yksikön sidostiedot, osoitin ympäristöön ja osoitin Excel-lisäosaan.
3. Valitse Excelin **Ota muokkaus käyttöön** -painike, jotta voit ajaa Excel-lisäosan. Excel-lisäosa toimii Excel-ikkunan oikealla puolella olevassa ruudussa.
4. Jos käytät Excel-lisäosaa ensimmäistä kertaa, valitse **Luota tähän lisäosaan**.
5. Jos näet kirjautumisruudun, valitse **Kirjaudu sisään** ja kirjaudu sitten sisään samoilla tunnuksilla, joilla kirjaudut Finance and Operations -sovellukseen. Excel-apuohjelma käyttää aiempaa sisäänkirjautumista selaimesta ja kirjaa sinut sisään automaattisesti, jos se on mahdollista. (Käyttöjärjestelmäkohtaisia lisätietoja käytetystä selaimesta on kohdassa [Office-apuohjelmien käyttämät selaimet](/office/dev/add-ins/concepts/browsers-used-by-office-web-add-ins.) Kirjautumisen onnistumisen voi varmistaa tarkistamalla, mikä nimi on Excel-apuohjelman oikeassa yläkulmassa. 

Excel-lisä lukee valitsemasi yksikön tiedot automaattisesti. Huomaa, että työkirjassa ei ole tietoja ennen kuin Excel-lisäosa on lukenut tiedot.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Avaa yksikön tiedot Excelissä käynnistämisen yhteydessä
1. Avaa Office-kauppa valitsemalla **Myymälä**-painike Excelin **Lisää**-välilehden **Lisäosat**-ryhmässä.
2. Etsi Office-kaupasta avainsanalla **Dynamics** ja valitse **Lisää** **Microsoft Dynamics Office -lisäosa** -kohdan vieressä (Excel-lisäosa).
3. Jos käytät Excel-lisäosaa ensimmäistä kertaa, valitse **Luota tähän lisäosaan** voidaksesi käyttää sitä. Excel-lisäosa toimii Excel-ikkunan oikealla puolella olevassa ruudussa.
4. Avaa **Asetukset**-ruutu valitsemalla **Lisää palvelimen tiedot** -painike.
5. Kopioi kohteena olevan Finance and Operations -sovellusesiintymän URL-osoite selaimessa, liitä se **Palvelimen URL-osoite** -kenttään ja poista kaikki teksti isäntänimen jälkeen. URL-osoitteessa tulisi olla vain isäntänimi.

    Jos URL-osoite on esimerkiksi `https://xxx.dynamics.com/?cmp=usmf&amp;mi=CustTableListPage`, poista kaikki kaikki muut tiedot paitsi `https://xxx.dynamics.com`.

6. Valitse **OK** ja vahvista muutos valitsemalla **Kyllä**. Excel-lisäosa käynnistetään uudelleen. Se lataa metatiedot.

    **Rakenne**-painike on nyt käytettävissä. Jos Excel-lisäosassa on **Lataa sovelmat** -linkki, et ole todennäköisesti kirjautunut oikeana käyttäjänä. Lisätietoja tämän ongelman ratkaisemisesta on kohdan [Sovelmien lataaminen](../office-integration/office-integration-troubleshooting.md#issue-the-excel-add-in-loads-but-instead-of-showing-data-it-displays-load-applets-in-the-task-pane) vianmääritysosassa.

7. Valitse **Rakenne**. Excel-lisäosa hakee yksikön metatiedot.
8. Valitse **Lisää taulu**. Näkyviin tulee luettelo yksiköistä. Yksiköt näytetään muodossa "Nimi – Otsikko".
9. Valitse luettelosta yksikkö, kuten **Asiakas - Asiakkaat**. Valitse sitten **Seuraava**.
10. Jos haluat lisätä kentän **Käytettävissä olevat kentät** -luettelosta **Valitut kentät** -luetteloon, valitse kenttä ja valitse sitten **Lisää**. Vaihtoehtoisesti voit kaksoisnapsauttaa **Käytettävissä olevat kentät** -luettelon kenttää.
11. Kun olet lisännyt haluamasi kentät **Valitut kentät** -luetteloon, varmista, että kohdistin on oikeassa kohdassa taulukkoa (esimerkiksi solu A1) ja valitse sitten **Valmis**. Valitse sitten **Valmis** ja sulje suunnitteluohjelma.
12. Valitse **Päivitä** ja hae tietojoukko.

## <a name="view-and-update-entity-data-in-excel"></a>Näytä ja päivitä yksikön tiedot Excelissä
Kun Excel-lisäosa lukee yksikön tiedot työkirjaan, voit päivittää tiedot milloin tahansa valitsemalla Excel-lisäosassa **Päivitä**.

## <a name="edit-entity-data-in-excel"></a>Muokkaa yksikön tietoja Excelissä
Voit muuttaa yksikön tietoja tarpeen mukaan ja julkaista muutokset takaisin Finance and Operations -sovelluksiin valitsemalla Excel-apuohjelmassa **Julkaise**. Jos haluat muokata tietuetta, valitse työkirjassa solu ja muuta sitten solun arvoa. Jos haluat lisätä uuden tietueen, seuraa jotakin näistä vaiheista:

- Napsauta tietolähdetaulun jotakin kohtaa ja valitse sitten **Uusi** Excel-lisäosassa.
- Napsauta tietolähdetaulun viimeistä riviä ja paina sarkainpainiketta, kunnes kohdistin siirtyy pois rivin viimeisestä sarakkeesta ja luo uuden rivin.
- Napsauta tietolähdetaulun alapuolella olevaa riviä ja aloita tietojen syöttäminen soluun. Kun siirrät kohdistuksen pois solusta, taulu laajentuu uudelle riville.
- Valitse otsikkotietueiden kenttäsidoksia varten jotakin kentistä ja valitse sitten **Uusi** Excel-apuohjelmassa.

Huomaa, että uusi tietue luodaan vain, jos kaikki avain- ja pakolliset kentät on sidottu työkirjassa tai jos oletusarvot on täytetty suodatusehdon avulla.

Jos haluat poistaa tietueen, seuraa jotakin näistä vaiheista:

- Napsauta hiiren kakkospainikkeella poistettavan rivin numeroa työkirjan rivin vieressä ja valitse sitten **Poista**.
- Napsauta hiiren kakkospainikkeella poistettavan rivin numeroa ja valitse sitten **Poista** &gt; **Taulun rivit**.

Jos tietolähteitä on lisätty liittyvinä tietolähteinä, otsikko julkaistaan ennen rivejä. Jos muiden tietolähteiden välillä on riippuvaisuuksia, joudut ehkä vaihtamaan oletusjulkaisujärjestystä. Jos haluat muuttaa julkaisujärjestystä, valitse Excel-lisäosassa **Asetukset**-painike (ratassymboli) ja valitse sitten **Data Connector** -pikavälilehdessä **Määritä julkaisujärjestys**.

## <a name="add-or-remove-columns"></a>Lisää tai poista sarakkeita
Voit säätää työkirjaan automaattisesti lisättäviä sarakkeita suunnittelijasovelluksessa.

> [!NOTE]
> Jos **Rakenne**-painike ei näy Excel-lisäosan **Suodatin**-painikkeen alla, ota tietolähteen suunnitteluohjelma käyttöön. Valitse **Asetukset**-painike (ratassynboli) ja valitse sitten **Ota rakenne käyttöön** -valintaruutu.

1. Valitse Excel-lisäosassa **Rakenne**. Kaikki tietolähteet luetellaan.
2. Valitse tietolähteen vierestä **Muokkaa**-painike (kynäsymboli).
3. Muuta **Valitut kentät** -luettelon kenttäluetteloa haluamallasi tavalla seuraavasti:

    - Jos haluat lisätä kentän **Käytettävissä olevat kentät** -luettelosta **Valitut kentät** -luetteloon, valitse kenttä ja valitse sitten **Lisää**. Vaihtoehtoisesti voit kaksoisnapsauttaa **Käytettävissä olevat kentät** -luettelon kenttää.
    - Voit poistaa kentän **Valitut kentät** -luettelosta valitsemalla kentän ja valitsemalla sitten **Poista**. Vaihtoehtoisesti voit kaksoisnapsauttaa kenttää.
    - Jos haluat muuttaa kenttien järjestystä **Valitut kentät** -luettelossa, valitse kenttä ja valitse sitten **Ylös** tai **Alas**.

4. Ota käyttöön tietolähteeseen tehdyt muutokset valitsemalla **Päivitä**. Valitse sitten **Valmis** ja sulje suunnitteluohjelma.
5. Jos olet lisännyt kentän (sarakkeen), valitse **Päivitä**, niin ohjelma hakee päivitetyn tietojoukon.

## <a name="change-the-publish-batch-size"></a>Julkaisuerän koon muuttaminen
Kun käyttäjä julkaisee muutoksia tietotietueisiin Excel-apuohjelmalla, päivitykset lähetetään erissä. Julkaisuerän oletuskoko on 100 riviä. Versiossa 10.0.17 ja sitä uudemmissa versioissa **Julkaisuerän koon määrittämisen salliminen Excel-apuohjelmassa** -toiminto antaa joustavan tavan hallita julkaisuerän kokoa.

Järjestelmänvalvojat voivat määrittää koko järjestelmää koskevan julkaisuerän kokorajoituksen Avaa Excelissä -työkirjoissa. Määritys tehdään määrittämällä **Julkaisuerän raja** -kenttä **Office-sovelluksen parametrit** -sivun **Sovelluksen parametrit** -osassa.

Julkaisuerän koko voidaan muuttaa myös yksittäisessä työkirjassa Excel-apuohjelman avulla.

1. Avaa työkirja Excelissä.
2. Valitse **Asetukset**(ratas) -painike Excel-apuohjelman oikeassa yläkulmassa.
3. Määritä **Julkaisuerän koko** -kenttään sopiva arvo. Määritetyn arvon on oltava pienempi kuin koko järjestelmää koskeva julkaisuerän raja.
4. Valitse **OK**.
5. Tallenna työkirja. Jos työkirjaa ei tallenneta, kun apuohjelman asetuksia on muutettu, kyseiset muutokset eivät ole työkirjassa, kun se avataan uudelleen.

Excel-työkirjamallin tekijät voivat määrittää samalla tavoin mallien julkaisuerän koon, ennen kuin ne ladataan järjestelmään.

## <a name="copy-environment-data"></a>Kopioi ympäristön tiedot

Ympäristöstä työkirjaan luettavat tiedot voidaan kopioida toiseen ympäristöön. Et voi kuitenkaan muuttaa yhteyden URL-osoitetta noin vain, koska työkirjan tietovälimuisti jatkaa tietojen käsittelemistä aiemmin luotuina tietoina. Sen sijaan tietojen julkaisemisessa uuteen ympäristöön uusina tietoina on käytettävä Kopioi ympäristön tiedot -toimintoa.

1. Valitse **Asetukset**-painike (ratassymboli) ja valitse sitten **Data Connector** -pikavälilehden **Kopioi ympäristön tiedot**. 
2. Anna uuden ympäristön palvelimen URL-osoite. 
3. Vahvista muutokset valitsemalla **OK**. Vahvista toiminto valitsemalla **Kyllä**. Excel-lisäosa käynnistetään uudelleen. Se muodostaa yhteyden uuteen ympäristöön. Työkirjan aiemmin luotuja tietoja käsitellään uusina tietoina.

    Excel-lisäosan uudelleenkäynnistyksen jälkeen näkyviin tulee viestiruutu, jossa kerrotaan, että työkirja on ympäristön kopiointitilassa.

4. Voit kopioida tiedot uuteen ympäristöön uusina tietoina, kun valitset **Julkaise**. Voit peruuttaa ympäristön kopiointitoiminnon ja tarkistaa aiemmin luodut tiedot uudessa ympäristössä valitsemalla **Päivitä**.

## <a name="troubleshooting"></a>Vianmääritys
Tietyt ongelmat ovat ratkaistavissa muutaman helpon vaiheen kautta.

- **Lataa sovelmat -linkki näytetään** – Lisätietoja tämän ongelman ratkaisemisesta on kohdan [Sovelmien lataaminen](../office-integration/office-integration-troubleshooting.md#issue-the-excel-add-in-loads-but-instead-of-showing-data-it-displays-load-applets-in-the-task-pane) vianmääritysosassa. 
- **Näyttöön tulee Kielletty-virhesanoma** –Jos näyttöön tulee Kielletty-virhesanoma, kun Excel-lisäosa lataa metatietoja, Excel-lisäosaan kirjautuneella tilillä ei ole käyttöoikeutta kohteena olevaan palveluun, ilmentymään tai tietokantaan. Ratkaise ongelma varmistamalla, että Excel-lisäosan oikeassa yläkulmassa on oikea käyttäjänimi. Jos näkyvillä on väärä käyttäjänimi, valitse se. Kirjaudu sitten ulos ja kirjaudu takaisin sisään.
- **Excelin päällä näkyy tyhjä verkkosivu** – Jos kirjautumisen aikana avautuu tyhjä verkkosivu, tili vaatii AD FS:n käytön, mutta Excel-lisäosan suorittava Excel-versio ei ole tarpeeksi uusi eikä kirjautumisikkunaa voi ladata. Ratkaise ongelma päivittämällä käytössä oleva Excel-versio. Jos olet yritys, jolla on käytössä hidas päivityskanava, voit päivittää Excel-version käyttämällä [Office Deployment Tool -työkalua](/deployoffice/overview-office-deployment-tool) [vaihtaaksesi hitaan päivityskanavan nykyiseen päivityskanavaan](/deployoffice/overview-update-channels).
- **Aikakatkaisu tapahtuu tietojen muutoksia julkaistaessa** – Jos ilmoitus aikakatkaisusta avautuu, kun tietojen muutoksia yritetään julkaista yksikköön, kyseisen työnkirjan julkaisuerän koon pienentämistä kannattaa harkita. Jos yksikkö käynnistää suuren määrän logiikkaa tietueen muutosten yhteydessä, aikakatkaisujen estäminen voi edellyttää, että päivitykset lähetetään pienissä erissä.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
