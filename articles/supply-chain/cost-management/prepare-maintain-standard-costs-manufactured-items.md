---
title: Valmistettujen nimikkeiden standardikustannusten ylläpitämisen valmistelutoimet
description: Tässä ohjeaiheessa käsitellään valmistettujen nimikkeiden ylläpitokustannusten valmisteluvaiheita.
author: AndersGirke
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec68e1efc261920dc8f08ed602836b1939511dfce01008c093af7916ecd71618
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6734328"
---
# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a>Valmistettujen nimikkeiden standardikustannusten ylläpitämisen valmistelutoimet

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään valmistettujen nimikkeiden ylläpitokustannusten valmisteluvaiheita. Valmistettujen nimikkeiden vaiheet vaihtelevat hieman ostettujen nimikkeiden vaiheista.

Valmistettuihin nimikkeisiin määritetyt menettelytavat voivat vaikuttaa valmistettujen päänimikkeiden kustannusten laskentaan. Valmistele valmistettujen nimikkeiden ylläpitokustannukset seuraavien vaiheiden mukaisesti.

1. Määritä nimikemalliryhmä valmistettuun nimikkeeseen. 

   Nimikemalliryhmä määrittää, että käytetään standardikustannuksia.

2. Määritä nimikeryhmä valmistettuun nimikkeeseen. 

   Nimikeryhmä sisältää valmistettua nimikettä koskevia kirjanpitotilejä. Standardikustannusvarastomallia käyttävän valmistetun nimikkeen kirjanpitotileissä on mukana useita tuotantovariansseja, kustannuksen muutoksen varianssi ja varastokustannuksen uudelleenarvostus.

3. Määritä varaston mittayksikkö nimikkeeseen. 

   Nimikkeen kustannukset ilmoitetaan aina nimikkeen varaston mittayksiköinä.

4. Älä määritä kustannusryhmään valmistettuun nimikkeeseen, ellei nimikettä käsitellä ostettuna nimikkeenä.

5. Määritä tuoterakenteen laskentaryhmä valmistettuun nimikkeeseen. 

   Nimikkeen tuoterakenteen laskentaryhmä määrittää sovellettavat varoitusehdot. Tällä tavoin tuoterakenteen laskennan valmistumisen jälkeen voidaan muodostaa varoitussanomia mahdollista laskentavirheiden lähteistä. Varoitussanoma voi esimerkiksi ilmoittaa, että valittua tuoterakennetta tai reittiä ei ole. Tuoterakenteen laskentaryhmä sisältää hajotuksen lopettamisen menettelytavan, joka määrittää, milloin valmistettua nimikettä on käsiteltävä ostettuna nimikkeenä.

6. Jos valmistetulla nimikkeellä on vakiokustannukset, määritä sille vakiotilausmäärä. 

   Vakiotilausmäärä on kirjanpidon eräkoko vakiokustannusten kuolettamisessa. Esimerkkejä vakiokustannuksista ovat reititystyövaiheiden määritysajat ja tuoterakenteen komponenttien vakiomäärä.

7. Määritä valmistetun nimikkeen tuoterakenne. 

   Valmistetulle nimikkeelle voi määrittää tuoterakenneversioita. Varmista, että haluamasi versiot on merkitty hyväksytyiksi ja aktiivisiksi ja että niillä on haluamasi voimaantulopäivät. Tuoterakenneversio voi olla koko yrityksen laajuinen tai toimipaikkakohtainen.

8. Määritä valmistetun nimikkeen reititys. 

   Valmistetulle nimikkeelle voi määrittää reititysversioita. Varmista, että haluamasi versiot on merkitty hyväksytyiksi ja aktiivisiksi ja että niillä on haluamasi voimaantulopäivät. Reititysversion täytyy olla toimipaikkakohtainen.

Jos haluat käyttää reititystietoja kustannuslaskelmissa, valmisteluun tarvitaan lisävaiheita. Esimerkiksi reitityksen työvaiheisiin määritettävien kustannusluokkien täytyy olla oikeita ja valmiita.

## <a name="related-topics"></a>Liittyvät aiheet

[Valmistetun nimikkeen vakiokustannusten kuolettaminen](amortize-constant-costs-manufactured-item.md)

[Tuotettavissa tai hankittavissa olevien tuotteiden määrittäminen](manufactured-items-treated-as-purchased-items.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]