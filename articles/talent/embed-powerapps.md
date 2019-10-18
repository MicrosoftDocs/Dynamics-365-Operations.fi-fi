---
title: PowerApps-sovellusten upottaminen Dynamics 365 – Core HR:ssä
description: Tässä ohjeaiheessa käsitellään tapaa, jolla ratkaistaan ongelma, jossa PowerApps-valikkovaihtoehto on kadonnut järjestelmänhallintamoduulista.
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
ms.openlocfilehash: 4fbc24c5ceb73389b84b125eb942ac31757928aa
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008427"
---
# <a name="embed-powerapps-apps-in-core-hr"></a>PowerApps-sovellusten upottaminen Core HR:ssä

[!include [banner](includes/banner.md)]

**Lähetä**

**PowerApps**-valikkovaihtoehto on kadonnut **Järjestelmänhallinta**-moduulista.

**Syy**

Käyttöliittymää on muutettu ja Microsoft PowerApps sisältyy vakiomukautusmalliin.

**Ratkaisu**

PowerApps-sovellusten upotustapaa on muutettu. PowerApps-sovellukset lisätään nyt mukautusmallin avulla. Voit lisätä PowerApps-sovelluksia lähes kaikille Microsoft Dynamics 365 Talentin sivuille.

Lisätietoja PowerApps-sovelluksen upottamisesta Talentissa on kohdassa [PowerApps-sovellusten upottaminen](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).

Jokainen PowerApps-asiakas, joka on upottanut sovelluksia ennen muutosta, olisi pitänyt päivittää uuteen malliin.

**PowerApps**-painike on lähes jokaisen Talent-sivun oikeassa yläkulmassa. Voit lisätä PowerApps-sovelluksen tällä painikkeella.

Esimerkki:

1. Valitse **Henkilöstön hallinta \> Linkit \> Työntekijät \> Työntekijät**.
2. Valitse ensin **PowerApps**-painike ja sitten **Lisää PowerApp**.

    ![PowerApps-painike](media/png.png)

3. Täytä **Lisää PowerApp** -valintaikkunan kentät.

    ![Lisää PowerApp -valintaikkuna](media/insert-powerapp.png)

Voit vaihtoehtoisesti noudattaa seuraavia ohjeita.

1. Valitse sivun toimintoruudun **Asetukset**-välilehden **Mukauta**-ryhmässä **Mukauta tämä lomake**.

    ![Mukauta-ryhmä Asetukset-välilehdessä](media/options.png)

    Mukauttamisen työkalurivi tulee näkyviin.

2. Valitse työkalurivillä **Lisää \>PowerApp**.

    ![PowerApps-sovelluksen lisääminen mukauttamisen työkalurivin avulla](media/powerapp-bar.png)
