---
title: Tietojen integrointiprojektin luominen
description: Tässä aiheessa käsitellään tietojen integrointiprojekti luontia.
author: ShivamPandey-msft
ms.date: 05/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 4d69ffcb6ccfcc7bae2891f2539941f7b6bbf86e
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722880"
---
# <a name="create-a-data-integration-project"></a>Tietojen integrointiprojektin luominen

[!include [banner](../includes/banner.md)]

Tässä aiheessa käsitellään tietojen integrointiprojekti luontia.

1. Kirjaudu Microsoft Dynamics 365 Financeen.
2. Siirry kohtaan **Työtilat \> Tietojen hallinta** ja valitse **Tietoyksiköt**. Odota, kunnes kaikki tietoyksiköt on päivitetty, ennen kuin siirryt seuraavaan vaiheeseen.
3. Avaa [Power Apps -portaali](https://make.powerapps.com/) ja toimi seuraavasti:

    1. Valitse sopiva ympäristö.
    2. Valitse vasemmassa siirtymisruudussa **Dataverse \> Yhteydet**.
    3. Muodosta yhteys soveltuviin esiintymiin seuraavissa kohteissa:

        - Dynamics 365
        - Dynamics 365 for Fin & Ops

4. Avaa [Power Apps -ympäristöt](https://admin.powerapps.com/environments) ja toimi seuraavasti:

    1. Valitse **Tietojen integrointi**.
    2. Valitse **Yhteysjoukot**.
    3. Valitse **Uusi yhteysjoukko**.
    4. Kirjoita yhteyden nimi.
    5. Valitse sopivat yhteydet seuraaville kohteille:

        - Dynamics 365
        - Dynamics 365 for Fin & Ops

    6. Valitse sopiva organisaation yhdistämismääritys.
    7. Valitse **Luo**.

5. Avaa [Power Apps -ympäristöt](https://admin.powerapps.com/environments) ja toimi seuraavasti:  

    1. Luo kunkin seuraavan mallin yksittäinen tietojen integrointiprojekti käyttämällä juuri luomaasi yhteysjoukkoa:

        - Asiakasmaksun merkitykselliset tiedot (CDS:stä Fin and Opsin 10.0.17 ja sitä uudempiin versioihin)
        - Kassavirran aikasarjojen tulokset (CDS:stä Fin and Opsiin)
        - Budjetin aikasarjojen tulokset (CDS:stä Fin and Opsiin)

      > [!NOTE]
      > Useiden tietojen integrointiprojektien luominen kuhunkin malliin saattaa aiheuttaa virheitä, jotka estävät päivitykset.

    2. Määritä kunkin projektin oikea ajoittaminen.

> [!NOTE]
> Jos pakolliset entiteetit eivät näy Dataversessä, siirry kohtaan **Luotonvalvonta** > **Asetukset** > **Finance Insights** > **Finance insights -parametrit**. Ota käyttöön **Asiakasmaksun ennusteet** -toiminto ja valitse **Luo ennustemalli**. Kun tekoälymallin käyttöönotto on päättynyt (onnistunut tai epäonnistunut), integroinnin luomiseen tarvittavat Dataverse-entiteetit otetaan käyttöön.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
