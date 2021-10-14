---
title: Määrityksistä poikkeamisten diagnostiikkatyypit
description: Tässä aiheessa kuvataan, kuinka käytetään ja luodaan määrityksistä poikkeamisten kanssa käytettäviä diagnostiikkatyyppejä.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestDiagnosticType, InventTestCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: edaa3a8b5c6446f039f33589166d832dcd9d0b9a
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580933"
---
# <a name="diagnostic-types-for-nonconformances"></a>Määrityksistä poikkeamisten diagnostiikkatyypit

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, kuinka käytetään ja luodaan määrityksistä poikkeamisten kanssa käytettäviä diagnostiikkatyyppejä.

Määritä diagnostiikkatoimenpiteiden luokitus **Diagnostiikan tyypit** -sivulla. Kun luot korjauksen määrityksestä poikkeamiselle, valitset diagnostiikan. Korjaus ilmaisee hyväksytyn poikkeaman vianmääritystoimenpiteen ja sen tekijän. Se määrittää myös halutun ja suunnittelun valmistumispäivämäärän.

## <a name="examples-of-diagnostic-types"></a>Esimerkkejä diagnostiikkatyypeistä

Työskentelet valmistusyrityksessä, ja useat nimikkeet ovat epäonnistuneet laatutestissä. Nämä nimikkeet siirretään karanteenialueelle ja merkitään määrityksistä poikkeaviksi tuotteiksi. Määrityksistä poikkeamisen tietue luodaan Microsoft Dynamics 365 Supply Chain Managementissa tietojen seuraamiseksi ongelman ratkaisun kautta.

Tässä tapauksessa laatuongelmat tapahtuvat, koska nimikkeitä pakkaavan koneen laakerit ovat vioittuneet ja ylikuumenneet. Tämän ongelman korjaus on laitteen osien korvaaminen.

Kun määrität diagnostiikkatyypit, voit luoda useita tietueita, joista jokainen edustaa erityyppistä ongelmaa, joka koneella saattaa olla. Vaihtoehtoisesti voit luoda yhden yleisen diagnostiikkatyypin, joka kuvaa koneiden korjausta.

## <a name="create-a-diagnostic-type"></a>Diagnostiikkatyypin luominen

1. Valitse **Varastonhallinta \> Asetukset \> Laadunhallinta \> Diagnostiikan tyypit**.
1. Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**. Määritä sitten uudelle rivillä seuraavat kentät:

    - **Diagnostiikka** – Anna diagnostiikkatyypin yksilöivä tunniste tai nimi.
    - **Kuvaus** – Anna diagnostiikkatyypin yksityiskohtainen kuvaus.

1. Sulje sivu.

## <a name="additional-resources"></a>Lisäresurssit

- [Laadunhallinnan yleiskuvaus](quality-management-processes.md)
- [Laadun ja määrityksistä poikkeamisen hallinnan ottaminen käyttöön](enable-quality-management.md)
- [Määrityksistä poikkeamisia hyväksyvät työntekijät](quality-responsible-workers.md)
- [Määrityksistä poikkeamisia koskevat karanteenivyöhykkeet](quality-quarantine-zones.md)
- [Määrityksistä poikkeamisten ongelmatyypit](quality-problem-types.md)
- [Määrityksistä poikkeamisten laatukulut](quality-charges.md)
- [Toiminnot määrityksistä poikkeamisille](quality-operations.md)
- [Laadunhallinta varastoprosesseja varten](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
