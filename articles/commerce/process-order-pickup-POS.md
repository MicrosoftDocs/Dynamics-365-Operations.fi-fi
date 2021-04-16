---
title: Asiakkaan tilausten noutojen käsitteleminen myyntipisteessä
description: Tässä aiheessa kerrotaan toiminnoista, jotka ovat käytettävissä myyntipistesovelluksessa tilausten noutojen käsittelyä varten.
author: Hhainesms
ms.date: 01/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: b5c17a65a54ae88118bc5ecaa25cdadb67861129
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802764"
---
# <a name="process-customer-order-pickups-in-pos"></a>Asiakkaan tilausten noutojen käsitteleminen myyntipisteessä

[!include [banner](includes/banner.md)]

Kun [asiakastilaus](customer-orders-overview.md) luodaan myymälänoutoa varten, myymälän käyttäjä voi käynnistää varaston poiminnan myyntipistesovelluksen avulla. Myyntipiste suorittaa lopullisen maksun siepauksen tarpeen mukaan. Se myös täyttää kerätyille määrille varaston ja taloushallinnon kirjauksen.

Jos olet myymälän käyttäjä, voit suorittaa noudon joko myyntipisteen **Peruuta tilaus**- tai **Tilauksen täyttäminen** -toiminnon avulla. Jotta **Nouto**-toiminto olisi käytettävissä, sinun on ensin tehtävä jokin seuraavista vaiheista:

- Voit käyttää **Peruuta tilaus** -toimintoa hakemalla ja valitsemalla kerätyn tilauksen.
- Jos haluat käyttää **tilauksen täyttämistoimintoa**, etsi ja valitse vähintään yksi tilausrivi.

Jos valittuja tilauksia tai tilausrivejä ei ole konfiguroitu noutoon tässä myymälässä tai jos tilaus on jo kerätty kokonaan, **noutotoiminto** ei ole käytettävissä.

![Noutotoiminto](media/pickupoperation.png)

Microsoft Dynamics 365 Commercen versiossa 10.0.17 ja sitä myöhemmissä versioissa **Myyntipisteen noutotilausten käsittelyn parannettu käyttökokemus** -ominaisuus voidaan ottaa käyttöön Commerce headquarters -ohjelmassa toimintohallinnan avulla. Jos tämä toiminto on poissa käytöstä, käyttäjät eivät voi valita noutomääriä. Riville tilattu koko määrä on oletusarvoisesti noudettava määrä. Tämä kokemus voi olla ongelmallinen, koska käyttäjät voivat unohtaa valita joitakin nimikkeitä noutoa varten, kun he tekevät noudon tilauksen täyttämisen kautta.

**Myyntipisteen noutotilausten käsittelyn parannettu käyttökokemus** -ominaisuus antaa käyttäjille paremman hallinnan noudettavien tuotteiden valintaan sekä noudettavien tuotteiden määrään. Käyttäjien ei tarvitse valita kaikkia myyntitilauksen rivejä tilauksen täyttämissivulta, ennen kuin he valitsevat **Nouto**. Kaikki mahdollisesti noudettavat nimikkeet ovat näkyvissä. Käyttäjät voivat määrittää useita rivejä noutoa varten, vaikka vain yksi tuoterivi olisi valittuna.

Kun **Myyntipisteen noutotilausten käsittelyn parannettu käyttökokemus** -ominaisuus on otettu käyttöön ja **Nouto**-toiminto valitaan, näkyviin tulee **Nouto**-valintaikkuna. Siinä voit valita noudettavat nimikkeet ja määrät. Oletusarvon mukaan kaikki tilattu määrä, jonka varasto on kerätyssä tai pakatussa tilassa, katsotaan olevan sopiva noutoon. Oletusarvon mukaan tämä määrä määritetään noutomääräksi. Voit muuttaa syötettyä määrää, jos määrän arvo ei ole nolla eikä se ylitä valitun rivin avointa (ei-laskutettua) kokonaismäärää.

![Nouto-valintaikkuna](media/pickupselect.png)

Kun olet valinnut noudettavat määrät ja valinnut sitten **Nouto**, esiin tulee tapahtumasivu. Jos [monikanavamaksut](omni-channel-payments.md)-ominaisuus on otettu käyttöön ja tiedostossa on ennalta hyväksyttyjä luottokorttimaksuja, maksu on kohdistettava.

Tapahtumasivulla järjestelmä laskee erääntyvät summat laskemalla valittujen noutonimikkeiden erääntymissumman ja vähentämällä sitten aiemmin maksetut talletukset tai hyväksytyt luottokorttimaksut. Sinun on käsiteltävä maksu noutotapahtuman viimeistelemiseksi. Jos tapahtumasivun [näyttöasettelu](pos-screen-layouts.md) on määritetty siten, että se sisältää **Päätä tapahtuma** -työvaiheen eikä summaa eräänny, voit suorittaa tapahtuman valitsematta maksutapaa. Jos **Päätä tapahtuma** -toiminto ei ole käytettävissä, voit valita **Summat**-ruudusta **Maksettavaa 0,00 $** -linkin, jos haluat päättää tapahtuman valitsematta maksutapaa.

![Asiakkaan tilauksen noutotapahtuman tapahtumasivu](media/pickupcart.png)

## <a name="changing-pickup-lines-or-quantities"></a>Noutorivien tai -määrien muuttaminen

Jos noutomäärää on muutettava sen jälkeen, kun noudettavat nimikkeet on valittu, voit valita **Määritä määrä**. Et voi asettaa noutomääräksi **0** (nolla) tai kasvattaa sitä arvoon, joka ylittää tilatulle riville jäävän laskuttattoman määrän. Jos haluat poistaa noutorivin tapahtuman ostoskorista, valitse **Mitätöi tapahtuma**. Nykyinen tapahtuma pysäytetään ja **Nouto**-toiminnon työnkulku käynnistyy uudelleen.

**Myyntipisteen noutotilausten käsittelyn parannettu käyttökokemus** -ominaisuus on otettu käyttöön, organisaatiot voivat lisätä **Muuta noutorivejä** -toiminnolle painikkeen tapahtumasivun näyttöasetteluun. Kun olet luonut noutotapahtuman ostoskorin myyntipisteessä ja valinnut nimikkeet, voit valita **Muuta noutorivejä**, jos sinun on muutettava noutonimikkeitä, mutta et halua mitätöidä koko tapahtumaa. Näyttöön tulevassa **Muuta noutorivejä** -valintaikkunassa voit muuttaa noutonimikkeitä ja -määriä. Tapahtuman ostoskori päivitetään vastaamaan muutoksiasi.

![Muuta noutonimikkeitä -valintaikkuna](media/pickupchange.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]