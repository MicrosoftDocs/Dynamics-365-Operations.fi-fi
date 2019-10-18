---
title: Siirrä käyttöomaisuuserä
description: Tässä tehtäväoppaassa siirretään käyttöomaisuuskirjan taloushallinnon tiedot yhdestä taloushallinnon dimensiojoukosta uuteen taloushallinnon dimensiojoukkoon.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 167591cf160916f256e2d10f122eca312ba07639
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186828"
---
# <a name="transfer-a-fixed-asset"></a>Siirrä käyttöomaisuuserä

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä tehtäväoppaassa siirretään käyttöomaisuuskirjan taloushallinnon tiedot yhdestä taloushallinnon dimensiojoukosta uuteen taloushallinnon dimensiojoukkoon.  Siinä käytetään kirjanpitäjän roolia ja USMF-yrityksen esittelytietoja.

1. Siirry siirtymisruudussa kohtaan **Moduulit > Käyttöomaisuuserät > Käyttöomaisuuserät > Käyttöomaisuuserät**.
2. Etsi ja valitse luettelosta siirrettävä käyttöomaisuus.
3. Valitse toimintoruudussa **Käyttöomaisuus**.
4. Valitse **Siirrä käyttöomaisuudet**.
5. Kirjoita päivämäärä **Siirtopäivä**-kenttään.
6. Syötä siirtoa kuvaavia kommentteja.
    
    Tässä luettelossa on kaikki käyttöomaisuuden kirjat.  
7. Merkitse uuteen taloushallinnon dimensioon siirrettävät kirjat.
    * Tässä luettelossa on valitun kirjan aiemmin luodut taloushallinnon dimensioiden arvot.  
    * Valitse valitun käyttöomaisuuskirjan päivitettävä taloushallinnon dimensio.  
8. Avaa haku valitsemalla **Taloushallinnon dimensio** -kentässä avattavan valikon painike.
    * Määritä tarvittaessa muut taloushallinnon dimensiot.  
    * Kaikki taloushallinnon dimension arvot muuttuvat siirron yhteydessä siitä huolimatta, onko arvo syötetty vai onko kohta jätetty tyhjäksi. Ajatellaan, että syötit arvon BusinessUnit-kohteelle, mutta jätit CostCenter- ja Department-kohteen taloushallinnon dimensiot tyhjiksi. Jos tilirakenne sallii CostCenter-kohteen ja Department-kohteen tyhjät arvot, siirron yhteydessä jokainen BusinessUnit-kohteen arvomalli saa uuden arvon. CostCenter ja Department jäävät tyhjiksi.  
9. Valitse **Päivitä**.
    * Voit esikatsella muutoksia ennen siirron tekemistä.  
    * Tarkastele tuloksia, ennen kuin siirrät käyttöomaisuuskirjat.  
10. Valitse **Siirrä**.

