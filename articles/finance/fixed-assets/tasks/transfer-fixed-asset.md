---
title: Siirrä käyttöomaisuuserä
description: Tässä tehtäväoppaassa siirretään käyttöomaisuuskirjan taloushallinnon tiedot yhdestä taloushallinnon dimensiojoukosta uuteen taloushallinnon dimensiojoukkoon.
author: saraschi2
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7588e0058713d7facf053aa269210fc88e5a3ff2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823881"
---
# <a name="transfer-a-fixed-asset"></a>Siirrä käyttöomaisuuserä

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]