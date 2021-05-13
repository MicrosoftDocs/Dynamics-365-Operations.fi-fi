---
title: Määrityksistä poikkeamisten ongelmatyypit
description: Tässä aiheessa kuvataan, kuinka voit luoda ja käyttää ongelmatyyppejä määrityksistä poikkeamisille.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventProblemType, InventProblemTypeSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df509365f5c900898921acfbda380b5e20c7a251
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956644"
---
# <a name="problem-types-for-nonconformances"></a>Määrityksistä poikkeamisten ongelmatyypit

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, kuinka voit luoda ja käyttää ongelmatyyppejä määrityksistä poikkeamisille.

Määritä **Ongelmatyypit**-sivulla luokitus laatuongelmille, joita kohdataan erityyppisissä määrityksistä poikkeamisen tyypeissä. Määritä jokaiselle luotavalle ongelmatyypille määrityksistä poikkeamisten tyypit, joiden kanssa ongelmatyyppiä voidaan käyttää. Voit määrittää seuraavat määrityksistä poikkeamisten tyypit:

- **Sisäinen** – Tämän tyyppiset määrityksistä poikkeamiset koskevat käytettävissä olevaa varastoa (esimerkiksi laatutilaukset tai karanteenitilaukset).
- **Asiakas:** Tämän tyyppiset määrityksistä poikkeamiset liittyvät myyntitilauksiin.
- **Toimittaja:** Tämän tyyppiset määrityksistä poikkeamiset liittyvät ostotilauksiin.
- **Huoltopyyntö:** Tämän tyyppiset määrityksistä poikkeamiset liittyvät huoltotilauksiin.
- **Tuotanto** –Tämän tyyppiset määrityksistä poikkeamiset liittyvät erätilauksiin tai tuotantotilauksiin.
- **Oheistuotteen tuotanto** –Tämän tyyppiset määrityksistä poikkeamiset liittyvät erätilauksiin tai oheistuotteisiin.

Kun luot uuden ongelman tyypin, valitse toimintoruudusta **Määrityksistä poikkeamisen tyypit** ja luo luettelo määrityksistä poikkeamisen tyypeistä, jotka on hyväksytty ongelmatyypille. Vikakoodiin liittyvä ongelmatyyppi voi esimerkiksi koskea kaikkia määrityksistä poikkeamisen tyyppejä. Asiakasvalituksiin liittyvä ongelmatyyppi saattaa kuitenkin koskea vain **Asiakas**- ja **Huoltopyyntö**-tyyppejä määrityksistä poikkeamisille.

## <a name="examples-of-problem-types"></a>Esimerkkejä ongelmatyypeistä

Seuraavassa on esimerkkejä ongelmatyyppien skenaarioista, joita voidaan käyttää eri määrityksistä poikkeamisten tyyppien kanssa:

- **Asiakas**: Asiakas teki valituksen, asiakas teki palautuksen tai laatumääritykset eivät täyttyneet.
- **Toimittaja:** Tuote oli vioittunut, laatumääritykset eivät täyty tai väärä tuote vastaanotettiin.
- **Huoltopyyntö:** Laatumääritykset eivät täyty, asiakas teki valituksen tai kone on huollettava.
- **Tuotanto:** Laatumääritykset eivät täyty, kone on huollettava tai tuote on vioittunut.
- **Oheistuotteen tuotanto:** Laatumääritykset eivät täyty, kone on huollettava tai tuote on vioittunut.

## <a name="create-a-problem-type-and-assign-it-to-nonconformance-types"></a>Ongelmatyypin luominen ja sen määrittäminen määrityksistä poikkeamisten tyyppeihin

1. Valitse **Varastonhallinta \> Asetukset \> Laadunhallinta \> Ongelmatyypit**.
1. Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**. Määritä sitten uudelle rivillä seuraavat kentät:

    - **Ongelmatyyppi** – Anna ongelmatyypin yksilöivä tunniste tai nimi.
    - **Kuvaus** – Anna ongelmatyypin yksityiskohtainen kuvaus.

1. Kun uusi rivi on vielä valittuna, valitse **Määrityksistä poikkeamisen tyypit** toimintoruudusta.
1. Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**. Määritä sitten uudelle riville **Määrityksistä poikkeamisen tyyppi** -kentän arvoksi määrityksistä poikkeamisen tyyppi, jonka haluat sallia ongelmatyypille.
1. Toista edellinen vaihe jokaiselle määrityksistä poikkeamisen tyypille, jonka haluat valtuuttaa ongelmatyypille.
1. Sulje sivut.

## <a name="additional-resources"></a>Lisäresurssit

- [Laadunhallinnan yleiskuvaus](quality-management-processes.md)
- [Laadun ja määrityksistä poikkeamisen hallinnan ottaminen käyttöön](enable-quality-management.md)
- [Määrityksistä poikkeamisia hyväksyvät työntekijät](quality-responsible-workers.md)
- [Määrityksistä poikkeamisia koskevat karanteenivyöhykkeet](quality-quarantine-zones.md)
- [Määrityksistä poikkeamisten diagnostiikkatyypit](quality-diagnostic-types.md)
- [Määrityksistä poikkeamisten laatukulut](quality-charges.md)
- [Toiminnot määrityksistä poikkeamisille](quality-operations.md)
- [Laadunhallinta varastoprosesseja varten](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
