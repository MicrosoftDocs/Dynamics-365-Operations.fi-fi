---
title: Tuotantotilausten ilmoittaminen valmiiksi
description: "Valmiiksi ilmoittaminen tapahtuu tuotantovaiheessa. Tässä vaiheessa valmis tuote raportoidaan ja siirretään tuotantotilauksesta varastoon."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f8adcbcc2157058151c26179eb2eb925b0092d2d
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="report-production-orders-as-finished"></a>Tuotantotilausten ilmoittaminen valmiiksi

[!include[banner](../includes/banner.md)]


Valmiiksi ilmoittaminen tapahtuu tuotantovaiheessa. Tässä vaiheessa valmis tuote raportoidaan ja siirretään tuotantotilauksesta varastoon.

Kun tuotantotilaukseen kuuluvien valmiiden tavaroiden määrä ilmoitetaan valmiiksi, ne päivitetään käytettäviksi varastossa. Osittainen määrä alunperin suunnitellusta tilausmäärästä voidaan ilmoittaa valmiiksi. Määrien valmiiksi ilmoittamisen yhteydessä on myös mahdollista ilmoittaa virhemäärät liittyvällä virhesyyllä. Kun tuotantotilauksen tilaksi päivitetään Ilmoitettu valmiiksi, tuotantotilaukselle ei raportoida enempää määriä.
Myös seuraavat ominaisuudet liittyvät **Ilmoitettu valmiiksi** -prosessiin:
-   Voit määrittää raaka-aineiden ja ajan kulutuksen suhteessa ilmoitettuun määrään (jälkipoisto)
-   Nimikkeille, joiden käyttö on mahdollista varastoinnin prosesseissa, voi luoda poispanotyöt.
-   Valmiiden tavaroiden suunnitellun tai vakiokustannusarvon voi määrittää raportoitavaksi kirjanpitotileille.
-   Ilmoitetulle määrälle voidaan luoda laatutilaus, laatuliitoksen määritykseen perustuen.

Määrä ilmoitetaan tuotossijaintiin. Sen jälkeen luodaan varastotyön, jossa määrä siirretään tuotossijainnista lopulliseen kohteeseen, joka määritellään poispanotyön sijaintidirektiivissä.

-   Laatutilauksen voi luoda, kun tuotantotilaus ilmoitetaan valmiiksi, jos sille on asetettu laatuliitos.

## <a name="set-a-production-order-to-reporting-as-finished"></a>Tuotantotilauksen asettaminen Ilmoitettu valmiiksi -tilaan
Voit asettaa tuotantotilauksen tilaksi **Ilmoitettu valmiiksi** normaalin tuotantotilauksen päivitystoiminnon avulla, reititys- ja työkorttikirjauskansioiden avulla tai **Ilmoita valmiiksi** -kirjauskansion avulla. Voit myös päivittää vaiheen **Ilmoitettu valmiiksi** -tilaan työkortinpäätteen ja työkorttilaitteen sivuilta, kun ilmoitat tuotantotilauksen viimeisen työn tiedot. Viimeiseksi, voit ottaa **Ilmoita valmiiksi** -asetuksen käyttöön prosessina varaston käsipäätelaiteratkaisulle.  




