---
title: Tietojen integrointiprojektin luominen (esiversio)
description: Tässä ohjeaiheessa kerrotaan, miten tietojen integrointiprojekti luodaan.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 050c4f0fe1aea07c3866e2e9d7a6db6c758205ca
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208506"
---
# <a name="create-a-data-integrator-project-preview"></a>Tietojen integrointiprojektin luominen (esiversio)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

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
        - Kassavirran aikasarjojen tulokset (CDS:stä Fin and Opsiin)
        - Budjetin aikasarjojen tulokset (CDS:stä Fin and Opsiin)

    2. Määritä kunkin projektin oikea ajoittaminen.

> [!NOTE]
> Jos pakolliset entiteetit eivät näy CDS:ssä, siirry kohtaan **Luotonvalvonta > Asetukset > Finance Insights > Finance Insights -parametrit**. Ota käyttöön Asiakasmaksun ennusteet -toiminto ja ja valitse **Luo ennustemalli**-painike. Kun tekoälymallin käyttöönotto on päättynyt (onnistunut tai epäonnistunut), integroinnin luomiseen tarvittavat CDS-entiteetit otetaan käyttöön CDS:ssä.

## <a name="privacy-notice"></a>Tietosuojatiedot

Esiversiot (1) voivat käyttää vähemmän tietosuojaa ja suojaustoimenpiteitä kuin Dynamics 365 Finance and Operations -palvelu, (2) eivät sisälly tämän huoltotilauksen palvelutasosopimukseen, (3) niitä ei ole tarkoitettu henkilötietojen tai muiden sellaisten tietojen käsittelemiseen, joihin liittyy lainsäädännön tai määräysten vaatimustenmukaisuusvaatimuksia ja (4) niillä on rajoitettu tuki.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]