---
title: Power Apps-sovellusten upottaminen Dynamics 365 – Core HR:ssä
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
ms.openlocfilehash: 6d1b7f1dd71e6bcbf10c4d91fe33e9494b041a2c
ms.sourcegitcommit: ae0efac749ab34d423fac44d00a597801c143fbb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/22/2019
ms.locfileid: "2830206"
---
# <a name="embed-power-apps-apps-in-dynamics-365---core-hr"></a>Power Apps-sovellusten upottaminen Dynamics 365 – Core HR:ssä

[!include [banner](includes/banner.md)]

**Lähetä**

**Power Apps**-valikkovaihtoehto on kadonnut **Järjestelmänhallinta**-moduulista.

**Syy**

Käyttöliittymää on muutettu ja Microsoft Power Apps sisältyy vakiomukautusmalliin.

**Ratkaisu**

Power Appsin upotustapaa on muutettu. Power Apps lisätään nyt mukautusmallin avulla. Voit lisätä Power Appsin lähes kaikille Microsoft Dynamics 365 Talentin sivuille.

Lisätietoja Power Appsin upottamisesta Talentissa on kohdassa [Microsoft Power Appsin upottaminen](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).

Jokainen Power Apps-asiakas, joka on upottanut sovelluksia ennen muutosta, olisi pitänyt päivittää uuteen malliin.

**Power Apps**-painike on lähes jokaisen Talent-sivun oikeassa yläkulmassa. Voit lisätä Power Appsin tällä painikkeella.

Esimerkki:

1. Valitse **Henkilöstön hallinta \> Linkit \> Työntekijät \> Työntekijät**.
2. Valitse ensin **Power Apps**-painike ja sitten **Lisää PowerApp**.

    ![Power Apps-painike](media/png.png)

3. Täytä **Lisää PowerApp** -valintaikkunan kentät.

    ![Lisää PowerApp -valintaikkuna](media/insert-powerapp.png)

Voit vaihtoehtoisesti noudattaa seuraavia ohjeita.

1. Valitse sivun toimintoruudun **Asetukset**-välilehden **Mukauta**-ryhmässä **Mukauta tämä lomake**.

    ![Mukauta-ryhmä Asetukset-välilehdessä](media/options.png)

    Mukauttamisen työkalurivi tulee näkyviin.

2. Valitse työkalurivillä **Lisää \>PowerApp**.

    ![Power Apps-sovelluksen lisääminen mukauttamisen työkalurivin avulla](media/powerapp-bar.png)
