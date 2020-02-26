---
title: Power Apps -sovellusten upottaminen Dynamics 365 Human Resourcesissa
description: Tässä ohjeaiheessa käsitellään tapaa, jolla ratkaistaan ongelma, jossa Microsoft Power Apps-valikkovaihtoehto on kadonnut järjestelmänhallintamoduulista.
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
ms.openlocfilehash: 8275a8a7c68fa13d6b9880c4c411deaa2dcbb998
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2020
ms.locfileid: "3017870"
---
# <a name="embed-power-apps-apps-in-dynamics-365-human-resources"></a>Power Apps -sovellusten upottaminen Dynamics 365 Human Resourcesissa

**Lähetä**

**Power Apps**-valikkovaihtoehto on kadonnut **Järjestelmänhallinta**-moduulista.

**Syy**

Käyttöliittymää on muutettu ja Microsoft Power Apps sisältyy vakiomukautusmalliin.

**Ratkaisu**

Power Appsin upotustapaa on muutettu. Power Apps lisätään nyt mukautusmallin avulla. Voit lisätä Power Appsin lähes kaikille Microsoft Dynamics 365 Talentin sivuille.

Lisätietoja Power Appsin upottamisesta Talentissa on kohdassa [Power Appsin upottaminen](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).

Jokainen Power Apps-asiakas, joka on upottanut sovelluksia ennen muutosta, olisi pitänyt päivittää uuteen malliin.

**Power Apps**-painike on lähes jokaisen Talent-sivun oikeassa yläkulmassa. Voit lisätä sovelluksia tällä painikkeella.

Esimerkki:

1. Valitse **Henkilöstön hallinta \> Linkit \> Työntekijät \> Työntekijät**.
2. Valitse- **Power Apps** -painike ja sitten **Lisää sovellus Power Appsista**.

    ![Power Apps-painike](media/png.png)

3. Täytä kentät **Lisää sovellus Power Appsista** -valintaruudussa.

    ![Sovelluksen lisääminen Power Apps -valintaruudusta](media/insert-powerapp.png)

Voit vaihtoehtoisesti noudattaa seuraavia ohjeita.

1. Valitse sivun toimintoruudun **Asetukset**-välilehden **Mukauta**-ryhmässä **Mukauta tämä sivu**.

    ![Mukauta-ryhmä Asetukset-välilehdessä](media/options.png)

    Mukauttamisen työkalurivi tulee näkyviin.

2. Valitse työkaluriviltä **Lisää sovellus Power Appsista**.

    ![Power Apps-sovelluksen lisääminen mukauttamisen työkalurivin avulla](media/powerapp-bar.png)
