---
title: Puhelinkeskusten maksutavat
description: Tässä artikkelissa käsitellään Dynamics 365 Commercen puhelinkeskuksessa käytettäviä maksutapoja.
author: josaw1
ms.date: 03/28/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCRSalesTableOrderHistory, MCRCCAuthManagement
audience: Application User
ms.reviewer: josaw
ms.custom: 92163
ms.assetid: 8e738907-870b-466c-ab0c-07f4a4aa47f3
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 7f47b6865f408a1dc833dcf15fc254ef8b802bcc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902708"
---
# <a name="payment-methods-in-call-centers"></a>Puhelinkeskusten maksutavat

[!include [banner](includes/banner.md)]

Puhelinkeskuskanavan määritys Dynamics 365 Commercessa sisältää **Ota käyttöön tilausten viimeistely** -asetuksen. Tämän asetuksen avulla voidaan varmistaa, että kaikki kanavan käyttäjien luomat tilaukset vapautetaan tilaustenkäsittelyyn vain, jos ne on maksettu ennakkoon tai jos esihyväksytty maksu on hyväksyttyjen toleranssien mukainen. Jos **Ota käyttöön tilausten viimeistely** -asetus on otettu käyttöön, puhelinkeskuksen käyttäjät voivat kirjata maksuja asiakkaiden myyntitilauksille käyttämällä puhelinkeskuksen maksujen käsittelyominaisuuksia. Jos asetus poistetaan käytöstä, puhelinkeskuksen käyttäjät ei voi käyttää puhelinkeskuksen maksujen käsittelyominaisuuksia. He voivat kuitenkin käyttää myyntitilauksissa esimaksuja käyttämällä oletusarvoista myyntireskontratoimintoa.

Yritys voi määrittää kanavamäärityksen osana puhelinkeskuskanavassa sallitut maksutavat. Puhelinkeskuskanava käyttää niitä maksutapoja, jotka on määritetty myymäläkanaville.

Voit määrittää puhelinkeskuksen maksutavan valitsemalla ensin **Retail ja Commerce** \> **Kanavat** \> **Puhelinkeskukset** \> **Kaikki puhelinkeskukset** ja sitten **Asetukset**-valikossa **Maksutavat**-vaihtoehto.

Voit määrittää maksutapaa luodessasi viisi maksutapatoimintoa.

| Toiminto            | kuvaus |
|---------------------|-------------|
| Normaali              | Käytä maksutapana **Normaali**-toimintoa, kun määritä maksutavaksi esimerkiksi käteisen tai tositteet. Kun nämä maksutyypit kohdistetaan myyntitilaukseen puhelinkeskuksessa, **Ennakkomaksu**-merkinnäksi tulee oletusarvoinen **Kyllä**. Tällä tavoin ennakkomaksutosite kirjataan heti asiakkaan tilille, kun tilaus on lähetetty. Käyttäjät voivat halutessaan muuttaa **Ennakkomaksu**-merkinnän arvoksi **Ei**, jolloin maksutositetta ei luoda ennen laskun kirjausta. Ennakkomaksutosite kirjataan asiakkaan tapahtumahistoriaan, jossa se täsmäytetään järjestelmällisesti myyntitilauksen laskuun. |
| Tarkistus               | Käytä **Sekki**-toimintoa, kun haluat määrittää sekkimaksuvälineen maksutavaksi. Kun tätä maksutapaa käytetään myyntitilauksessa, käyttäjän on kirjattava asiakkaan sekin numero maksun kohdistuksen käsittelyn osana. Sekkimaksut käsitellään aina ennakkomaksuina, kun ne kohdistetaan ja maksutositteet luodaan heti tilauksen lähetyksen yhteydessä. Nämä ennakkomaksutositteet täsmäytetään järjestelmällisesti tilaukselle luotuihin laskuihin. |
| Kortit               | Korttimaksutavat ovat kaikki maksutavat, jotka edellyttävät asiakkaan maksukortissa määritetyn kortin numeron kirjaamista. Tällaisia ovat esimerkiksi luotto- ja lahjakortit. Kun määrität tällaisia maksutyyppejä, tähän maksutapaan liitettävät korttitunnukset on määritettävä **Korttiasetukset**-valikossa. Käyttäjät voivat ilmoittaa tilaustenkäsittelyn yhteydessä, onko korttimaksu ennakkomaksu. He voivat tehdä sen käyttämällä maksumerkintäsivun **Ennakkomaksu**-vaihtoehtoa. Ellei yritys edellytä ennakkomaksuja, oikea luottokorttimaksu käsitellään yleensä kahdessa vaiheessa, jossa valtuutus saadaan tilaustenkäsittelyn aikana. Maksu puolestaan täsmäytetään ja kerätään asiakkaan kortilta laskutuksen yhteydessä. Lahjakortteille suositellaan ennakkomaksua, koska lahjakortin saldo pitäisi vähentää heti, jota asiakas ei voi käyttää samaa arvoa muualla. |
| Asiakas            | Maksutavan **Asiakas**-toiminto viittaa siihen, että maksu kohdistetaan asiakkaan luottokorttirajaan tai asetetaan ennakkomaksuksi. Commercessa asiakkaalle voidaan määrittää luottoraja, joka voidaan tarkistaa tilaustenkäsittelyn aikana. **Asiakas**-toimintoon linkitetyllä maksutavalla tehtävät maksut luovat asiakastiliä koskevan velan. Kun myyntitilaus sitten laskutetaan, erääntyvä saldo näytetään. Näissä tilanteissa asiakkaat lähettävät yleensä maksun annettujen ehtojen mukaisesti. Vaihtoehtoisesti erääntyvä saldo voidaan täsmäyttää kohdistamalla asiakastilin edellinen avoin hyvityksen tosite. Huomaa, että vaikka määrität tämän maksutavan, se ei näy puhelinkeskuksen tilaustenkäsittelyn maksuvalintavaihtoehdoissa, ellei **Salli ennakkomaksu** -merkintää ole määritetty käsiteltävän asiakkaan asiakastietueessa. Tämä merkintä on asiakastietueen **Oletusmaksut**-välilehdessä. |
| Maksuvälineen poisto tai vaihtokassa | Puhelinkeskus ei käytä **Maksuvälineen poisto tai vaihtokassa** -toimintoa. Sitä käytetään vain, kun määritä maksutavan, jota myyntipistesovellus käyttää myymäläkanavassa. |

Määritettävät maksutavat on linkitettävä kirjanpitoon tai pankkitiliin. Jos ohitat tämän vaiheen, käyttäjät vastaanottavat virheen, kun he yrittävät tallentaa maksutyypin.

## <a name="refund-payment-methods"></a>Palautuksen maksutavat

Palautuksen käsittelyskenaarioissa puhelinkeskus käyttää myös joitakin myyntireskontrassa määritettyjä maksutapoja. Voit määrittää maksutavat valitsemalla **Retail ja Commerce** \> **Kanavan asetukset** \> **Puhelinkeskuksen asetukset** \> **Puhelinkeskuksen palautusmenetelmät**. Tämä määritys on tehtävä, jotta palautussekit asiakkaille voidaan käsitellä. Jos asiakas maksoi tilauksen alun perin käteisellä tai sekillä, käyttäjä haluaa ehkä lähettää asiakkaalle palautusekin myyntireskontran kautta. Tässä tapauksessa puhelinkeskuksen käteis- ja sekkimaksutyypit on yhdistettävä oikeaan maksutapaan myyntireskontrassa, jotta palautuksen oikea käsittely voidaan varmistaa.

Jos käyttäjä lisäksi käsittelee palautustilauksen puhelinkeskuksen käyttäjänä Commercessa mutta hän ei voi linkittää palautusta alkuperäiseen myyntiin, **Palautus**-maksutapa on määritettävä puhelinkeskuksen parametreissa. Valitse **Retail ja Commerce** \> **Kanavan asetukset** \> **Puhelinkeskuksen asetukset** \> **Puhelinkeskuksen parametrit** ja varmista sitten **Palautus**-välilehden **Maksutapa**-kentässä, että maksutapa on määritetty. Maksutapa on palautuksille käytettävä maksutapa. Yleensä se määritetään joko sekki- tai asiakastilitapana.


[!INCLUDE[footer-include](../includes/footer-banner.md)]