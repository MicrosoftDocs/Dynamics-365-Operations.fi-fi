---
title: Sähköisen raportoinnin toimittajan mallisekit
description: Tässä ohjeaiheessa on yleisiä tietoja sähköisen raportoinnin mallisekkimuotojen käyttämisestä.
author: ShylaThompson
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: ae42c9012a430aeeed6adb78b33776c727e4a3f8
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551146"
---
[!include [banner](../includes/banner.md)]

# <a name="electronic-reporting-sample-vendor-checks"></a>Sähköisen raportoinnin toimittajan mallisekit

Voit muotoilla toimittajan sekkejä sähköisellä raportoinnilla. Markkinoilla on monia pankki- ja sekkipalvelukohtaisia sekkimuotoja. Sähköisen raportoinnin työkalusäilön maksun sekkimalliin sisältyy sekkimuotomalleja. Näiden mallisekkien nimet ovat **Sekki keskellä (USA)** ja **Sekki ylhäällä, kanta alapuolella (USA)**.

## <a name="what-check-formats-are-currently-supported"></a>Mitä sekkimuotoja tuetaan tällä hetkellä?

Tarkista Microsoft Dynamics Lifecycle Servicesin (LCS) jaetusta omaisuuskirjastosta luettelo tämän hetkisistä käytettävistä olevista tiedostoista, joiden tyyppi on **GER-määritys**. Seuraavassa Määritettävät asetukset -osiossa on linkki ohjeaiheeseen, jossa kerrotaan, miten luodaan LCS-säilö käytettävissä olevien määritysten tarkastelua varten ja tuodaan valitut määritykset.

Microsoft Dynamics 365 Finance sisältää mallimuodon, jossa sekki on ylimmäisenä ja sen alapuolella on kaksi maksusuoritusosaa. Siinä on myös mallimuoto, jossa sekki on keskellä kahden maksusuoritusosan välissä. Nämä mallimuodot vastaavat Deluxe-yrityssekkimuotoja.

## <a name="what-do-i-have-to-set-up"></a>Mitä asetuksia on määritettävä?

- Ennen sekkien tulostusta sähköisessä raportoinnissa ainakin yksi aktiivinen sekkimääritys on tuotava sähköisen raportoinnin määrityksiin. Ohjeet löydät artikkelista [Lataa sähköisen raportoinnin konfiguraatiot Lifecycle Servicesistä](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).
- Kun määrität pankkitilin maksuliikenteen hallinnan sekkejä, valitse ensin **Yleinen sähköinen vientimuoto** -valintaruutu ja sitten sopiva sekkimuoto vientimuotomääritykseksi.
- Määritä myös, kuinka monta luetteloriviä maksusuoritukseen tulostetaan. Muista, että otsikkorivit lasketaan mukaan tähän lukuun. Kahdessa mallisekkimuodossa suositeltava luettelorivien määrän on 17. Tämä luku kuitenkin vaihtelee sekkipaperin ja tulostinohjaimen mukaan.
- Asettelu kannattaa varmistaa tulostamalla testisekki. Tulosta sekki valitsemalla **Tulostuskoe**-vaihtoehto. Mallisekkimuodot toimivat parhaiten, kun **Reunukset**-asetukseksi on valittu Microsoft Excelin tulostimen lisäominaisuuksissa **Ei mitään**. Kun testisekki on luotu, ota Excel-tulosteen muokkaus käyttöön ja määritä sivun asettelu niin, että kaikkien reunusten asetus on **0** (nolla). Vertaa sekkien testikappaletta sekkipaperiin ja säädä asetuksia, kunnes olet tyytyväinen kohdistukseen.
- Kun luot maksukirjauskansiossa maksuja määritetyllä pankkitilille, sekit tulostetaan määritetyssä muodossa.

Lisätietoja on ohjeaiheessa [Sähköisen raportointimuodon muokkaaminen](../../dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md).
