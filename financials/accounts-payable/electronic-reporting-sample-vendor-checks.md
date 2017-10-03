---
title: "Sähköisen raportoinnin toimittajan mallisekit"
description: "Tässä ohjeaiheessa on yleisiä tietoja sähköisen raportoinnin mallisekkimuotojen käyttämisestä."
author: twheeloc
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.assetid: 
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: a8ba439ff643fce4811be9224a3edf96b2b9025c
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---

[!include[banner](../includes/banner.md)]

# <a name="electronic-reporting-sample-check-formats"></a>Sähköisen raportoinnin mallisekkimuodot

Voit muotoilla toimittajan sekkejä sähköisellä raportoinnilla. Markkinoilla on monia pankki- ja sekkipalvelukohtaisia sekkimuotoja. Sähköisen raportoinnin työkalusäilön maksun sekkimalliin sisältyy sekkimuotomalleja. Näiden mallisekkien nimet ovat **Sekki keskellä (USA)** ja **Sekki ylhäällä, kanta alapuolella (USA)**.

## <a name="what-check-formats-are-currently-supported"></a>Mitä sekkimuotoja tuetaan tällä hetkellä?

Tarkista Microsoft Dynamics Lifecycle Servicesin (LCS) jaetusta omaisuuskirjastosta luettelo tämän hetkisistä käytettävistä olevista tiedostoista, joiden tyyppi on **GER-määritys**. Seuraavassa Määritettävät asetukset -osiossa on linkki ohjeaiheeseen, jossa kerrotaan, miten luodaan LCS-säilö käytettävissä olevien määritysten tarkastelua varten ja tuodaan valitut määritykset.

Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition sisältää mallimuodon, jossa sekki on ensin ylhäällä ja sitten seuraavana on kaksi maksusuoritusosaa. Siinä on myös mallimuoto, jossa sekki on keskellä kahden maksusuoritusosan välissä. Nämä mallimuodot vastaavat Deluxe-yrityssekkimuotoja.

## <a name="what-do-i-have-to-set-up"></a>Mitä asetuksia on määritettävä?

- Ennen sekkien tulostusta sähköisessä raportoinnissa ainakin yksi aktiivinen sekkimääritys on tuotava sähköisen raportoinnin määrityksiin. Ohjeet löydät artikkelista [Lataa sähköisen raportoinnin konfiguraatiot Lifecycle Servicesistä](/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).
- Kun määrität pankkitilin maksuliikenteen hallinnan sekkejä, valitse ensin **Yleinen sähköinen vientimuoto** -valintaruutu ja sitten sopiva sekkimuoto vientimuotomääritykseksi.
- Määritä myös, kuinka monta luetteloriviä maksusuoritukseen tulostetaan. Muista, että otsikkorivit lasketaan mukaan tähän lukuun. Kahdessa mallisekkimuodossa suositeltava luettelorivien määrän on 17. Tämä luku kuitenkin vaihtelee sekkipaperin ja tulostinohjaimen mukaan.
- Asettelu kannattaa varmistaa tulostamalla testisekki. Tulosta sekki valitsemalla **Tulostuskoe**-vaihtoehto. Mallisekkimuodot toimivat parhaiten, kun **Reunukset**-asetukseksi on valittu Microsoft Excelin tulostimen lisäominaisuuksissa **Ei mitään**. Kun testisekki on luotu, ota Excel-tulosteen muokkaus käyttöön ja määritä sivun asettelu niin, että kaikkien reunusten asetus on **0** (nolla). Vertaa sekkien testikappaletta sekkipaperiin ja säädä asetuksia, kunnes olet tyytyväinen kohdistukseen.
- Kun luot maksukirjauskansiossa maksuja määritetyllä pankkitilille, sekit tulostetaan määritetyssä muodossa.

Lisätietoja on ohjeaiheessa [Sähköisen raportointimuodon muokkaaminen](/dynamics365/unified-operations/dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template).

