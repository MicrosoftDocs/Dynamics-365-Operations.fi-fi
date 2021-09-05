---
title: Tehtäväoppaiden tallentaminen LCS:ään sekä niiden toistaminen
description: Tässä ohjeaiheessa kerrotaan, miten tehtäväoppaat tallennetaan Microsoft Dynamics Lifecycle Servicesiin (LCS) ja miten niitä toistetaan.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 42fad014590abebf159b71227a44eb8df60bf05e
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416878"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a>Tehtäväoppaiden tallentaminen LCS:ään sekä niiden toistaminen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Ympäristön tiedot** 

Microsoft Dynamics 365 Human Resources, joka oli otettu käyttöön Microsoft Dynamics Lifecycle Servicesin kanssa (LCS)

**Varasto-otto**

Asiakas haluaa tallentaa uudet tehtävätallenteet LCS-projektiin ja sitten toistaa tallennettuja tehtäväoppaita.

**Ratkaisu**

Tallenna tehtävätallenne seuraavien ohjeiden mukaisesti LCS-palveluun.

1. Kirjaudu LCS-palveluun ja valitse projekti.
2. Valitse **Liiketoimintaprosessin mallintaja** -ruutu.
3. Näytä sivu päivitetyssä BPM-käyttöliittymässä.
4. Valitse ensin kirjasto sitten **Kopioi**.
5. Anna liiketoimintaprosessin mallintajalle (BPM) nimi.
6. Kirjaudu Human Resources LCS:n kautta.
7. Kirjoita **Haku**-kenttään **ohje**. Lifecycle Servicesin ohje avautuu.
8. Valitse Lifecycle Services -ohjemäärityksen **Päivitä**-painike.

    BPM-kirjaston pitäisi tulla näkyviin ja sen pitäisi olla aktiivinen.

9. Sulje sivu.
10. Luo tehtävätallenne.
11. Kun olet valmis, valitse **Tallenna Lifecycle Servicesiin**.

    ![Tallenna Lifecycle Servicesiin.](media/task-guides.png)

12. Valitse BPM-kirjasto ja solmu, johon tehtävätallenne tallennetaan.

Toista tehtäväopas LCS-palvelusta seuraavien ohjeiden mukaisesti.

1. Käynnistä tehtävän tallennustoiminto.
2. Valitse **Avaa LCS-palvelusta**.
3. Valitse kirjasto ja BPM-solmu, jossa tallennettu tehtäväopas on.
4. Avaa tehtäväopas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
