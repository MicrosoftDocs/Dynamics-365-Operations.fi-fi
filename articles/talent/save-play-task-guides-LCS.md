---
title: Tehtäväoppaiden tallentaminen LCS:ään sekä niiden toistaminen
description: Tässä ohjeaiheessa kerrotaan, miten tehtäväoppaat tallennetaan Microsoft Dynamics Lifecycle Servicesiin (LCS) ja miten niitä toistetaan.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e84f0c18cfb52de2c6c8c40af9a08a88c947e38c
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010565"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a>Tehtäväoppaiden tallentaminen LCS:ään sekä niiden toistaminen

[!include [banner](includes/banner.md)]

**Ympäristön tiedot** 

Microsoft Dynamics 365 Talent, joka oli otettu käyttöön Microsoft Dynamics Lifecycle Servicesin kanssa (LCS)

**Varasto-otto**

Asiakas haluaa tallentaa uudet tehtävätallenteet LCS-projektiin ja sitten toistaa tallennettuja tehtäväoppaita.

**Tarkkuus**

Tallenna tehtävätallenne seuraavien ohjeiden mukaisesti LCS-palveluun.

1. Kirjaudu LCS-palveluun ja valitse projekti.
2. Valitse **Liiketoimintaprosessin mallintaja** -ruutu.
3. Näytä sivu päivitetyssä BPM-käyttöliittymässä.
4. Valitse ensin kirjasto sitten **Kopioi**.
5. Anna liiketoimintaprosessin mallintajalle (BPM) nimi.
6. Kirjaudu Talentiin LCS-palvelusta.
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
