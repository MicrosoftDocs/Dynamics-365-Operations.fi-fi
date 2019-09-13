---
title: Toimittajamaksun peruuttaminen
description: Tässä artikkelissa kuvataan, mitä eroa on maksun palauttamisella, poistamisella, mitätöimisellä ja hylkäämisellä. Lisäksi artikkelissa esitellään kaksi tapaa peruuttaa toimittajan sekki.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankChequeTable, LedgerJournalTransBankChequeReversal, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14361
ms.assetid: 9f0a1883-cbe0-4cc7-b9f3-dd12fb85ebe8
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db9208c8e76d963d5b8f6bee6b7c73268af68734
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867747"
---
# <a name="reverse-a-vendor-payment"></a>Toimittajamaksun peruuttaminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan, mitä eroa on maksun palauttamisella, poistamisella, mitätöimisellä ja hylkäämisellä. Lisäksi artikkelissa esitellään kaksi tapaa peruuttaa toimittajan sekki. 

Toisinaan toimittajamaksun kirjaamisen jälkeen maksu on peruutettava. Peruutus eroaa maksun poistamisesta, mitätöinnistä tai hylkäämisestä. Maksun voi poistaa vain, jos sen tila on **Luotu**. Tämä tila ilmaisee, että maksu on luotu, mutta järjestelmä ei ole vielä suorittanut sitä. Tämä rajoitus pätee aina maksutavasta riippumatta. Voit mitätöidä kirjaamattomat sekit sen jälkeen, kun ne on luotu, mutta ennen niiden kirjaamista. Jos luotu maksu suoritetaan sähköisenä rahansiirtona, voit hylätä maksun ennen sen kirjaamista. Jos haluat hylätä maksun, muuta **Maksutila**-arvoa. Maksu, joka on mitätöity tai hylätty, voidaan luoda uudelleen, kun **Maksutila**-arvoksi on palautunut **Ei mitään**. 

Maksun kirjaamisen jälkeen käytetään peruutuksia. Sähköisesti suoritettuja maksuja ei voi peruuttaa enää kirjaamisen jälkeen. Sen sijaan maksun summalle on luotava uusi tapahtuma, jotta velka voidaan siirtää takaisin toimittajan tilille. Kirjatut sekit voi peruuttaa kahdella tavalla. Toisessa tavassa peruutukset kirjataan heti, kun napsautat **Maksun mitätöinti** -painiketta **Sekki**-sivulla. Kun käytät toista tapaa ja napsautat **Maksun mitätöinti** -painiketta **Sekki**-sivulla, peruutus lähetetään sekkipalautusten kirjauskansioon Maksuliikenteen hallinta -kohtaan, jossa tarkistaja voi kirjata tai hylätä peruutuksen. 

Voit tarkistaa organisaatiossasi käytössä olevan tavan **Maksuliikennetiedot**-sivulta. Jos **Käytä tarkistusprosessia maksujen palautuksissa** -asetuksena on **Kyllä**, peruutukset lähetetään sekkipalautusten kirjauskansioon tarkistettaviksi. Seuraavassa taulukossa kuvataan, kuinka sekin peruutusmenetelmät eroavat.

| Jos organisaatiosi ei tarkista sekkien peruutuksia ennen kirjausta                                                                                                                                  | Jos organisaatiosi tarkistaa sekkien peruutukset ennen kirjausta                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sekki peruutetaan heti, kun valitset **Sekki**-sivulta **OK**.                                                                                                                      | Sekkiä ei peruuteta heti. Sekkien peruutuksen kirjauskansio luodaan tarkastusta varten. Jos sekkien peruutusten kirjauskansio poistetaan, sekki voidaan palauttaa uudelleen.                                                                                                                                                                                                                                                                |
| Alkuperäisen sekin kirjanpitomerkinnät palautetaan.                                                                                                                                         | Alkuperäisen sekin kirjanpitomerkinnän kirjanpitotiliä ei ole ehkä kirjattu. Alkuperäisen sekin kirjauskansion taloushallinnon dimensioita käytetään oletusarvoisina taloushallinnon dimensioina sekkipalautusten kirjauskansiossa. Näitä oletusarvoja voi muuttaa. Kun sekkipalautuksen kirjauskansio kirjataan, ostoreskontran päätilit lisätään automaattisesti kirjausprofiileista, ja ne ovat voineet muuttua. |
| Alkuperäisen sekin kirjaukseen käytettyjä kirjanpitorakenteita käytetään sekin palauttamiseen, vaikka tilirakennetta on muutettu. Kirjanpitotiliyhdistelmää ei vahvisteta. | Jos tilirakennetta muutetaan sen jälkeen, kun alkuperäinen sekki on kirjattu, uusi taloushallinnon dimensio voi olla pakollinen sekin peruutukseen. Tätä taloushallinnon dimensiota ei ehkä ole lisätty automaattisesti alkuperäisen maksun kirjauskansiosta. Tiliyhdistelmä tarkistetaan sekin peruutuksen kirjaamisen yhteydessä.                                                                                                        |
| Kiinteitä dimensioita ei oteta käyttöön peruutuksessa. Näin voidaan varmistaa, että peruutus tehdään samoilla kirjanpitotileillä.                                                                                      | Kiinteitä dimensioita käytetään sekkien peruutusten kirjauskansiossa kirjauksen aikana. Taloushallinnon dimensioarvoa ei ole ehkä olemassa alkuperäisen sekin kirjanpitomerkinnässä, riippuen siitä, milloin kiinteä dimensio määritettiin.                                                                                                                                                                                                     |

## <a name="reverse-posted-checks-without-reviewing-them"></a>Peruuta Kirjatut sekit tarkistamatta niitä
Jos organisaatio haluaa sekkien peruutukset kirjattavaksi heti, kun valitset **Sekit**-sivulta **Maksun mitätöinti**. Määritä **Maksuliikennetiedot**-sivulla **Käytä tarkistusprosessia maksujen palautuksissa** -asetukseksi **Ei**. **Sekit**-sivulla voit valita peruutettavan sekin ja valita sitten **Maksun mitätöinti**. Määritä sitten päivämäärä ja valitse peruutuksen syy.

## <a name="reverse-posted-checks-after-they-are-reviewed-in-the-check-reversal-journal"></a>Kirjattujen sekkien peruuttaminen, kun ne on tarkistettu sekkipalautusten kirjauskansiossa
Jos organisaatio haluaa tarkistaa sekkien peruutukset ennen niiden kirjaamista, luo sekkipalautusten kirjauskansio ja määritä **Maksuliikennetiedot**-sivulla **Käytä tarkistusprosessia maksujen palautuksissa** -asetukseksi **Kyllä**. **Sekit**-sivulla voit valita peruutettavan sekin ja valita sitten **Maksun mitätöinti**. Määritä sitten päivämäärä ja valitse peruutuksen syy. Rahoituksellinen syy on määritettävä sekä Pankki-että Toimittaja-tyypeille. Sinun on myös valittava kirjauskansion nimi, jotta voit luoda sekkipalautusten kirjauskansion.

### <a name="review-a-reversal"></a>Peruutuksen tarkistaminen

Jos olet peruutusten tarkistuksia tekevä käyttäjä, voit hyväksyä ja kirjata kirjauskansion tai hylätä peruutuksen poistamalla kirjauskansion. **Sekkipalautusten kirjauskansio** -sivulla voit valita tarkistettavan palautusten kirjauskansion. Valitse sitten **rivit**. Voit tarkistaa peruutetun sekin ja valita sitten toisen seuraavista hyväksymisvaihtoehdoista:

-   Jos haluat hyväksyä ja kirjata palautusten kirjauskansion, valitse **Kirjaa** tai **Kirjaa ja siirrä**.
-   Jos haluat hylätä peruutuksen, poista sekkipalautusten kirjauskansio.

> [!NOTE]
> Jos poistat kirjauskansion, peruutus poistetaan järjestelmästä mutta alkuperäinen sekki säilyy **Sekki**-sivulla. Tämän jälkeen sekin tilana ei enää ole **Odottaa peruutusta**.

## <a name="results-of-posting-a-reversal"></a>Peruutuksen kirjauksen tulokset
Kun kirjaat sekin peruutuksen, tapahtuu seuraavaa:

-   Sekin tilaksi päivitetään **Peruutus**.
-   Jos **Täsmäytä**-vaihtoehto oli valittuna peruutussivulta peruutuksen aikana, sekki täsmäytetään (**Täsmäytetty**-vaihtoehto tulee valituksi), eikä sitä näy **Tilin täsmäyttäminen** -sivulla.
-   Peruutustosite kirjataan uudelleen pankkitilille, jolta sekki myönnettiin. Näin sekin summa hyvitetään pankkitilille.
-   Tosite kirjataan kirjanpitoon.
-   Muokkaustiedot päivitetään **Sekki**-sivun **Historia**-kenttäryhmään.

> [!NOTE] 
> Kun peruutat konsernin sisäiselle kauppatapahtumalle myönnetyn sekin, vastakirjaukset saadaan konsernin sisäisen laskennan asetuksista, ei alkuperäisestä tapahtumasta. Jos peruutettu sekki myönnettiin toimittajamaksulle, tapahtuu myös seuraavaa:

-   Järjestelmä poistaa käytöstä maksun, jota vasten alkuperäisen maksun lasku selvitettiin. (Tilitys peruutetaan.)
-   Maksun peruutuksen tapahtuma kirjataan toimittajan tiliä vastaan, ja peruutettu maksu selvitetään alkuperäistä maksua vastaan. Alkuperäisen toimittajan suorituksen **Viimeinen tilitystosite** -kenttä **Toimittajatapahtumat**-sivulla päivitetään vastaamaan peruutetun tapahtuman tositenumeroa.

Jos peruutettu sekki myönnettiin asiakaspalautukselle, tapahtuu myös seuraavaa:

-   Maksun peruutuksen tapahtuma kirjataan asiakastiliä vastaan, ja alkuperäisen maksun sekä alkuperäisen tiedoston välinen tilitys peruutetaan (luodaan negatiivinen maksu).
-   Maksun peruutus koskee alkuperäistä maksua. Alkuperäisen asiakkaan suorituksen **Viimeinen tilitystosite** -kenttä **Asiakastapahtumat**-sivulla päivitetään vastaamaan peruutetun tapahtuman tositenumeroa.




