---
title: Varaston sulkeminen
description: "Voit myös valita, että kirjanpitoon päivitetään ottotapahtumien vastaanottotapahtumiin täsmäytysprosessissa tehdyt muutokset."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventClosing
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 61973
ms.assetid: c210c882-6849-4704-b78c-a777dd6cfdb6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: dc192b332bd736fd2ba1aac16e9e4614f3afc1dd
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="inventory-close"></a>Varaston sulkeminen

[!include[banner](../includes/banner.md)]


Voit myös valita, että kirjanpitoon päivitetään ottotapahtumien vastaanottotapahtumiin täsmäytysprosessissa tehdyt muutokset.

Varaston sulkemisprosessi selvittää varasto-ottotapahtumat vastaanottotapahtumiksi nimikkeen nimikemalliryhmässä valitun varastonarvostusmenetelmän perusteella. Selvitysprosessin yhteydessä voit määrittää, että kirjanpito on päivitettävä, jotta se vastaa tehtyjä oikaisuja. Varaston sulkemiseen tai uudelleenlaskentaan saakka tapahtumat kirjataan kuitenkin lasketun keskimääräisen kustannushinnan mukaan. 

Varaston sulkemisen jälkeen ei voi enää tehdä kirjauksia asettamillesi varaston sulkemispäivämäärää edeltäville kausille, ellet peruuta valmista varaston sulkuprosessia. Jos varaston sulkeminen esimerkiksi suoritetaan kaudelle, joka päättyy 31. tammikuuta, et voi kirjata tapahtumia, joiden päivämäärä on aikaisempi kuin 31. tammikuuta. 

Varaston nimikkeille määritetään toinen kahdesta varastotyypeistä: nimike tai palvelu. Varaston sulkeminen suorittaa samaa toimet molemmille tyypeille. Palvelunimikkeissä varaston sulkeminen täsmäyttää varasto-otot edelleen vastaanottojen kanssa. 

Varaston sulkemisväli on eri yrityksissä eri pituinen. Tapahtumien määrä auttaa kuitenkin määrittämään, kuinka usein varaston sulkeminen tulisi suorittaa. Useimmat yritykset suorittavat varaston sulkemisen tavallisesti sulkemis- ja täsmäytystoimien yhteydessä joka kuukauden päätteeksi.

## <a name="inventory-recalculation-and-the-general-ledger"></a>Varaston uudelleenlaskenta ja kirjanpito
Jos varastoon ja kirjanpitoon pitää tehdä oikaisuja kuukauden tai muun varastokauden aikana, voit suorittaa varaston uudelleenlaskennan varaston sulkemisen asemesta. Varaston uudelleenlaskennassa varastotapahtumiin tehdään oikaisuja, mutta täsmäytyksiä ei tehdä. 

Varaston uudelleenlaskennan aikana oikaistaan käytettävissä oleva varasto ja varastotapahtumat. Lisäksi suoritetaan varastojen uudelleenlaskenta ja varaston sulkemiset. Nämä tehtävät vaikuttavat niihin kirjanpitotileihin, jotka on linkitetty alkuperäiseen varastotapahtumaan. 

**Esimerkki** 

Kun luot ostotilauksen myyntitilauksesta, päivitetään alkuperäisen myyntitilauksen kirjanpitotilit. Vaikka tälle nimikkeelle määritetyn nimikeryhmän kirjanpitotilit olisivat vaihtuneet myyntitilauksen kirjaamisen jälkeen ja varaston uudelleenlaskenta olisi luonut oikaisusumman, tämä oikaisusumma kirjataan alkuperäiselle kirjanpitotilille. Oikaistua summaa ei kirjata nimikkeen uusille kirjanpitotileille. 

Kun päivitys on valmis, voit tarkastella kirjattua kirjanpitotositetta, joka on kirjattu tehtävän vuoksi.

1.  Valitse tarkistettava päivitys **Päätös ja oikaisu** -sivun **Yhteenveto** -välilehdessä.
2.  Valitse **Tiedot** ja sitten **Tosite**.

## <a name="effects-of-the-inventory-close-process-on-the-general-ledger"></a>Varaston sulkemisprosessin vaikutukset kirjanpitoon
Useat **Päätös ja oikaisu** -sivulla suorittamasi tehtävät päivittävät kirjanpitoa. Kirjanpito päivittyy esimerkiksi silloin, kun teet oikaisuja varaston käytettävissä olevaan määrään tai varastotapahtumiin tai suoritat varaston uudellenlaskennan ja varaston sulkemisen. 

Nämä tehtävät päivittävät kirjanpitotilejä, jotka on linkitetty alkuperäiseen varastotapahtumaan. Jos esimerkiksi myyntitilaus ja ostotilaus selvitetään, alkuperäisessä myyntitilauksessa käytetyt kirjanpitotilit oikaistaan. Näin tapahtuu, vaikka tähän nimikkeeseen määritetyn nimikeryhmän kirjanpitotilit ovat muuttuneet myyntitilauksen kirjaamisen jälkeen. Kun varaston sulkeminen on luonut tilityssumman, tilityssumma kirjataan alkuperäisiin kirjanpitotileihin, ei nimikkeelle määritettyihin uusiin kirjanpitotileihin. Kirjanpito voidaan myös päivittää, jos peruutat varaston sulkemisen. 

**Huomautuksia:**

-   Varaston sulkeminen ei ole pakollista, jos käytät standardikustannusten arvostustapaa.
-   Ennen sulkemismenettelyn suorittamista voit tarkastaa listan nimikkeistä, joita ei voi selvittää päivityksen aikana.
-   Varaston sulkeminen kannattaa ajoittaa aikaan, jona kuormitus ei ole huipussaan, jotta tietojenkäsittelyresurssit voidaan jakaa tasaisemmin.

## <a name="the-inventory-close-log"></a> Varaston sulkemisloki
Kun varasto on suljettu, viestikeskuksessa voidaan ilmoittaa, että yksikön kustannushinta on virheellinen, koska tapahtumaa ei voitu täysin selvittää. 

Ennen kuin tämä sanoma tulee näyttöön, järjestelmä ilmoittaa nimiketunnuksen sekä tapahtuman, johon tilanne vaikuttaa. Sanoma kertoo, että tapahtumassa käytettävää kustannussummaa ei päivitetty varaston sulkemisen takia. Sanoma tulee näyttöön, kun varasto-ottotapahtumaa ei voida selvittää. 

Järjestelmä tarkistaa varaston sulkemisprosessin yhteydessä jokaisesta taloushallinnon dimensiosta, onko varasto-ottoja enemmän kuin vastaanottoja määritettyyn sulkemispäivämäärään mennessä. Näin voi tapahtua, kun ostotilauksen varastotapahtumaa ei kirjata kokonaan, koska toimittajan laskua ei ole vastaanotettu, tai koska tuotannon ylätason tuoterakennekomponentteja ei kirjata kirjanpitoon. (Osatuotannolle ei ole tehty kustannuslaskentaa.) Tällöin seuraava sulkeminen ei oikaise kaikkiin varasto-ottoihin oikeaa kustannushintaa, sillä kaikkia tarvittavia vastaanottotietoja ei ole käytettävissä. 

Järjestelmä ilmoittaa jokaiselle sulkemismenettelyn ajon osalta, onko varoitukset sisältävä lokitiedosto tallennettu ja voiko sitä tarkastella. 

Jos sanoma sisältää useita varoituksia, on suositeltavaa suorittaa seuraavat toimenpiteet:

-   Päivitä vastaanotot kirjanpitoon.
-   Siirrä sulkemispäivää eteenpäin.
-   Uudelleenarvioi liiketoimintaprosessit.

Joissakin tapauksissa et voi ehkä tehdä mitään varoitusten suhteen. Kun esimerkiksi käytetään merkintää ja merkityn ostotilauksen rahoituspäivämäärä on sulkemispäivän jälkeen, sulkemispäivää ei voi muuttaa.

## <a name="reversing-a-completed-inventory-close"></a>Valmiin varaston sulkemisen peruuttaminen
Saatat joskus joutua peruuttamaan valmiin varaston sulkemisen ja palauttamaan täsmäytykset tilaan, jossa ne olivat ennen oikaisujen tekemistä. Kun valmis varaston sulkeminen peruutetaan, varasto myös avataan uudelleen, ja kirjaukset kyseisellä kaudella ovat taas mahdollisia. Kirjanpitoon voidaan tehdä myös liittyvät muutokset. Kun olet tehnyt haluamasi muutokset, voit suorittaa varaston sulkemisen uudelleen kaudelle, jota käsittelet. 

**Huomautus:** Vain viimeinen suljettu varastojakso voidaan avata uudelleen. Jos haluat peruuttaa aiemman varaston sulkemisen, jokainen seuraava varaston sulkeminen on peruutettava yksi kerrallaan uusimmasta sulkemisesta alkaen.




