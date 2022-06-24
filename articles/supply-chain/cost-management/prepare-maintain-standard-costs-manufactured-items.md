---
title: Valmistettujen nimikkeiden standardikustannusten ylläpitämisen valmistelutoimet
description: Tässä artikkelissa käsitellään valmistettujen nimikkeiden ylläpitokustannusten valmisteluvaiheita.
author: JennySong-SH
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
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 423da8022faf8066c5aa524c49c5071d0871de04
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886012"
---
# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a>Valmistettujen nimikkeiden standardikustannusten ylläpitämisen valmistelutoimet

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään valmistettujen nimikkeiden ylläpitokustannusten valmisteluvaiheita. Valmistettujen nimikkeiden vaiheet vaihtelevat hieman ostettujen nimikkeiden vaiheista.

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

## <a name="related-articles"></a>Liittyvät artikkelit

[Valmistetun nimikkeen vakiokustannusten kuolettaminen](amortize-constant-costs-manufactured-item.md)

[Tuotettavissa tai hankittavissa olevien tuotteiden määrittäminen](manufactured-items-treated-as-purchased-items.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]