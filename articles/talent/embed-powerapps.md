---
title: "PowerApps-sovellusten upottaminen Core HR:ään"
description: "Tässä ohjeaihe on ratkaisu ongelmalle, jossa PowerApps-valikkovaihtoehto on kadonnut järjestelmänhallintamoduulista."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 197b553f0b202ee29ad42274e2c0e03446ec782c
ms.contentlocale: fi-fi
ms.lasthandoff: 12/04/2018

---

# <a name="embed-powerapps-apps-in-core-hr"></a>PowerApps-sovellusten upottaminen Core HR:ään

[!include [banner](includes/banner.md)]

**Ongelma**

**PowerApps**-valikkovaihto on kadonnut **Järjestelmänhallinta**-moduulista.

**Syy**

Käyttöliittymää on muutettu ja Microsoft PowerApps sisältyy vakiomukautusmalliin.

**Tarkkuus**

PowerApps-sovellusten upotustapaa on muutettu. PowerApps-sovellukset lisätään nyt mukautusmallin avulla. Voit lisätä PowerApps-sovelluksia lähes kaikille Microsoft Dynamics 365 for Talentin sivuille.

Lisätietoja PowerApps-sovelluksen upottamisesta Talentissa on kohdassa [PowerApps-sovellusten upottaminen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).

Jokainen ennen muutoksia sovelluksia upottanut PowerApps-asiakas olisi pitänyt päivittää uuteen malliin.

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

