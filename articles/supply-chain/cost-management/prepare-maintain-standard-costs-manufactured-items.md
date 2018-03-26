---
title: "Valmistettujen nimikkeiden standardikustannusten ylläpitämisen valmistelutoimet"
description: "Tässä ohjeaiheessa käsitellään valmistettujen nimikkeiden ylläpitokustannusten valmisteluvaiheita."
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: c1942d1f2c8eeb05a6cbaddd2d7911a93b7e05a1
ms.contentlocale: fi-fi
ms.lasthandoff: 03/07/2018

---


# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a>Valmistettujen nimikkeiden standardikustannusten ylläpitämisen valmistelutoimet

[!include[banner](../includes/banner.md)]

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

<a name="related-topics"></a>Liittyvät aiheet
--------

[Valmistetun nimikkeen vakiokustannusten kuolettaminen](amortize-constant-costs-manufactured-item.md)

[Tuotettavissa tai hankittavissa olevien tuotteiden määrittäminen](manufactured-items-treated-as-purchased-items.md)


