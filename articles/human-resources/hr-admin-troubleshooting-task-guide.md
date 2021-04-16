---
title: Tehtäväoppaiden tallentaminen LCS:ään sekä niiden toistaminen
description: Tässä artikkelissa kerrotaan, miten tehtäväoppaat tallennetaan Microsoft Dynamics Lifecycle Servicesiin (LCS) ja miten niitä toistetaan.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 51ffdb508f09ceaaefb458cd614b9c64604eb639
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797908"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a>Tehtäväoppaiden tallentaminen LCS:ään sekä niiden toistaminen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Ympäristön tiedot** 

Microsoft Dynamics 365 Human Resources, joka oli otettu käyttöön Microsoft Dynamics Lifecycle Servicesin kanssa (LCS)

**Varasto-otto**

Asiakas haluaa tallentaa uudet tehtävätallenteet LCS-projektiin ja sitten toistaa tallennettuja tehtäväoppaita.

**Tarkkuus**

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

    ![Tallenna Lifecycle Servicesiin](media/task-guides.png)

12. Valitse BPM-kirjasto ja solmu, johon tehtävätallenne tallennetaan.

Toista tehtäväopas LCS-palvelusta seuraavien ohjeiden mukaisesti.

1. Käynnistä tehtävän tallennustoiminto.
2. Valitse **Avaa LCS-palvelusta**.
3. Valitse kirjasto ja BPM-solmu, jossa tallennettu tehtäväopas on.
4. Avaa tehtäväopas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]