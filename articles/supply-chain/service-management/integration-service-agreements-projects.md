---
title: Huoltosopimusten ja projektien integrointi
description: Kun käsittelet huoltosopimuksia ja huoltosopimusrivejä, käytät tietoja, jotka on määritetty Projektinhallinta ja kirjanpito -osan alueissa.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7252de08b40aa0668d3ce801b4cbd6f3a53ef12f
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673575"
---
# <a name="integration-for-service-agreements-and-projects"></a>Huoltosopimusten ja projektien integrointi 

[!include [banner](../includes/banner.md)]


Kun käsittelet huoltosopimuksia ja huoltosopimusrivejä, käytät tietoja, jotka on määritetty seuraavissa **Projektinhallinta ja kirjanpito** -osan alueissa.

## <a name="project-prices"></a>Projektihinnat

Huoltosopimustapahtuman kustannus- ja myyntihinnat johdetaan kustannushinta-asetuksista, joita sovelletaan huoltosopimukseen liitettyyn projektiin. Kustannus- ja myyntihinnat voidaan määrittää projekti-, työntekijä- ja luokkakohtaisesti. 

## <a name="project-validation"></a>Projektin oikeellisuustarkistus

Huoltosopimusriville valittavissa olevia projekteja, työntekijöitä ja luokkia voidaan rajata **Projektinhallinta ja kirjanpito** -osan oikeellisuustarkistusasetusten avulla. Määrittämällä oikeellisuustarkistusasetuksia voit yhdistää työntekijöitä, projekteja ja luokkia ja määrittää niille käyttöoikeuksia. 

## <a name="project-line-properties"></a>Projektirivin ominaisuudet

Rivin ominaisuus määritetään automaattisesti huoltosopimusriville.

Rivin ominaisuudet luodaan **Rivin ominaisuudet** -lomakkeella **Projektinhallinta ja kirjanpito** -osassa. Huoltosopimukseen määritetty rivin ominaisuus liitetään huoltosopimukseen valittuun projektiin ja lisätään sen jälkeen automaattisesti huoltosopimusriville. 

## <a name="default-offset-accounts"></a>Oletusvastatilit

Jos kirjaat kulutapahtuman, tapahtumalle valitaan automaattisesti oletusarvoinen kulun vastatili. Oletusarvoinen kulutili määritetään nykyiseen huoltosopimukseen liitetyssä projektissa.

## <a name="project-categories"></a>Projektin luokat

Huoltosopimusriveille valittavissa olevat luokat määritetään **Tuoteluokat**-lomakkeella **Projektinhallinta ja kirjanpito** -osassa. 

> [!NOTE]
> <P>Luokat, joiden <STRONG>Käytössä kirjauskansioissa</STRONG>- valintaruutu on valittuna <STRONG>Projekti</STRONG>-välilehdellä <STRONG>Projektiluokat</STRONG>-lomakkeessa, ovat valittavissa. Jos <STRONG>Luokat, jotka eivät ole käytössä</STRONG> -valintaruutu on valittuna <STRONG>Kirjauskansiot</STRONG> -välilehdellä <STRONG>Projektinhallinta ja kirjanpito</STRONG> -lomakkeessa, kaikki luokat ovat valittavissa.</P>

## <a name="project-parameters"></a>Projektiparametrit

Jos **Poistetut työntekijät** -kenttä **Kirjauskansiot**-välilehdellä **Projektinhallinta ja kirjanpito** -lomakkeessa on valittuna, voit valita ei-aktiivisia ja aktiivisia työntekijöitä **Huoltosopimukset**- ja **Huoltotilaukset** -lomakkeissa.

Lisäksi voit ottaa käyttöön **Aloitusaika**- ja **Päättymisaika**-kentät **Projekti**-välilehdellä **Huoltotilaukset**-lomakkeessa, jos haluat määrittää huoltotilausriveille aloitus- ja päättymisajat.

## <a name="enable-the-starting-and-ending-time-feature-for-service-orders"></a>Aloitus- ja päättymisaikaominaisuuden ottaminen käyttöön huoltotilauksissa

1.  Valitse **Projektinhallinta ja kirjanpito** \> **Asetukset** \> **Projektinhallinnan ja kirjanpidon parametrit**.

2.  Valitse **Kirjauskansiot**-välilehti ja valitse sitten **Näytä aloitus-/ lopetusajat** -valintaruutu.

3.  Napsauta **Projektinhallinta ja kirjanpito** \> **Määritys** \> **Kirjauskansiot** \> **Kirjauskansioiden nimet**.

4.  Valitse huoltotilaukseen liitetyn kirjauskansion nimi.

5.  Valitse **Yleinen**-välilehti ja valitse sitten **Näytä aloitus-/ lopetusajat** -valintaruutu.


> [!NOTE]
> <P>Valitse huoltotilauksen kirjauskansion nimi <STRONG>Tunti</STRONG>-kentässä <STRONG>Kirjauskansiot</STRONG>-välilehdellä <STRONG>Huoltohallinnan parametrit</STRONG> -lomakkeessa.</P>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]