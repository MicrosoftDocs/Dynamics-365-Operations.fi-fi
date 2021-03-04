---
title: Varastosovelluksen tapahtumat
description: Tässä ohjeaiheessa käsitellään varastosovelluksen tapahtumasanomien käsittelyssä erätyön osana käytettyä varastosovelluksen tapahtumien käsittelyä.
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 210008c4a1366773f465c59b38eca30f11f0b38c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426934"
---
# <a name="warehouse-app-event-processing"></a>Varastosovelluksen tapahtumakäsittely

[!include [banner](../includes/banner.md)]

Supply Chain Managementissa suoritettavat erätyöt voivat käyttää tapahtumien käsittelyjonon varastosovelluksen määrittämiä tietoja, jotta ilmoitettuihin tapahtumiin voidaan reagoida tarvittaessa. Tämä toiminto lisää liittyvät tapahtumat jonoon vastauksena sovellusta käyttävien työtekijöiden tekemiin tietyn tyyppisiin toimintoihin. Esimerkiksi käytettäessä **Luo ja käsittele siirtotilauksia varastosovelluksessa** -toimintoa siirtotilauksen otsikko ja rivit luodaan ja päivitetään taustalla, kun järjestelmä suorittaa **Käsittele varastosovelluksen tapahtumia** -erätyön.

## <a name="enable-the-process-warehouse-app-events-feature"></a>Käsittele varastosovelluksen tapahtumia -toiminnon ottaminen käyttöön

Ennen kuin käytät tätä toimintoa, se on otettava käyttöön järjestelmässä. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sivua ja tarkistaa toiminnon tilan sekä ottaa sen käyttöön tarvittaessa. Käsittele varastosovelluksen tapahtumia -toiminnossa on seuraavat osat:

- **Moduuli** - Varastonhallinta
- **Toiminnon nimi** – Käsittele varastosovelluksen tapahtumia

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Erätyön määrittäminen käsittelemään varastosovelluksen tapahtumia

### <a name="process-warehouse-app-events"></a>Käsittele varastosovelluksen tapahtumat

Määritä aikataulutettu erätyö käsittelemään siirtotilausten luonti-ja rivipäivitysten varastosovelluksen tapahtumat.

1. Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Käsittele varastosovelluksen tapahtumat**.
1. Käsittele varastosovelluksen tapahtumat -valintaikkuna avautuu. Laajenna **Suorita taustalla** -pikavälilehti ja määritä **Erän käsittely** -arvoksi **Kyllä**.
1. Valitse **Suorita taustalla** -pikavälilehdessä **Toistuminen**.
1. **Määritä toistuminen** -valintaikkuna aukeaa. Määritä yritykselle ajon aikataulu tarvittaessa.
1. Palaa **Käsittele varastosovelluksen tapahtumat** -valintaikkunaan valitsemalla **OK**.
1. Lisää erätyö eräajoon valitsemalla **OK** **Käsittele varastosovelluksen tapahtumat** -valintaikkunassa.

## <a name="query-warehouse-app-events"></a>Varastosovelluksen tapahtumakyselyt

Voit näyttää varastosovelluksen luoman tapahtumajonon ja tapahtumasanomat valitsemalla **Varastonhallinta \> Kyselyt ja raportit \> Mobiililaitteen lokit \> Varastosovelluksen tapahtumat**.

## <a name="the-standard-event-queue-process"></a>Tapahtuman vakiojonoprosessi

Varastosovellusten tapahtumajonoa käytetään yleensä seuraavaksi käsitellyn työnkulun kanssa:

1. Tapahtuma lisätään jonoon tapahtumasanoman avulla. Uuden sanoman tapahtuman tila on aluksi **Odottaa**, jolloin **Käsittele varastosovelluksen tapahtumat** -erätyö ei poimi ja käsittele tätä sanomaa.
1. Heti kun sanoman tilaksi päivitetään **Asetettu jonoon**, **Käsittele varastosovelluksen tapahtumat** -erätyö poimii ja käsittelee tapahtuman.
1. Erätyö päivittää tapahtuman tilaksi joko **Valmis** tai **Epäonnistui** sen mukaan, oliko pyydetty prosessi mahdollinen.
1. Kun kaikkien liittyvien tapahtumasanomien tila on **Valmis**, tapahtuma poistetaan jonosta.

 Yksityiskohtainen esimerkki on kohdassa [Siirtotilauksen luonti varastosovellusprosessissa](create-transfer-order-from-warehouse-app.md).

## <a name="handle-event-errors"></a>Tapahtumavirheiden käsitteleminen

Varastotapahtuman käsittelyn osana pyydetty sanomatehtävä ei ehkä vastaanota prosesseja erätyöstä. Siinä tapauksessa tapahtumasanoman tilaksi muuttuu **Epäonnistui**. **Eräloki**-tietojen avulla saadaan tietoja, miksi jokin toiminto on tehtävä ongelman korjaamiseksi.

Yksityiskohtainen esimerkki on kohdassa [Siirtotilauksen luonti varastosovelluksessa](create-transfer-order-from-warehouse-app.md).

Epäonnistuneen varastosovelluksen tapahtumasanoman nollaaminen:

1. Valitse **Varastonhallinta \> Kyselyt ja raportit \> Mobiililaitteen loki \> Varastosovelluksen tapahtumat**.
1. Etsi ja valitse **Varastosovelluksen tapahtumasanomat** -pikavälilehdessä liittyvä tapahtuma, jonka **Tapahtuman tila** -sarakkeessa näkyy **Epäonnistui**.
1. Valitse **Palauta** **Varastosovelluksen tapahtumasanomat** -työkalurivillä.
1. Jatka työskentelyä, kunnes kaikki liittyvät sanomat on palautettu.

Voit poistaa **Epäonnistui**-tapahtumasanoman myös käyttämällä **Varastosovelluksen tapahtumasanomat** -työkalurivin **Poista**-vaihtoehtoa.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]