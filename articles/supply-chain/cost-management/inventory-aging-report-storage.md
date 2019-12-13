---
title: Varaston erääntymisraportti
description: Tässä ohjeaiheessa käsitellään toimintoa, jolla voi suorittaa varaston erääntymisraportin ja jolla tuloksen saa käyttöön lomakkeena ja kaaviona.
author: AndersGirke
manager: AnnBe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 21411c104c854224ff3689dc8e080b88d9fc7d23
ms.sourcegitcommit: 9267608347c9781fb4ba70f1384ca24da69c716d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/15/2019
ms.locfileid: "2810248"
---
# <a name="inventory-aging-report"></a>Varaston erääntymisraportti


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Microsoft Dynamics 365 Supply Chain Managementissa voi suorittaa **Varaston erääntyminen** -raportin, jonka saa sitten käyttöön lomakkeena ja kaaviona. Lomakkeessa sarakkeita ja koostesaldoja säädetään dynaamisesti määritetyn asettelun mukaan. Kaavio muodostaa visuaalisen suodatusta tukevan yleiskuvan, jossa voi porautua tietoihin. Lisäksi **Varaston erääntymisraportti** -nimisessä tietoyksikössä voi tuoda **Varaston erääntyminen** -raportin tulokset esimerkiksi Microsoft Excel- tai PDF-tiedostona.

Tällainen **Varaston erääntyminen** -raportin suorittamistapa on kätevä, jos tuloksessa on runsaasti rivejä. Tuloksessa voi olla esimerkiksi runsaasti rivejä, jos 50 000 nimikkeestä ja 300 myymälästä luodaan varastoja ja pyydät varaston erääntymistä nimikkeen, sijainnin ja varaston perusteella.

## <a name="run-an-inventory-aging-report"></a>Varaston erääntymisraportin suorittaminen

1. Valitse **Kustannushintojen hallinta \> Kyselyt ja raportit \> Varaston erääntymisraportin tallennus**.
1. Valitse **Uusi**.
1. Kirjoita raportin yksilöivä nimi **Prosessin tunniste – nimi**-kenttään.
1. Valitse **Tunniste – tunnus** -raportti ja tee tarvittava suodatus.

    Raportti suoritetaan aina erätyönä.

1. Kun erätyö on valmis, tulos näkyy **Varaston erääntymisraportin tallennus** -sivulla.
1. Voit tarkastella tulosta perinteisenä ruudukkoasetteluna valitsemalla **Näytä tiedot**. Voit tarkastella tulosta koostekaaviona valitsemalla **Näytä kaavio**.

    > [!NOTE]
    > Lomake ei sisällä raporttiasettelussa määritettyjä välisummia.

Voit viedä **Varaston erääntymisraportti** -tietoyksikössä **Varaston erääntyminen** -raportin tuloksen käyttämällä **Prosessin tunniste – nimi** -kentän suodatinta niissä muodoissa, joita tietojen hallinta tukee.
