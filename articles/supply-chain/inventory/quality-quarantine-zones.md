---
title: Määrityksistä poikkeamisia koskevat karanteenivyöhykkeet
description: Tässä aiheessa kuvataan, kuinka voit luoda ja käyttää karanteenivyöhykkeitä määrityksistä poikkeamisille.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c770da899f07597896d0d392b5192ddc4162bec6271d0e11c34797d7a15f857e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754032"
---
# <a name="quarantine-zones-for-nonconformances"></a>Määrityksistä poikkeamisia koskevat karanteenivyöhykkeet

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, kuinka voit luoda ja käyttää karanteenivyöhykkeitä määrityksistä poikkeamisille.

Määritä **Karanteenivyöhykkeet**-sivulla vyöhykkeet, jotka voidaan liittää määrityksistä poikkeamiseen. Kun luot määrityksistä poikkeamisen, voit määrittää **Karanteenivyöhyke**- ja **Karanteenityyppi**-kentät **Yleinen**-välilehdellä **Määrityksistä poikkeamisen** -sivulla. **Karanteenivyöhyke**-kentässä näkyy yleensä alue tai sijainti, jossa nimike sijaitsee. **Karanteenityyppi**-kentässä nimike määritetään joko arvolla *Rajoitettu käyttö* tai *Käyttökelvoton*.

Kun tulostat määrityksistä poikkeamisen tai korjausraportin määrityksistä poikkeamiselle, voit tarkastella karanteenivyöhykettä, jolla nimike sijaitsee.

Voit myös tulostaa määrityksistä poikkeamisen tunnisteen määrityksistä poikkeamiselle. Tässä raportissa näkyy määritetty karanteenivyöhyke ja käyttötiedot, jotka ohjaavat viallisen materiaalin käsittelyssä. Karanteenivyöhykkeet voivat vastata varastopaikkoja tai operatiivisia resursseja.

## <a name="examples-of-quarantine-zones"></a>Esimerkkejä karanteenivyöhykkeistä

### <a name="example-1"></a>Esimerkki 1

Työskentelet elektroniikan valmistusyhtiössä, joka tuottaa ja jakelee televisioita, kaiuttimia ja mediasoittimia. Tässä tapauksessa voit määrittää karanteenivyöhykkeen niin, että se vastaa kutakin tuotetyyppiä.

### <a name="example-2"></a>Esimerkki 2

Kolmea lokeroa ja kahta hyllykköä käytetään määrityksistä poikkeavien nimikkeiden varastoimiseen. Tässä tapauksessa voit määrittää viisi karanteenivyöhykettä, yhden kullekin lokerolle ja kullekin hyllykölle.

## <a name="create-a-quarantine-zone"></a>Luo karanteenivyöhyke

1. Valitse **Varastonhallinta \> Asetukset \> Laadunhallinta \> Karanteenivyöhykkeet**.
1. Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**. Määritä sitten uudelle rivillä seuraavat kentät:

    - **Karanteenivyöhyke** – Syötä karanteenivyöhykkeen yksilöivä tunnus tai nimi.
    - **Kuvaus** – Anna karanteenivyöhykkeen yksityiskohtainen kuvaus.

1. Sulje sivu.

## <a name="additional-resources"></a>Lisäresurssit

- [Laadunhallinnan yleiskuvaus](quality-management-processes.md)
- [Laadun ja määrityksistä poikkeamisen hallinnan ottaminen käyttöön](enable-quality-management.md)
- [Määrityksistä poikkeamisia hyväksyvät työntekijät](quality-responsible-workers.md)
- [Määrityksistä poikkeamisten ongelmatyypit](quality-quarantine-zones.md)
- [Määrityksistä poikkeamisten diagnostiikkatyypit](quality-diagnostic-types.md)
- [Määrityksistä poikkeamisten laatukulut](quality-charges.md)
- [Toiminnot määrityksistä poikkeamisille](quality-operations.md)
- [Laadunhallinta varastoprosesseja varten](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
