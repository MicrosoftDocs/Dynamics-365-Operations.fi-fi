---
title: Kulutusraporttien luominen
description: Tässä artikkelissa kerrotaan, kuinka kulutusraportit luodaan resurssien hallinnassa.
author: johanhoffmann
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 136d6248db8012e5870e0627ddbd3703aa63703b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852897"
---
# <a name="create-consumption-reports"></a>Kulutusraporttien luominen

[!include [banner](../../includes/banner.md)]

 

Kun olet luonut ja kirjannut työtilausten kulutusrekisteröinnit käyttöomaisuuden hallinnassa, käytettävissä on kaksi raporttia kulutuksen yksityiskohtien näyttämistä varten.


## <a name="asset-consumption-report"></a>Resurssien kulutusraportti

Kun työtilausten kulutus on kirjattu, voit tulostaa käyttöomaisuuden kulutusraportin. Raportissa näkyvät käyttöomaisuudelle kirjatut tunnit, tuntikustannukset, nimikekustannukset ja kulut.

1. Valitse **Resurssien hallinta** > **raportit** > **Resurssit** > **Resurssien kulutus**.

2. Valitse **Resurssien kulutus** -valintaikkunassa parametrit ja erittelytaso, jotka haluat nähdä, valitsemalla asianmukaisissa vaihtopainikkeissa **Kyllä** ja lisäämällä toiminnallisen sijainnin taso **Näytä**-osaan.
    - **Tasot** -kentän avulla voit määrittää, miten yksityiskohtaisia resurssiriveistä haluat liittyen toiminnallisiin sijainteihin. 
    
        Jos esimerkiksi annat kentässä arvon "1" ja kyseessä on monitasoinen toiminnallinen sijaintirakenne, kaikki toimintosijainnin resurssit näkyvät ylimmällä tasolla, joten rivi voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista. 
        
        Jos annat arvon "0" **Tasot**-kentässä, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki resurssit kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät. 
        
    - Valitse **Kyllä** **Kaikkien aliresurssien summa** -vaihtopainikkeessa, jos haluat nähdä kunkin alakäyttöomaisuuserän summat raportissa.

3. Valitse päivämääräväli **Päivämäärät** -osassa.

4. Valitse **Kohde-** pikavälilehdessä, jos haluat näyttää raportin näytössä, tulostaa sen tai tallentaa sen tiedostona tai sähköpostina.

5. Voit tarvittaessa valita tietyt raportissa näytettävät käyttöomaisuudet. Valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodatin** ja lisää käyttöomaisuudet, jotka haluat sisällyttää raporttiin.

6. Luo raportti valitsemalla **OK**.


## <a name="work-order-consumption-report"></a>Työtilauksen kulutusraportti

Kun työtilausten kulutus on kirjattu, voit tulostaa työtilauksen kulutusraportin. Raportissa näkyvät työtilauksille kirjatut tunnit, tuntikustannukset, nimikekustannukset ja kulut.

1. Valitse **Resurssien hallinta** > **Raportit** > **Työtilaukset** > **Työtilauksen kulutus**.

2. Valitse **Työtilauksen kulutus**-valintaikkunassa raporttiin sisällytettävät parametrit valitsemalla **Kyllä** **Näytä**-osion asianmukaisissa vaihtopainikkeissa.

3. Valitse päivämääräväli **Päivämäärät** -osassa.

4. Valitse **Kohde-** pikavälilehdessä, jos haluat näyttää raportin näytössä, tulostaa sen tai tallentaa sen tiedostona tai sähköpostina.

5. Voit tarvittaessa valita tietyt raportissa näytettävät työtilaukset. Valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodatin** ja lisää työtilaukset, jotka haluat sisällyttää raporttiin.

6. Luo raportti valitsemalla **OK**.


>[!NOTE]
>Voit myös luoda [työtilausraportin](../work-orders/work-order-report.md), joka sisältää enemmän työtilaustietoja.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]