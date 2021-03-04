---
title: Jaksotuksien yleiskuvaus
description: Tässä artikkelissa esitellään jaksotukset ja annetaan tietoja niiden määrittämisestä ja tapahtumien luomisesta.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b97055f7eac12e3e82d028a0097ca926e5c355a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442729"
---
# <a name="accruals-overview"></a>Jaksotuksien yleiskuvaus

[!include [banner](../includes/banner.md)]

Tässä artikkelissa esitellään jaksotukset ja annetaan tietoja niiden määrittämisestä ja tapahtumien luomisesta.

Jaksotuksia käytetään jaksotuskirjanpidossa seuraamaan tuottoa, joka todetaan kaudella, jolla se on ansaittu, eikä silloin kun maksu vastaanotetaan, sekä seuraamaan kuluja (kustannuksina), jotka kirjataan kun niitä esiintyy, eikä silloin kun maksu suoritetaan.

## <a name="accrual-schemes"></a>Jaksotusmallit
Jaksotusmalleja käytetään määrittämään laskennalliset tuotot ja kustannukset, ja samaa jaksotusmallia voidaan käyttää sekä tuottoihin että kustannuksiin. Kirjanpidon jaksotukset jakavat kirjauskansiorivin tuotot niin, että tuotot ja kustannukset kirjataan oikeille kausille. **Jaksotusmalli** -sivulla voit määrittää debit- ja kredit-tilit, joita käytetään kun jaksotusmalli on käytössä.

-   **Veloitus** – Määrittämäsi päätili korvaa veloituksen päätilin kirjauskansion tositerivillä. Tätä tiliä käytetään myös lykkäyksen peruuttamiseen, perustuen kirjanpidon jaksotustapahtumiin.
-   **Luotto** – Määrittämäsi päätili korvaa luoton päätilin kirjauskansion tositerivillä. Tätä tiliä käytetään myös lykkäyksen peruuttamiseen, perustuen kirjanpidon jaksotustapahtumiin.

Kun olet määrittänyt, mitä tilejä käytetään, voit määrittää kuinka tositenumero luodaan jaksotustapahtumien luonnin yhteydessä. Voit myös määrittää, kuinka usein tapahtumat tapahtuvat, kuinka monta kertaa tapahtumia luodaan ja milloin tapahtumat kirjataan. Jaksotusmallin luomisen jälkeen voit käyttää sitä tietyissä kirjauskansioissa käyttämällä Kirjanpidon jaksotus -toimintoa.

## <a name="ledger-accruals"></a>Kirjanpidon jaksotukset
Kirjauskansiota syötettäessä napsauta **Kirjanpidon jaksotukset** **Toiminnot**-valikossa. Tämän jälkeen valitessasi jaksotusmallin näet kirjauskansion perustemäärän, jota ulottuu kauden yli, jaksotusmallin määräämästi. Esimerkiksi, jos maksat työntekijän vakuutuksen koko vuodeksi tammikuussa ja maksettava summa on 12 000 euroa, sinun on tunnistettava tämä kulu kuukausittain. Voit valita alkamispäivämäärän. Voit myös määrittää perustuuko jaksotettava summa tiliin vai vastatiliin. Kun olet tehnyt valintasi, valitse **Tapahtumat** tarkastellaksesi kaikkia tapahtumia, jotka on luotu jaksotusmallin perusteella. Esimerkiksi jos jaat 12 000 euron vakuutuksen kulut koko vuodelle näet 1 000 joka kuukausi. Kun olet kirjannut päiväkirjan, voit tarkastella tapahtumia käyttämällä **Tositetapahtumat** -kyselysivulla. Jos jaksotusmallia ei voida käyttää (esimerkiksi kun on kyse myyntitilauksen laskusta tai ostotilauksen laskusta), voit kirjata ennakkoon maksetun summan kreditiin ja kulusumman debetiin. Voit valita **Vastatilin** kun käytät jaksotusmallia.


Lisätietoja on ohjeaiheissa [Jaksotusmallien luominen](tasks/create-accrual-schemes.md) ja [Kirjanpidon jaksotustapahtumien luominen](tasks/create-ledger-accrual-transactions.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]