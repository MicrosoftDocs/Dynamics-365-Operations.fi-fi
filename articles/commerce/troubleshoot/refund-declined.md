---
title: Palautustilauksen palautus on hylätty
description: Tämä artikkeli antaa vianmääritysohjeet, jotka voivat auttaa palautustilauksen palautuksen hylkäämisen yhteydessä, jos laskutuksessa käytetty luottokortti eroaa alkuperäisen maksun varmennuksessa käytetystä kortista.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: d8d1c40673d4b159a7b7bf00bf6011ba45f47edd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268229"
---
# <a name="refund-on-a-return-order-is-declined"></a>Palautustilauksen palautus on hylätty

[!include [banner](../../includes/banner.md)]

Tämä artikkeli antaa vianmääritysohjeet, jotka voivat auttaa palautustilauksen palautuksen hylkäämisen yhteydessä, jos laskutuksessa käytetty luottokortti eroaa alkuperäisen maksun varmennuksessa käytetystä kortista.

## <a name="description"></a>kuvaus

Hyvitys hylätään, kun palautustilauksen laskussa käytetty luottokortti eroaa alkuperäisen maksun varmennuksessa käytetystä kortista. Näyttöön tulee seuraava virhesanoma: "Jotkin maksut eivät ole oikeassa tilassa kirjausta varten. Tarkista kaikkien maksujen tila uudelleen ennen laskutusta."

Maksun varmennustiedot sisältävät seuraavan virhesanoman: "Adyen-yhdyskäytävän SendRequest() epäonnistui. Tila: 'InternalServerError'.22144; Adyen palautti tyhjän vastauksen.(22001);"

![Hylätty palautustilauksen palautus -virhe.](media/refund-order-decline.jpg)

## <a name="resolution"></a>Ratkaisu

### <a name="enable-blind-returns-in-adyen"></a>Sokkopalautusten käyttöönotto Adyenissa

Voit ottaa sokkopalautukset käyttöön noudattamalla [Dynamics 365 Payment Connector Adyenia varten – vianmääritys](adyen-support.md) -ohjeen vaiheita, jotta voit ottaa yhteyttä Adyenin tukiryhmään ja pyytää, että sokkopalautukset otetaan käyttöön Adyen-myyjätilillä.

## <a name="additional-resources"></a>Lisäresurssit

[Dynamics 365 -maksuyhdistin Adyenia varten](../dev-itpro/adyen-connector.md)

[Dynamics 365:n Adyen-maksuyhdistimen määritys](https://docs.adyen.com/plugins/microsoft-dynamics)
