---
title: Sähköisten raportointien avulla voit määrittää ja luoda positiivisia maksutiedostoja
description: Tässä ohjeaiheessa käsitellään Positive pay -toiminnon määrittämistä käyttämällä elektronista raportointia.
author: panolte
ms.date: 03/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 43dd1a9cba1fe8df5cff26fe76af7e2957a0d6a4
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544471"
---
# <a name="set-up-positive-pay-files-by-using-electronic-reporting"></a>Sähköisten raportointien avulla voit määrittää positiivisia maksutiedostoja

Määritä positiivinen maksu sähköisen luettelon luomiseksi pankille toimitettavista sekeistä. Kun sekki esitetään pankille, pankki vertaa sitä aiemmin lähetettyyn sekkiluetteloon. Jos sekki on sama kuin luettelossa, pankki selvittää sekin. Jos sekki ei vastaa luettelon sekkiä, pankki säilyttää sekin tarkistusta varten.

## <a name="set-up-the-electronic-reporting-configuration"></a>Määritä sähköisen raportoinnin konfiguraatio

1. Valitse **Työtilat \> Sähköinen raportointi**.
2. Valitse **Microsoft**-määrityspalveluntarjoajan ruudusta **Arkistot**.
3. Valitse **Yleinen** ja valitse sitten **Avaa**.
4. Jos tietovarastoon on oltava yhteys, valitse sininen linkki valintaikkunasta.
5. Etsi ja valitse konfigurointiluettelosta **Positiivisen maksumallin \> positiivinen maksumuoto**.
6. Valitse **Versiot**-pikavälilehdellä valitun uusin versio ja valitse sitten **Tuo**.

## <a name="set-up-a-positive-pay-format"></a>Positive pay -muodon määrittäminen

1. Valitse **Maksuliikenteen hallinta \> Asetukset \> Positiiviset maksumuodot**.
2. Valitse **Uusi**.
3. Määritä **Maksun muoto**- ja **Kuvaus**-kentät.
4. Valitse **Yleinen sähköinen vientimuoto** -valintaruutu.
5. Aseta **Vientimuodon määritys** -kentän arvoksi **Positiivinen maksumuoto**.

## <a name="assign-a-positive-pay-format-to-a-bank-account"></a>Positive pay -muodon määrittäminen pankkitileille

1. Valitse **Maksuliikenteen hallinta \> Pankin tilit \> Pankkitilit**.
2. Avaa pankkitili.
3. Määritä **Yleinen**-pikavälilehdessä **Positiivisen maksun muoto** -kentän arvoksi aiemmin luotu muoto.
4. Määritä **Positiivisen maksun aloituspäivä** -kenttään nykyinen päivämäärä.

## <a name="generate-a-positive-pay-file"></a>Luo Positive pay -tiedosto

1. Valitse **Maksuliikenteen hallinta \> Pankkitilit \> Pankkitilit**.
2. Avaa pankkitili, jonka positiivinen maksu on määritetty.
3. Valitse **Hallitse maksuja \> Positiivinen maksu \> Positiivinen maksutiedosto**.
4. Määritä **Määräpäivämäärä**-kenttä. Ennen tätä päivämäärää luodut sekit sisällytetään raporttiin.

Tuloksena saatava XML-tiedosto ladataan.
