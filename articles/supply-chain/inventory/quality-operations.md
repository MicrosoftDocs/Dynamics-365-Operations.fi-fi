---
title: Toiminnot määrityksistä poikkeamisille
description: Tässä aiheessa kuvataan, kuinka voit luoda ja käyttää toimintoja määrityksistä poikkeamisille.
author: yufeihuang
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
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 35619454af8b1cb1b7d383d393362f58d9dd0ea6
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573870"
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
