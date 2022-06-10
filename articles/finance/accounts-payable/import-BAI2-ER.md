---
title: Pankkitilin täsmäytyksen edistyneen tuonnin käyttöönottäminen sähköisen raportoinnin avulla
description: Tässä ohjeaiheessa kerrotaan, kuinka sähköisen raportoinnin avulla määritetään edistynyt pankkien täsmäytysprosessi.
author: panolte
ms.date: 03/30/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 30530a9870ba2ff0546237d2698d1675afa78104
ms.sourcegitcommit: 2b4ee1fe05792332904396b5f495d74f2a217250
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2022
ms.locfileid: "8770191"
---
# <a name="set-up-advanced-bank-reconciliation-import-by-using-electronic-reporting"></a>Pankkitilin täsmäytyksen edistyneen tuonnin käyttöönottäminen sähköisen raportoinnin avulla

[!include [banner](../includes/banner.md)]

Voit tuoda pankkitilin täsmäytyksen lisätoimintojen avulla sähköiset tiliotteet ja täsmäyttää ne automaattisesti pankkitapahtumien kanssa Microsoft Dynamics 365 Financessa. Tässä aiheessa käsitellään tiliotteiden tuontitoimintoa. Tiliotteen tuontiasetukset vaihtelevat sähköisen tiliotteen muodon mukaan. Microsoft Dynamics 365 Finance tukee kolmea tiliotemuotoa, jotka ovat ISO20022, MT940 ja BAI2. 

## <a name="set-up-the-electronic-reporting-configuration"></a>Määritä sähköisen raportoinnin konfiguraatio

1. Valitse **Työtilat \> Sähköinen raportointi**.
2. Valitse **Microsoft**-määrityspalveluntarjoajan ruudusta **Arkistot**.
3. Valitse **Yleinen** ja valitse sitten **Avaa**.
4. Jos tietovarastoon on oltava yhteys, valitse sininen linkki valintaikkunasta.
5. Konfigurointiluettelosta löytyy **pankin tiliotteen malli \> BAI2-pankkitiliotemalli**.
6. Valitse **BAI2**-muoto.
7. Valitse **Versiot**-pikavälilehdellä valitun uusin versio ja valitse sitten **Tuo**.

## <a name="set-up-the-bank-statement-format"></a>Määritä tiliotemuotoilu

1. Valitse **Maksuliikenteen hallinta \> Asetukset \> Pankkitilin täsmäytyksen lisätoimintojen asetukset \> Tiliotteen muotoilu**.
2. Valitse **Uusi**.
3. Määritä **laskelman muoto**- ja **nimi**-kentät.
4. Valitse **Yleinen sähköinen tuontimuoto** -valintaruutu.
5. Aseta **Tuontimuodon määritys** -kentän arvoksi **BAI2**-muoto.

## <a name="set-up-the-bank-account"></a>Määritä pankkitili

1. Valitse **Maksuliikenteen hallinta \> Pankkitilit \> Pankkitilit**.
2. Avaa pankkitili.
3. Valitse **Täsmäytys**-pikavälilehdessä **Pankkitilin täsmäytyksen lisätoiminnot**-asetukseksi **Kyllä**.
4. Määritä **Tiliotteen muotoilu** -kenttään aiemmin luomasi muoto **BAI2**.

## <a name="import-the-bank-statement"></a>Tuo tiliote

1. Siirry kohtaan **Maksuliikenteen hallinta \> Tiliotteen täsmäytys \> Tiliotteet**.
2. Valitse **Tiliotteet**-sivun yläosasta **Tuo tiliote**.
3. Määritä **Pankkitili**-kenttä tiliotteen pankkitilille.
4. Määritä **Tiliotteen muotoilu** -kenttään aiemmin luomasi muoto **BAI2**.
5. Valitse ensin **Selaa** ja sitten **BAI**-tiedosto.
6. Valitse **Lataa palvelimeen**.
7. Valitse **OK** tuodaksesi valitun tiedoston.


## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Esimerkkejä tiliotteiden muodoista ja teknisistä asetteluista
Alla on esimerkkejä tuonnin lisäasetuksia pankkitilin täsmäytystietojen tuontitiedoston teknisistä asettelumäärityksistä sekä kolme esimerkkitiliotetiedostoa: [Tuontitiedoston esimerkit](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Tekninen asettelumääritys                             | Esimerkkitiliotetiedosto          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)     |
| DynamicsAXISO20022Layout | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)     |

