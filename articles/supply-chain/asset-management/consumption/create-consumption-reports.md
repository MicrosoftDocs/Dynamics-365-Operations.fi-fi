---
title: Kulutusraporttien luominen
description: Tässä ohjeaiheessa kerrotaan, kuinka kulutusraportit luodaan resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3d978f8b991211e477dd8f766fe67432d9d493d0
ms.sourcegitcommit: c0b581e4c647b6c47bc14d1d7bfe267832afecba
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/21/2019
ms.locfileid: "1913084"
---
# <a name="create-consumption-reports"></a>Kulutusraporttien luominen

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Kun olet luonut ja kirjannut työtilausten kulutusrekisteröinnit käyttöomaisuuden hallinnassa, käytettävissä on kaksi raporttia kulutuksen yksityiskohtien näyttämistä varten.


## <a name="asset-consumption-report"></a>Resurssien kulutusraportti

Kun työtilausten kulutus on kirjattu, voit tulostaa käyttöomaisuuden kulutusraportin. Raportissa näkyvät käyttöomaisuudelle kirjatut tunnit, tuntikustannukset, nimikekustannukset ja kulut.

1. Valitse **Resurssien hallinta** > **raportit** > **Resurssit** > **Resurssien kulutus**.

2. Valitse **Resurssien kulutus** -valintaikkunassa parametrit ja erittelytaso, jotka haluat nähdä, valitsemalla asianmukaisissa vaihtopainikkeissa "kyllä" ja lisäämällä toiminnallisen sijainnin taso **Näytä**-osaan.
    - **Tasot** -kentän avulla voit määrittää, miten yksityiskohtaisia resurssiriveistä haluat liittyen toiminnallisiin sijainteihin. Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoinen toiminnallinen sijaintirakenne, kaikki toimintosijainnin resurssit näkyvät ylimmällä tasolla, joten rivi voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista. Jos lisäät arvon "0" **Tasot**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki resurssit kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät. 
    - Valitse "kyllä" **Kaikkien aliresurssien summa** -vaihtopainikkeessa, jos haluat nähdä kunkin alakäyttöomaisuuserän summat raportissa.

3. Valitse päivämääräväli **Päivämäärät** -osassa.

4. Valitse **Kohde-** pikavälilehdessä, jos haluat näyttää raportin näytössä, tulostaa sen tai tallentaa sen tiedostona tai sähköpostina.

5. Voit tarvittaessa valita tietyt raportissa näytettävät käyttöomaisuudet. Valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodatin**ja lisää käyttöomaisuudet, jotka haluat sisällyttää raporttiin.

6. Luo raportti valitsemalla **OK**.


## <a name="work-order-consumption-report"></a>Työtilauksen kulutusraportti

Kun työtilausten kulutus on kirjattu, voit tulostaa työtilauksen kulutusraportin. Raportissa näkyvät työtilauksille kirjatut tunnit, tuntikustannukset, nimikekustannukset ja kulut.

1. Valitse **Resurssien hallinta** > **Raportit** > **Työtilaukset** > **Työtilauksen kulutus**.

2. Valitse **Työtilauksen kulutus** -valintaikkunassa raporttiin sisällytettävät parametrit valitsemalla "kyllä" **Näytä**-osion asianmukaisissa vaihtopainikkeissa.

3. Valitse päivämääräväli **Päivämäärät** -osassa.

4. Valitse **Kohde-** pikavälilehdessä, jos haluat näyttää raportin näytössä, tulostaa sen tai tallentaa sen tiedostona tai sähköpostina.

5. Voit tarvittaessa valita tietyt raportissa näytettävät työtilaukset. Valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodatin**ja lisää työtilaukset, jotka haluat sisällyttää raporttiin.

6. Luo raportti valitsemalla **OK**.


>[!NOTE]
>Voit myös luoda [työtilausraportin](../work-orders/work-order-report.md), joka sisältää enemmän työtilaustietoja.

