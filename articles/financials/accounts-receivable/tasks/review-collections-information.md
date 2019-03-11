---
title: Perimistietojen tarkistaminen
description: Tässä menettelyssä käsitellään perintätietojen tarkastelemista sekä erilaisia asetusvaihtoehtoja ja perintätapahtumia.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustCollectionsPool, SysQueryForm, CustCollectionsAgent, OMTeamSelectMemberDialog, CustVendReportInterval, CustParameters, CustAgingSnapshot, CustVendAgingBucketLookUp, CustCollectionsPoolsListPage, CustCollectionsContactPart, CustCollections
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 44d89d2bacc8f301a19bfd09d229809d492a55fb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "349098"
---
# <a name="review-collections-information"></a>Perimistietojen tarkistaminen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä käsitellään perintätietojen tarkastelemista sekä erilaisia asetusvaihtoehtoja ja perintätapahtumia. Näissä toimintaohjeissa käytetään esittely-yritystä USMF.


## <a name="create-customer-pools"></a>Luo asiakaspoolit
1. Valitse Luotonvalvonta > Asetukset > Asiakaspoolit.
    * Voit määrittää tällä sivulla asiakaspooleja, jotka ovat asiakastiliryhmää määrittäviä kyselyjä. Ne voidaan näyttää ja niitä voidaan hallita perintä- ja erääntymisprosesseissa. Voit suodattaa Perinnät-luettelosivun ja liittyvien luettelosivujen tietoja asiakaspoolien avulla. Voit suodattaa myös erääntymistilannevedoksen luontiin sisältyneet asiakastilit asiakaspoolien avulla.  
    * Voit suodattaa erääntymistilannevedoksen luontiin sisältyneet asiakastilit asiakaspoolien avulla.  
2. Valitse Uusi.
3. Kirjoita arvo Ryhmän tunniste -kenttään.
4. Kirjoita Ryhmän kuvaus -kenttään arvo.
5. Valitse Valitse poolin ehdot.
6. Kirjoita arvo Ehdot-kenttään.
7. Valitse OK.
8. Valitse Asiakaspoolin esikatselu.

## <a name="create-collections-agents"></a>Luo perimisasiamiehet
1. Valitse Luotonvalvonta > Asetukset > Perimisasiamiehet.
    * Voit määrittää tällä sivulla työntekijöitä perimisasiamiehiksi. Ja voit halutessasi määrittää niihin asiakaspooleja. Perimisasiamies on henkilö, joka työskentelee asiakkaiden kanssa varmistaakseen, että maksut peritään ajoissa.  
    * Tällä sivulla määritetyt perimisasiamiehet lisätään automaattisesti perimisryhmään. Jos ryhmä on valittu Myyntireskontran parametrit -sivun Ryhmä-kentässä, perimisasiamiehet lisätään tähän ryhmään. Jos ryhmää ei ole valittu, uusi Perintä-niminen ryhmä luodaan automaattisesti ja perimisasiamiehet lisätään kyseiseen ryhmään.  
2. Valitse Uusi.
3. ValitseLisää.
4. Valitse Sulje.
5. ValitseLisää.
6. Merkitse valittu rivi luettelossa.
7. Avaa haku napsauttamalla Ryhmän tunnus -kentässä avattavan valikon painiketta.
8. Etsi haluamasi tietue luettelosta ja valitse se.
9. Valitse Oletusryhmä-valintaruutu tai poista sen valinta.
    * Valitse tämä vaihtoehto, kun haluat sisällyttää kaikki valitun perimisasiamiehen suodatinluetteloiden asiakaspoolit. Jos tätä vaihtoehtoa ei valita, vain perimisasiamiehelle määritetyt asiakaspoolit ovat käytettävissä suodatinluetteloissa.  

## <a name="create-aging-period-definition"></a>Luo erääntymiskausimääritys
1. Siirry kohtaan Luotonvalvonta > Asetukset > Erääntymiskausien määritykset.
    * Erääntymiskauden määrityksien avulla voit analysoida asiakas- ja toimittajatilien erääntymistä antamasi päivämäärän perusteella. Jokainen erääntymiskauden määritykselle asettamasi erääntymiskausi vastaa saraketta luettelosivulla tai lomakkeella tai raportissa, kun analyysi suoritetaan.  
2. Valitse Uusi.
3. Kirjoita arvo Erääntymiskauden määritys -kenttään.
4. Kirjoita arvo Kuvaus-kenttään.
    * Määritä kunkin erääntymiskausimääritykseen sisällytettävän erääntymiskauden nimi, yksikkö ja väli. Rivi, jonka Yksikkö-kentän arvo on 0 (nolla), ilmaisee analyysin suorituspäivän. Nollarivin edellä olevien rivien Yksikkö-kentän oletusarvo on -1 ja nollarivin jälkeisten rivien 1, mutta arvoja voi muuttaa.  Muuta rivien järjestystä Ylös- ja Alas-painikkeilla. Nollariviä ei voi siirtää.  
    * Aseta osoitin kohtaan, johon haluat uuden rivin, ja valitse Lisää.  
    * Valitse erääntymiskauden ilmaisin Perintä-lomakkeeseen ja luettelosivulle. Voit esimerkiksi valita vihreän ilmaisimen nykyiselle kaudelle, keltaisen 30 päivää erääntyneelle kaudelle ja punaisen 90 päivää erääntyneelle kaudelle.  
    * Valitse erääntymiskauden määrityksen tulostussuunta. Tämä valinta määrittää, missä järjestyksessä sarakkeet näkyvät asiakkaan erääntymisraportissa tai toimittajan erääntymisraportissa.  Eteenpäin – Tulosta sarakkeet siinä järjestyksessä, missä otsikot näkyvät taulukossa ylimmältä riviltä alkaen.  Taaksepäin – Tulosta sarakkeet päinvastaisessa järjestyksessä kuin missä otsikot näkyvät taulukossa alimmalta riviltä alkaen.    

## <a name="setup-collections-parameters"></a>Määritä perinnän parametrit
1. Siirry kohtaan Luotonvalvonta > Asetukset > Myyntireskontran parametrit.
2. Valitse Perintä-välilehti.
3. Laajenna tai tiivistä Perinnän oletukset -osa.
    * Valitse erääntymisen oletustilannevedoksen erääntymiskauden määritelmä, jota käytetään Perintä-lomakkeessa  
    * Valitse ryhmä, johon perimisasiamiehet on määritetty Perimisasiamies-lomakkeessa. Luettelossa näkyvät vain ryhmät, joiden ryhmätyyppi on Perintä.  
4. Laajenna tai tiivistä Poisto-osa.
    * Valitse kirjanpidon kirjauskansioille määritetty kirjauskansio, jota käytetään, kun tapahtuma kirjataan poistoksi Perintä-lomakkeessa tai liittyvillä luettelosivuilla.  
    * Valitse oletussyykoodi, jota käytetään, kun kirjattavat poistotapahtumat luodaan Perinnät-sivulla tai liittyvillä luettelosivuilla.  
    * Valitse tämä vaihtoehto, kun haluat luoda erillisen kirjauskansiorivin arvonlisäverosummille silloin, kun poiskirjaustapahtumat luodaan Perinnät-sivun tai liittyvien luettelosivujen avulla. Jos valitset tämän vaihtoehdon, voit seurata kätevästi poistotapahtumissa käytettäviä arvonlisäverosummia. Voit seurata arvonlisäverosummia erikseen, kun haluat oikaista liittyvän kauden arvonlisäverovelan helposti.  
5. Laajenna tai tiivistä Sähköpostimalli-osa.
    * Valitse sähköpostimalli, jota käytät sähköpostien lähettämiseen valitsemalla Perintä-lomakkeessa Sähköposti > Tapahtumat yhteyshenkilölle.  
    * Valitse sähköpostimalli, jota käytät asiakkaan tiliotteen lähettämiseen liitteenä valitsemalla Perintä-lomakkeessa Sähköposti > Raportti yhteyshenkilölle.  
    * Valitse sähköpostimalli, jota käytät sähköpostien lähettämiseen valitsemalla Perintä-lomakkeessa Sähköposti > Tapahtumat myyjälle.  

## <a name="age-customer-balance"></a>Eräännytä asiakkaan saldo
1. Siirry kohtaan Luotonvalvonta > Kausittaiset tehtävät > Eräännytä asiakkaan saldot.
    * Valitse erääntymiskausimääritys. Erääntymistilannevedosprosessi eräännyttää tapahtumat valitun erääntymiskauden määrityksessä määritettyjen erääntymiskausien perusteella.  
    * Valitse asiakaspooli tai jätä tämä kenttä tyhjäksi, kun luot asiakkaille erääntymistilannevedosta. Jos valitset asiakaspoolin, erääntymistilannevedosprosessia käytetään vain niissä asiakastileissä, jotka ovat osa asiakaspoolia. Valityn asiakaspoolin tyypin on oltava Erääntymistilannevedos.  
    * Valitse päivämäärän tyyppi, johon erääntymistilannevedos perustuu.    Tapahtumapäivä – tapahtuman päivämäärä, jonka perusteella kukin tapahtuma erääntyy.    Eräpäivä – eräpäivä, jonka perusteella kukin tapahtuma erääntyy.    Asiakirjan päivämäärä – asiakirjan päivämäärä, jonka perusteella kukin tapahtuma erääntyy.  
    * Valitse päivämäärä, jota käytetään erääntymistilannevedoksen kuluvana päivänä. Erääntymiskaudet lasketaan tämän päivämäärän perusteella.    Tämän päivän päivämäärä – Käytä järjestelmän päivämäärää. Käytä tätä vaihtoehtoa, jos käsittely on määritetty tapahtumaan toistuvana eränä. Jos käytät tätä päivämäärää, toistuva erä voidaan suorittaa säännöllisesti ja silloin käytetään järjestelmän päivämäärää.    Valittu päivämäärä – Käytä määrittämääsi päivämäärää. Jos valitset tämän vaihtoehdon, anna erääntymispäivä.  
2. Valitse OK.

## <a name="view-aged-customer-balances"></a>Näytä erääntyneet asiakkaan saldot
1. Siirry kohtaan Luotonvalvonta > Perintä > Erääntyneet saldot.
    * Voit tarkastella tällä luettelosivulla asiakkaan saldoja ja erääntymissummia erääntymiskauden mukaan. Nämä tiedot on tallennettu erääntymistilannevedokseen. Erääntymiskaudet on määritelty käytetyn erääntymiskauden määritelmän mukaan. Erääntymiskauden määritelmä on otettu asiakkaspoolista, jos sellainen on määritetty poolikyselylle. Jos asiakaspoolilla ei ole erääntymiskausimääritelmää, käytetään Myyntireskontran parametrit -lomakkeessa määritettyä oletuserääntymiskauden määritelmää.  
2. Laajenna Yhteyshenkilö-tietoruutu.
    * Asiakkaan perinnän yhteyshenkilö.  
    * Asiakkaan oletusmyyjä.  
3. Laajenna Luottoraja-tietoruutu.
    * Voit tarkastella Luottotiedot-tietoruudussa asiakkaan luottorajaa ja nykyisiä saldotietoja.  

## <a name="view-customer-collections-details"></a>Näytä asiakkaan perintätiedot
1. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
2. Laajenna Osoite-tietoruutu.
3. Laajenna Yhteyshenkilö-tietoruutu.
4. Laajenna Erääntyminen-tietoruutu.
5. Laajenna Luottoraja-tietoruutu.
6. Valitse toimintoruudussa Perintä.
    * Päivitä asiakkaan erääntymistilannevedos käyttämällä kuluvaa päivämäärää erääntymispäivämääränä, johon tapahtumapäivämääriä verrataan. Jos erääntymistilannevedoksessa on useiden yritysten tietoja, päivitetyssä erääntymistilannevedoksessa on tietoja samoista yrityksistä. Summat tallennetaan sen yrityksen kirjanpitovaluuttaan, johon olet kirjautunut, kun päivitit erääntymistilannevedoksen.  
    * Valitse erääntymiskausimääritys. Asiakkaan erääntymistilannevedokseen liitetty erääntymiskausimääritys näytetään oletusarvoisesti. Erääntymiskausimääritys määrittää, mitkä erääntymiskaudet ja summat näytetään Erääntyneet saldot- ja Luottotiedot-tietoruuduissa.  
    * Avaa valikko, jossa on seuraavat nimikkeet: Yritys – näytä Erääntyneet saldot- ja Luottotiedot-tietoruutujen summat yrityksen kirjanpitovaluutassa.    Asiakas – näytä Erääntyneet saldot- ja Luottotiedot-tietoruutujen summat asiakkaan valuutassa.  
    * Valitse asiakkaan erääntymistilannevedoksessa ainakin yksi yritys, jonka tiedot näytetään. Luettelossa näytetään yritykset, jotka valittiin, kun erääntymistilannevedos luotiin.  
    * Näytä asiakkaan tiliote Microsoft Excel -muodossa. Voit valita tiliotteeseen sisällytettävän tapahtuma-alueen aloituspäivän ja päättää myöhemmin, sisällytetäänkö vain avoimet tapahtumat vai sekä avoimet että tilitetyt tapahtumat. Jos erääntymistilannevedoksessa on useita yrityksiä, kaikkien yritysten tapahtumat sisällytetään.  
    * Avaa Asiakirjat-lomake, jossa voit luoda ja muokata tiedostoja tai huomautuksia.  
7. Valitse toimintoruudussa Ota yhteyttä.
    * Avaa Outlook, jossa voit lähettää sähköpostiviestin Yhteyshenkilö-kentässä määritetty yhteyshenkilölle. Jos perinnän yhteyshenkilöä ei ole määritetty, käytetään asiakkaan ensisijaista osoitetta. Jos ensisijaista yhteyshenkilöä ei ole määritetty, sähköpostiviestit lähetetään Yhteyshenkilöt-lomakkeessa ensimmäisenä olevaan sähköpostiosoitteeseen. Valitut tapahtumat sisällytetään liitteinä. Excel-muotoisessa liitteessä on kolme laskentataulukkoa. Asiakkaan yhteyshenkilöille lähetettävien viestien sähköpostimalli voidaan määrittää Myyntireskontran parametrit -lomakkeessa.  
    * Tämä painike ei ole käytettävissä, jos tässä lomakkeessa valitulle yhteyshenkilölle ei ole määritetty sähköpostiosoitetta.  
    * Valmistele tiliote, avaa Outlook ja lähetä sähköpostiviestiin liitetty tiliote Yhteyshenkilö-kentässä määritettyyn osoitteeseen. Jos perinnän yhteyshenkilöä ei ole määritetty, käytetään asiakkaan ensisijaista osoitetta. Jos ensisijaista yhteyshenkilöä ei ole määritetty, sähköpostiviestit lähetetään Yhteyshenkilöt-lomakkeessa ensimmäisenä olevaan sähköpostiosoitteeseen.  
    * Tämä painike ei ole käytettävissä, jos tässä lomakkeessa valitulle yhteyshenkilölle ei ole määritetty sähköpostiosoitetta.  
    * Avaa Outlook ja lähetä sähköpostiviesti työntekijälle, joka on määritetty asiakkaalle määritetyn myyntiryhmän myyntiedustajalle. Jos tapahtumia on valittu, ne sisältyvät viestiin liitteinä. Excel-muotoisessa liitteessä on kaksi laskentataulukkoa. Myyjille lähetettävien viestien sähköpostimalli voidaan määrittää Myyntireskontran parametrit -lomakkeessa.  
    * Tämä painike ei ole käytettävissä, jos tässä lomakkeessa näkyvälle myyjälle ei ole määritetty sähköpostiosoitetta.  
    * Tarkastele asiakkaan tapahtumia ja tee niissä toimintoja. Jos käytät keskitettyjä maksuja, asiakkaan erääntymistilannevedokseen sisältyvien yritysten tiedot ovat mukana. Voit rajoittaa yrityksen tietoja toimintoruudun valintaryhmän yrityspainikkeella.  
    * Muuta valittujen tapahtumien perimistila.    Ei riitautettu – Perimistoimintoa ei ole tapahtunut tapahtumalle.    Riidanalainen – Asiakas on ilmoittanut, että tapahtumassa on ongelma.    Luvattu maksaa – Asiakas on sopinut maksavansa tapahtuman summan.    Ratkaistu – Kaikki tapahtumaan liittyvät ongelmat on ratkaistu ja eikä muita perimistoimintoja tarvita.  
    * Avaa valikko ja määritä lomakkeessa näytettävät toiminnot valitsemalla jokin seuraavista vaihtoehdoista: Avoin – Näytä vain tapahtumat, joita ei ole tilitetty.    Avoimet ja suljetut – Näytä kaikki tilitetyt ja tilittämättömät tapahtumat.  
    * Käsittele valittu NSF (ei katetta) -maksuna.    Tämä painike on käytettävissä vain, jos valittu tapahtuma on maksu (maksettavien saldo ilman laskua), joka on viety maksukirjauskansioon ja tapahtumalle määritetylle pankkitilille eikä maksua ole aiemmin peruutettu.  
    * Kirjaa valitut tapahtumat pois.  
    * Merkitse valitut tapahtumat keskinäistä tilitystä varten.  
    * Avaa Alkuperäinen tiedosto -lomake, jossa voit tarkastella ja tulostaa valitun tapahtuman asiakirjan.  
    * Avaa seuraavat vaihtoehdot sisältävä valikko: Perintä – Näytä vain Perinnät-lomakkeessa luodut tehtävät.    Kaikki– Näytä asiakkaan kaikki tehtävät riippumatta siitä, missä ne luotiin.  
    * Avaa valikko, jossa on seuraavat vaihtoehdot: Avoin – Näytä vain tehtävät, joita ei ole suljettu.    Avoimet ja suljetut – Näytä kaikki tehtävät niiden tilasta riippumatta.  
    * Valitse asiakkaalle määritetty perintätapaus tai jätä kenttä tyhjäksi. Jos tapaus on valittu, vain kyseiseen tapaukseen liittyvät tapahtumat ja tehtävät näkyvät tässä lomakkeessa.  
8. Valitse Näytä luettelo.
    * Valitse asiakas tai hyväksy oletusarvo. Oletusarvoisesti tämä asiakastili on valittu luettelosivulta tai lomakkeesta, josta avasit tämän lomakkeen. Jos avasit lomakkeen luettelosivulta, luettelon asiakkaat ovat asiakkaille, jotka on sisällytetty luettelosivulla käytettävään perintäpooliin.  

