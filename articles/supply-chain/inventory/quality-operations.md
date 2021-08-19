---
title: Toiminnot määrityksistä poikkeamisille
description: Tässä aiheessa kuvataan, kuinka voit luoda ja käyttää toimintoja määrityksistä poikkeamisille.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestOperations, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fda4aaadd5a2d9e6093b767d83a9187a970bf14c60f089f43b1b98a26cf0ac76
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739823"
---
# <a name="operations-for-nonconformances"></a>Toiminnot määrityksistä poikkeamisille

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, kuinka voit luoda ja käyttää toimintoja määrityksistä poikkeamisille.

Määritä **Toiminnot**-sivulla luokitukset hyväksytyn määrityksistä poikkeamisen käsittelyä varten. Kun liität määrityksistä poikkeamiseen toiminnon, voit myös määrittää yksityiskohtia tietoja, kuten tietoja liittyvästä materiaalista, työtunneista ja erilaisista toiminnon tekemiseen tarvittavista kuluista. Näiden tietojen avulla järjestelmä laskee toiminnon arvioidun kustannuksen. Tarkat tiedot ja arvioidut kustannukset on tarkoitettu viitetiedoiksi. Laatuun liittyvät toiminnot poikkeavat tuotantoreititystä varten määritettävistä toiminnoista.

> [!NOTE]
> Vaikka voitkin seurata kustannuksia, aikaa ja nimikkeitä, joita käytetään määrityksistä poikkeamiseen liittyvässä toiminnossa, syötetyt tiedot ovat vain tiedoksi. Sitä ei integroida automaattisesti kirjanpitoon, varaston alareskontraan tai **Työajan seuranta** -moduuliin.

## <a name="examples-of-operations"></a>Esimerkkejä toiminnoista

Työskentelet valmistusyhtiössä. Määrityksistä poikkeaminen luotiin ja hyväksyttiin nimikkeille, jotka epäonnistuivat laatutestissä. Korjaus on luotu sen merkiksi, että ongelma liittyy koneen huonoon laakeriin. Laakerin vaihto edellyttää useita vaiheita, ja kunkin työvaiheen vastuualuetta seurataan. Esimerkiksi seuraavat vaiheet voivat olla pakollisia:

1. Tuotantorivi pysäytetään ja puhdistusrutiini suoritetaan.
1. Huoltohenkilöt vaihtavat laakerin.
1. Laadunvalvontahenkilöstö tarkistaa laitteen, ennen kuin se kytketään takaisin päälle.

Tässä esimerkissä voidaan luoda seuraavat toiminnot, jotka edustavat työtä, joka on tehtävä:

- Pysäytä tuotantorivi.
- Puhdista tuotantorivi.
- Huolla kone.
- Tarkista kone.

## <a name="create-an-operation"></a>Luo toiminto

1. Valitse **Varastonhallinta \> Asetukset \> Laadunhallinta \> Toiminnot**.
1. Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**. Määritä sitten uudelle rivillä seuraavat kentät:

    - **Toiminto** – Syötä toiminnon yksilöivä tunnus tai nimi.
    - **Kuvaus** – Anna toiminnon yksityiskohtainen kuvaus.
    - **Tyyppi** – Jos toimintoa voidaan käyttää vain määrityksistä poikkeamisiin, jotka liittyvät tiettyyn tilaustyyppiin, valitse tilaustyyppi (*Ostotilaus* tai *Myyntitilaus*).

1. Sulje sivu.

## <a name="additional-resources"></a>Lisäresurssit

- [Laadunhallinnan yleiskuvaus](quality-management-processes.md)
- [Laadun ja määrityksistä poikkeamisen hallinnan ottaminen käyttöön](enable-quality-management.md)
- [Määrityksistä poikkeamisten luonti ja käsittely](tasks/create-process-non-conformance.md)
- [Määrityksistä poikkeamisia hyväksyvät työntekijät](quality-responsible-workers.md)
- [Määrityksistä poikkeamisia koskevat karanteenivyöhykkeet](quality-quarantine-zones.md)
- [Määrityksistä poikkeamisten diagnostiikkatyypit](quality-diagnostic-types.md)
- [Määrityksistä poikkeamisten laatukulut](quality-charges.md)
- [Määrityksistä poikkeamisten ongelmatyypit](quality-operations.md)
- [Laadunhallinta varastoprosesseja varten](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
