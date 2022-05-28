---
title: Tallenna TDS-huojennustodistuksen numerot
description: Tässä aiheessa kuvataan, miten toimittajille myönnetyt Vero vähennettynä lähteissä (TDS) -huojennustodistuksen numerot tallennetaan.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 994ddbb4666c326d237d53d529ba126f42d48595
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727142"
---
# <a name="record-tds-concession-certificate-numbers"></a>Tallenna TDS-huojennustodistuksen numerot

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, miten toimittajille myönnetyt Vero vähennettynä lähteissä (TDS) -huojennustodistuksen numerot tallennetaan.

1. Siirry kohtaan **Vero \> Välilliset verot \> Ennakonpidätys \> Ennakonpidätyksen huojennukset**.
2. Valitse **Verotyyppi**-kentässä **TDS**, jos haluat tallentaa huojennustodistukset TDS-verotyypille.
3. Luo rivi valitsemalla **Yhteenveto**-välilehdessä **Alt+N**.

    [![Uuden rivin otsikko.](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)

4. Valitse **Ennakonpidätyskoodi**-kentässä TDS-verokoodi, jota varten toimittajan huojennustodistukset on myönnetty. **Ennakonpidätyskoodin nimi** -kentässä näkyy TDS-verokoodin nimi.
5. Määritä **Päivämäärästä**- ja **Päivämäärään**-kenttiin sen huojennustodistuksen voimassaolokausi, joka laskee toimittajan TDS:n huojennuksen perusteella TDS-verokoodin avulla.
6. Kirjoita **Huomautukset**-kenttään mahdolliset huomautukset.
7. Kirjoita **Osio**-kenttään lakisääteinen osakoodi, jonka alaisena TDS-toimiluvan sertifikaattia käytetään.

    Jos osakoodi on 197, arvo "A" näkyy sekä lomakkeen 26Q sarakkeessa "Ei-vähennyksen syy / pienempi vähennys" sekä lomakkeen 27Q sarakkeessa "Ei-vähennyksen syy / pienempi vähennys / brutto ylös" (jos sellainen on). Jos osion koodi on 197A, arvo "B" näkyy molemmissa paikoissa.

8. Valitse **Sertifikaatti**-pikavälilehti, kun haluat kirjata toimittajien TDS-huojennustodistusten numerot.
9. Valitse **Toimittajatili**-kentässä toimittajatili, jota varten TDS-huojennustodistus on myönnetty.
10. Määritä **Päivämäärästä**- ja **Päivämäärään**-kenttiin TDS-huojennustodistuksen voimassaolokausi.

    TDS:n laskeminen huojennuksen perusteella perustuu kauteen, jolloin toimittajalle luodaan todistus.

11. Kirjoita **Todistus**-kenttään TDS-huojennustodistuksen numero.

    [![Todistus-pikavälilehti.](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)

12. Sulje sivu.
