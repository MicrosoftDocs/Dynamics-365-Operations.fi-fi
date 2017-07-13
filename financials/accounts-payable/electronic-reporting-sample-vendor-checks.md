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
ms.search.scope: Operations, Core
ms.assetid: 
ms.search.region: Global
ms.author: twheeloc
ms.dyn365.intro: 2017-06-30
ms.dyn365.version: Enterprise edition, July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 6cb473962f40ed9ef2f5f807f089098764f47009
ms.openlocfilehash: 8228690ee5ab7839ec19c307c23f9b6150006371
ms.contentlocale: fi-fi
ms.lasthandoff: 06/14/2017


---

[!include[banner](../includes/banner.md)]

# Sähköisen raportoinnin mallisekkimuodot
<a id="electronic-reporting-sample-check-formats" class="xliff"></a>

Voit muotoilla toimittajan sekkejä sähköisellä raportoinnilla. Markkinoilla on monia pankki- ja sekkipalvelukohtaisia sekkimuotoja. Sähköisen raportoinnin työkalusäilön maksun sekkimalliin sisältyy sekkimuotomalleja. Näiden mallisekkien nimet ovat **Sekki keskellä (USA)** ja **Sekki ylhäällä, kanta alapuolella (USA)**.

## Mitä sekkimuotoja tuetaan tällä hetkellä?
<a id="what-check-formats-are-currently-supported" class="xliff"></a>

Tarkista Microsoft Dynamics Lifecycle Servicesin (LCS) jaetusta omaisuuskirjastosta luettelo tämän hetkisistä käytettävistä olevista tiedostoista, joiden tyyppi on **GER-määritys**. Seuraavassa Määritettävät asetukset -osiossa on linkki ohjeaiheeseen, jossa kerrotaan, miten luodaan LCS-säilö käytettävissä olevien määritysten tarkastelua varten ja tuodaan valitut määritykset.

Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition sisältää mallimuodon, jossa sekki on ensin ylhäällä ja sitten seuraavana on kaksi maksusuoritusosaa. Siinä on myös mallimuoto, jossa sekki on keskellä kahden maksusuoritusosan välissä. Nämä mallimuodot vastaavat Deluxe-yrityssekkimuotoja.

## Mitä asetuksia on määritettävä?
<a id="what-do-i-have-to-set-up" class="xliff"></a>

- Ennen sekkien tulostusta sähköisessä raportoinnissa ainakin yksi aktiivinen sekkimääritys on tuotava sähköisen raportoinnin määrityksiin. Ohjeet löydät artikkelista [Lataa sähköisen raportoinnin konfiguraatiot Lifecycle Servicesistä](/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).
- Kun määrität pankkitilin maksuliikenteen hallinnan sekkejä, valitse ensin **Yleinen sähköinen vientimuoto** -valintaruutu ja sitten sopiva sekkimuoto vientimuotomääritykseksi.
- Määritä myös, kuinka monta luetteloriviä maksusuoritukseen tulostetaan. Muista, että otsikkorivit lasketaan mukaan tähän lukuun. Kahdessa mallisekkimuodossa suositeltava luettelorivien määrän on 17. Tämä luku kuitenkin vaihtelee sekkipaperin ja tulostinohjaimen mukaan.
- Asettelu kannattaa varmistaa tulostamalla testisekki. Tulosta sekki valitsemalla **Tulostuskoe**-vaihtoehto. Mallisekkimuodot toimivat parhaiten, kun **Reunukset**-asetukseksi on valittu Microsoft Excelin tulostimen lisäominaisuuksissa **Ei mitään**. Kun testisekki on luotu, ota Excel-tulosteen muokkaus käyttöön ja määritä sivun asettelu niin, että kaikkien reunusten asetus on **0** (nolla). Vertaa sekkien testikappaletta sekkipaperiin ja säädä asetuksia, kunnes olet tyytyväinen kohdistukseen.
- Kun luot maksukirjauskansiossa maksuja määritetyllä pankkitilille, sekit tulostetaan määritetyssä muodossa.

Lisätietoja on ohjeaiheessa [Sähköisen raportointimuodon muokkaaminen](/dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md).

