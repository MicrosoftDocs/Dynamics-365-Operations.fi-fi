---
title: Tietojen integrointiprojektin luominen
description: Tässä ohjeaiheessa kerrotaan, miten tietojen integrointiprojekti luodaan.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: b08af906c18f6c0790ca56c69a833733f48cd88c
ms.sourcegitcommit: 822aea26c5da259efe11ff3b3dc4cf1598425689
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/16/2021
ms.locfileid: "7386359"
---
# <a name="create-a-data-integrator-project"></a>Tietojen integrointiprojektin luominen

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten tietojen integrointiprojekti luodaan.

1. Kirjaudu Microsoft Dynamics 365 Financeiin.
2. Siirry kohtaan **Työtilat \> Tietojen hallinta** ja valitse **Tietoyksiköt**. Odota, kunnes kaikki tietoyksiköt on päivitetty, ennen kuin siirryt seuraavaan vaiheeseen.
3. Avaa [Power Apps -portaali](https://make.powerapps.com/) ja toimi seuraavasti:

    1. Valitse sopiva ympäristö.
    2. Valitse vasemmassa siirtymisruudussa **Tiedot \> Yhteydet**.
    3. Muodosta yhteys soveltuviin esiintymiin seuraavissa kohteissa:

        - Dynamics 365
        - Dynamics 365 for Fin & Ops

4. Avaa [Power Apps -ympäristöt](https://admin.powerapps.com/environments) ja toimi seuraavasti:

    1. Valitse **Tietojen integrointiohjelma**.
    2. Valitse **Yhteysjoukot**.
    3. Valitse **Uusi yhteysjoukko**.
    4. Kirjoita yhteyden nimi.
    5. Valitse sopivat yhteydet seuraaville kohteille:

        - Dynamics 365
        - Dynamics 365 for Fin & Ops

    6. Valitse sopiva organisaation yhdistämismääritys.
    7. Valitse **Luo**.

5. Avaa [Power Apps -ympäristöt](https://admin.powerapps.com/environments) ja toimi seuraavasti:  

    1. Luo seuraavien mallien tietojen integrointiprojektit käyttämällä juuri luomaasi yhteysjoukkoa:

        - Asiakasmaksujen tietojen tulokset kävijä tietojen tulokset (CDS:stä Fin and Opsiin)
            - Jos käytössä on 10.0.17 tai myöhempi versio, sinun on käytettävä mallia nimeltään Asiakasmaksujen tiedot -tulos (CDS:stä Fin and Opsiin 10.0.17+).
        - Kassavirran aikasarjojen tulokset (CDS:stä Fin and Opsiin)
        - Budjetin aikasarjojen tulokset (CDS:stä Fin and Opsiin)

    2. Määritä kunkin projektin oikea ajoittaminen.

> [!NOTE]
> Jos pakolliset entiteetit eivät näy CDS:ssä, siirry kohtaan **Luotonvalvonta > Asetukset > Finance Insights > Finance Insights -parametrit**. Ota käyttöön Asiakasmaksun ennusteet -toiminto ja ja valitse **Luo ennustemalli**-painike. Kun tekoälymallin käyttöönotto on päättynyt (onnistunut tai epäonnistunut), integroinnin luomiseen tarvittavat CDS-entiteetit otetaan käyttöön CDS:ssä.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
