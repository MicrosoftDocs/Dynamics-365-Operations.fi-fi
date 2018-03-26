---
title: "Siirtyminen sähköiseen hankintaan käytettyjen ulkoisten luetteloiden määrittäminen"
description: "Tässä ohjeaiheessa kuvataan ulkoisen luettelon tai siirtymisluettelon käyttöä tarjouspyynnön tietojen keräämisessä toimittajalta ja sen lisäämistä varasto-ottoehdotukseen."
author: mkirknel
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 2c37f0253454a23d90904dd6b000b955146ad121
ms.contentlocale: fi-fi
ms.lasthandoff: 03/07/2018

---

# <a name="set-up-an-external-catalog-for-punchout-eprocurement"></a>Siirtyminen sähköiseen hankintaan käytettyjen ulkoisten luetteloiden määrittäminen

[!include[banner](../includes/banner.md)]

Ulkoisen luettelon avulla voit varmistaa, että Dynamics 365 for Finance and Operations Enterprise edition heinäkuun 2017 päivityksellä myöhemmin käsiteltävät tuote- ja hintatiedot ovat paikkansapitäviä ja ajan tasalla. Varasto-ottoehdotus voidaan hyväksyä ja muuttaa ostotilaukseksi ja tilaus voidaan lähettää toimittajalle.

Kun ulkoinen luettelo on määritetty ja työntekijä valmistelee varasto-ottoehdotusta, tapahtuma voidaan ohjata ulkoiselle sivustolle, ulkoiseen luetteloon ja palauttaa ostoskori, joka on luotu ulkoisessa sivustossa. Tämän viestintä perustuu cXML-protokollaan ja se pitää määrittää osto- ja myyntiorganisaation järjestelmien välille.

Tiedonsiirron määrittääksesi toimittajan on luovutettava käyttöösi tietoja, joita voit käyttää ulkoisen luettelon konfiguraatiossa, kuten henkilöllisyys, ostajayrityksen toimialue, esimerkiksi "DUNS" ja "DUNS-numero", tunnistetiedot ja URL-osoite toimittajaluetteloon pääsemiseksi.

## <a name="setting-up-an-external-catalog"></a>Ulkoisen luettelon asettaminen

Ulkoisen luettelon avulla työntekijä, joka määrittää ostoehdotuksen, pitää ohjata ulkoiseen sivustoon valitsemaan tuotteita. Tuotteet, jotka työntekijä valitsee ulkoisesta luettelosta, palautetaan Dynamics 365 for Finance and Operationsiin ajan tasalla olevien hintatietojen kera, minkä jälkeen ne voidaan lisätä ostoehdotukseen. Tarkoituksena ei ole, että työntekijät voivat tehdä tilauksen ulkoisessa sivustossa. Ulkoista luetteloa määritettäessä on varmistettava, että sivuston, jota voidaan käyttää ulkoisesta luettelosta, tarkoituksena on tarjoustietojen kerääminen eikä todellisen tilauksen tekeminen.

### <a name="to-set-up-an-external-vendor-catalog-complete-the-following-tasks"></a>Kun määrität ulkoisen toimittajan tuoteluettelon, tee seuraavat tehtävät:

1. Määritä hankintaluokkahierarkia. Katso lisätietoja kohdasta [Aseta menettelytavat hankintaluokkien hierarkioille](tasks/set-up-policies-procurement-category-hierarchies.md).
2. Rekisteröi toimittaja Finance and Operationsiin. Ennen kuin voit määrittää toimittajan ulkoisen luettelon sivustolle pääsyn konfiguraatiot, sinun on määritettävä toimittaja ja toimittajan yhteystiedot Microsoft Dynamics 365 -järjestelmässä. Lisäksi ulkoisen luettelon toimittaja on lisättävä valittuun hankintaluokkaan. Lisätietoja toimittajien rekisteröinnistä Microsoft Dynamics 365:een on kohdassa [Toimittajayhteistyön käyttäjien hallinta](manage-vendor-collaboration-users.md). Tietoja toimittajien määrittämisestä hankintaluokkaan on kohdassa [Hyväksy toimittajia tiettyihin hankintaluokkiin](tasks/approve-vendors-specific-procurement-categories.md).
3. Varmista, että mittayksiköt ja toimittajan käyttämä valuutta on määritetty. Mittayksikön luomista koskevia lisätietoja on kohdassa [Mittayksiköiden hallinta](../pim/tasks/manage-unit-measure.md).
4. Konfiguroi ulkoinen toimittajaluettelo käyttämällä vaatimuksia toimittajan ulkoiselta luettelosivustolta. Lisätietoja tästä tehtävästä on kohdassa [Ulkoisen toimittajaluettelon määrittäminen](#configure-the-external-vendor-catalog).
5. Testaa toimittajan tuoteluettelon konfiguraatiot ja tarkista, että asetukset ovat voimassa ja voit käyttää toimittajan ulkoista tuoteluetteloa. Vahvista toimenpiteet, joilla vahvistat määrittämäsi pyynnön asetussanomat, **Vahvista asetukset** -toiminnolla. Tämän sanoman pitää avata toimittajien ulkoinen luettelosivusto selainikkunaan. Vahvistettaessa et voi tilata nimikkeitä ja palveluja toimittajalta. Tilataksesi nimikkeet ja palvelut on siirryttävä toimittajaluetteloon ostoehdotuksesta.
6. Aktivoi ulkoinen luettelo **Aktivoi luettelo** -painikkeella **Ulkoiset luettelot** -sivulla. Ulkoinen luettelo on otettava käyttöön, ennen kuin työntekijät voivat käyttää sitä. Voit poistaa ulkoisen luettelon milloin tahansa.


## <a name="configure-the-external-vendor-catalog"></a>Ulkoisen toimittajaluettelon määrittäminen

Tämä osa sisältää lisätietoja vaiheesta 4 edellä olevassa osassa.

1. Kirjoita toimittajan ulkoisen luettelon nimi ja kuvaus. Antamasi nimi näkyy ostokorissa, joka edustaa ulkoista luetteloa, joka näkyy työntekijöille, jotka luovat varasto-ottoehdotuksen. Työntekijät voivat avata toimittajan ulkoisen tuoteluettelosivuston napsauttamalla ostoskoria.
2. Lisätä kuva **Ulkoisen luettelon kuva** -toiminnolla. Antamasi kuva näkyy ostokorissa, joka edustaa ulkoista luetteloa, joka näkyy työntekijöille, jotka luovat varasto-ottoehdotuksen. Huomaa, että kuvan leveys ja korkeus on oltava samat. Muussa tapauksessa kuva ei näy oikein.
3. Valitse, näytetäänkö toimittajan tuoteluettelosivuston saman selaimen ikkunassa jossa työntekijän loi varasto-ottoehdotuksen, vai pitäisikö sen avautua uudessa ikkunassa.
4. Valitse luettelon toimittaja. **Yritykset**-luettelossa on rivi jokaiselle yritykselle, johon toimittaja on määritetty. Jotta käyttäjät voivat pyytää suoraan joidenkin yritysten toimittajan luettelon tuotteita, voit määrittää luettelon käytettävyyden **Estä käyttö** tai **Salli käyttö** -painikkeilla.
5. Kirjoita **Oletusarvoinen vanhentuminen (päivinä)** -kenttään, montako päivää ulkoisesta luettelosta vastaanotettu tarjous on voimassa ja kuinka kauan sitä voidaan käyttää ulkoiselta toimittajalta suoritettaviin ostoihin. Kun tarjous luodaan ja noudetaan toimittajan ulkoiselta luettelosivustolta, tarjous on voimassa nykyisestä järjestelmän päivämäärästä alkaen ja voimassa tähän kenttään kirjoittamasi päivien ajan.
6. Käynnistä hankintaluokkien määritys ulkoiseen luetteloon napauttamalla **Lisää** -painiketta. Valitse sitten Luokka-nimiluettelosta luokka. Luokkaluettelo on hankintaluokkien ylijoukko, johon toimittaja on määritetty kaikissa yrityksissä, jotka on määritetty toimittajalle.
[!NOTE]
Hankintakäytäntöjen avulla sallitaan tai rajoitetaan luokkien käyttöoikeuksia yrityksen ostoa tai toimintayksikön vastaanottoa varten. Siirtyminen ulkoiseen luetteloon edellyttää vähintään yhden luetteloon yhdistetyn hankintaluokan käyttöoikeuksia.
7. Määritä cXML-asetuspyyntöviesti, joka lähetetään toimittajalle. Automaattisesti luotu sanomamuoto on vähimmäismalli, joka vaaditaan, jotta voidaan aloittaa istunto. Syötä arvot tunnisteita varten.

Voit milloin tahansa ladata järjestelmän luoman viestin mallin valitsemalla **Palauta viestimuoto**. Huomaa, että jos palautat viestin muodon, nykyinen viesti korvataan automaattisesti luodulla viestimuodolla, jossa on tyhjiä tunnisteita.

### <a name="cxml-setup-message"></a>cXML-määritysviesti
Ohessa on kuvaus tunnisteista, jotka sisältyvät malliin:

| Kenttä | kuvaus | 
|---------|---------|
|< Header >< From >< Credential domain=”” >|Ostajan yrityksen toimialue.|
|< Header >< From >< Credential>< Identity >< /Identity > | Ostajan yrityksen tunnus.|
|< Header >< To >< Credential domain=”” > | Toimittajan yrityksen toimialue.|
|< Header >< To >< Credential>< Identity >< /Identity> | Toimittajan yrityksen tunnus.|
|< Header >< Sender >< Credential domain=”” > | Ostajan yrityksen toimialue.|
|< Header >< Sender >< Credential >< Identity >< /Identity> | Ostajan yrityksen tunnus.|
|< Header >< Sender >< Credential >< SharedSecret >< /SharedSecret >|Ostajan yrityksen jaettu salainen koodi.|
|< Request deploymentMode=”” >|Testaus tai tuotannon käyttöönotto.|
|< Request >< PunchOutSetupRequest >< SupplierSetup >< URL >< /URL>|Toimittajan yrityksen siirtymispäätepisteen URL-osoite.|

### <a name="extrinsic-elements"></a>Ulkoiset elementit

Ulkoinen elementti on lisätieto, kuten käyttäjätunnus, joka perustuu käyttäjä, jolle siirto suoritetaan. Ulkoinen elementti määritetään, kun siirto tapahtuu ja se voidaan lähettää viestin pyynnön asetussanomassa.
Toimittajalla voi olla vaatimus ulkoisen elementin vastaanottamisesta määrityspyynnössä. Tällöin kannattaa lisätä ulkoinen elementti ulkoisten elementtien luetteloon **Viestimuoto**-osassa **Ulkoinen luettelo** -sivulla. Määritä ulkoisen elementin nimi, jonka toimittaja voi tunnistaa, ja liitä se arvoon. Arvojen vaihtoehdot ovat: käyttäjänimi, sähköposti tai satunnainen arvo.
Saat lisätietoja cXML-protokollasta kohdasta: http://cxml.org/

## <a name="post-back-message"></a>Takaisinlähetysviesti
Takaisinlähetysviesti on viesti, joka saadaan toimittajalta, kun käyttäjä kirjautuu pois ulkoisesta sivustosta ja palaa Finance and Operationsiin. Takaisinlähetysviestejä ei voi määrittää. Sanomat perustuvat cXML protocol määritys. Seuraavassa on tietoja, jotka voivat kuulua takaisinlähetysviestissä, joka vastaanotetaan ostoehdotuksen rivillä:

| Toimittajalta vastaanotettu viesti | Kopioitu ostoehdotuksen riville Finance and Operationsissa|
|------------------------------|----------------------------------------------------------|
|< ItemIn quantity=”” > |Määrä|
|< ItemIn >< ItemID >< SupplierPartID >< /SupplierPartID >|Ulkoinen nimiketunnus|
|< ItemDetail>< UnitPrice >< Money currency=”” >| Valuutta|
|< ItemDetail >< UnitPrice >< Money >< /Money >| Yksikköhinta|
|< ItemDetail >< Description ShortName=”” >|Tuotteen nimi|
|< ItemDetail >< Description >< /Description >|Sisältyy nimikkeen kuvaukseen; Tuotenimi, jos ShortName ei ole määritetty.|
|< ItemDetail >< UnitOfMeasure >< /UnitOfMeasure >|Yksikkö|
|< ItemDetail >< Classification >< /Classification >|Sisältyy nimikkeen kuvaukseen|
|< ItemDetail >< Classification domain=”” >|Sisältyy nimikkeen kuvaukseen|

## <a name="delete-an-external-catalog"></a>Poista ulkoinen luettelo
Poista ulkoinen luettelo sivulla olevalla Poista-toiminnolla.

Ulkoista toimittajan tuoteluetteloa ei voi poistaa, jos tuotetta on pyydetty ulkoisesta toimittajan tuoteluettelosta. Sen sijaan ulkoisen toimittajan tuoteluettelon tilaksi määritetään ei-aktiiviseksi. Jos haluat poistaa ulkoisten toimittajien luettelon sivuston käyttöoikeudet mutta et poistaa niitä, muuta ulkoisen tuoteluettelon tilaksi ei-aktiivinen.


