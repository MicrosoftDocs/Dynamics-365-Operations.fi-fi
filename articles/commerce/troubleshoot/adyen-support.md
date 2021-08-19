---
title: Dynamics 365 Payment Connector Adyenia varten -ongelmien vianmääritys
description: Tämä ohjeaihe sisältää vianmäärityksen ohjeita, jotka voivat auttaa tuen saamiseen, kun Microsoft Dynamics 365 Payment Connector Adyenia varten -yhdistimeen liittyy ongelmia.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f40e29a17fe860440bd8192a89b0f5150f0db9ab213b2190f9deaf33a4f2aaba
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6743932"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a>Dynamics 365 Payment Connector Adyenia varten -ongelmien vianmääritys

[!include [banner](../../includes/banner.md)]

Tämä ohjeaihe sisältää vianmäärityksen ohjeita, jotka voivat auttaa tuen saamiseen, kun Microsoft Dynamics 365 Payment Connector Adyenia varten -yhdistimeen liittyy ongelmia.

## <a name="description"></a>kuvaus

Dynamics 365 Payment Connector Adyenia varten -liittimessä on ongelmia seuraavilla alueilla, ja tarvitset tukea Adyen-tiimiltä:

- Myyntipisteen (POS), Modernin myyntipisteen (MPOS), puhelinkeskuksen tai Dynamics 365 Commercen konfiguraatio
- Adyen-maksupalveluntarjoajan (PSP) viitenumero (esimerkiksi jos sinulla on kysymyksiä hylkäämisistä, mukaan lukien manuaaliset \[MKE\]-hylkäämiset)
- Mikä tahansa, joka ei toimi testi- tai live-kauppiasympäristöissä

## <a name="resolution"></a>Ratkaisu

Seuraavan sähköpostimallin avulla voit aloittaa tukiprosessin Adyen-tiimin kanssa. Voit nopeuttaa vianmääritystä varmistamalla, että sähköpostiviestissä on kaikki tarvittavat tiedot.

| Kenttä        | Arvo |
|--------------|-------|
| Loppupäivämäärä           | `support@adyen.com` |
| Kopio           | |
| Aiherivi | Microsoft Dynamics -tukipyyntö |
| Tekstiosa         | <p>Hei tukitiimi,</p><p>Pyydän tukea seuraavaan ongelmaan:</p><ul><li>Myyjän tili</li><li>Ympäristö (testi/tuotanto)</li><li>Kanava (myyntipiste/puhelinkeskus/Commercen sähköinen kauppa)</li><li>PSP-viitenumero, jos tapahtumaan liittyy tietty tapahtuma (voit löytää PSP-viitenumeron kuitista, Adyenin asiakasalueesta tai kassapäätteen tapahtumavalikosta).</li><li>Virhesanoman näyttökuva tai valokuva, jos käytettävissä</li><li>Tapahtumienvalvontalokit (.txt-muodossa)</li><li>Kuvaus ongelmasta ja kokeilemistasi vianmääritysvaiheista.</li></ul> |

## <a name="additional-resources"></a>Lisäresurssit

[Hyväksy maksuja Dynamics 365 Commercen Adyen-yhdistimen avulla](https://www.adyen.com/partners/dynamics-365-commerce)

[Dynamics 365 -maksuyhdistin Adyenia varten](../dev-itpro/adyen-connector.md)

[Dynamics 365:n Adyen-maksuyhdistimen määritys](https://docs.adyen.com/plugins/microsoft-dynamics)
