---
title: Varaston erääntymisraportin tallennus
description: Tässä ohjeaiheessa käsitellään toimintoa, jolla voi suorittaa varaston erääntymisraportin ja jolla tuloksen saa käyttöön lomakkeena ja kaaviona.
author: AndersGirke
manager: tfehr
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9148a9032615222a1fdfe453488e716bacadbabc
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275576"
---
# <a name="inventory-aging-report-storage"></a>Varaston erääntymisraportin tallennus


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Microsoft Dynamics 365 Supply Chain Managementissa voi suorittaa **Varaston erääntymisraportin tallennus** -raportin, jonka saa sitten käyttöön lomakkeena ja kaaviona. Lomakkeessa sarakkeita ja koostesaldoja säädetään dynaamisesti määritetyn asettelun mukaan. Kaavio muodostaa visuaalisen suodatusta tukevan yleiskuvan, jossa voi porautua tietoihin. Lisäksi **Varaston erääntymisraportti** -nimisessä tietoyksikössä voi tuoda **Varaston erääntymisraportin tallennus** -raportin tulokset esimerkiksi Microsoft Excel- tai PDF-tiedostona.

Tällainen **Varaston erääntymisraportin tallennus** -raportin suorittamistapa on kätevä, jos tuloksessa on runsaasti rivejä. Tuloksessa voi olla esimerkiksi runsaasti rivejä, jos 50 000 nimikkeestä ja 300 myymälästä luodaan varastoja ja pyydät varaston erääntymistä nimikkeen, sijainnin ja varaston perusteella.

## <a name="enable-the-inventory-value-storage-report-feature"></a>Varastoarvon tallennuksen raporttitoiminnon ottaminen käyttöön

Ennen kuin käytät tätä toimintoa, sinun on otettava se käyttöön järjestelmässä. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä ottaa sen käyttöön tarvittaessa. Toiminto näkyy seuraavasti:

- **Moduuli** - kustannustenhallinta
- **Toiminnon nimi** - Varaston erääntymisraportin tallennus

## <a name="run-an-inventory-aging-report-storage"></a>Suorita varaston erääntymisraportin tallennus

1. Valitse **Kustannushintojen hallinta \> Kyselyt ja raportit \> Varaston erääntymisraportin tallennus**.
1. Valitse **Uusi**.
1. Kirjoita raportin yksilöivä nimi **Prosessin tunniste – nimi**-kenttään.
1. Valitse **Tunniste – tunnus** -raportti ja tee tarvittava suodatus.

    Raportti suoritetaan aina erätyönä.

1. Kun erätyö on valmis, tulos näkyy **Varaston erääntymisraportin tallennus** -sivulla.
1. Voit tarkastella tulosta perinteisenä ruudukkoasetteluna valitsemalla **Näytä tiedot**. Voit tarkastella tulosta koostekaaviona valitsemalla **Näytä kaavio**.

    > [!NOTE]
    > Lomake ei sisällä raporttiasettelussa määritettyjä välisummia.

Voit viedä **Varaston erääntymisraportti** -tietoyksikössä **Varaston erääntymisraportin tallennus** -raportin tuloksen käyttämällä **Prosessin tunniste – nimi** -kentän suodatinta niissä muodoissa, joita tietojen hallinta tukee.
