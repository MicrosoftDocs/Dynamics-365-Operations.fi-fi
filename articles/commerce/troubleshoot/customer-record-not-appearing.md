---
title: Asiakastietueet eivät näy Commerce headquarters -sovelluksessa
description: Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa silloin, kun asiakastietueet eivät näy heti Commerce headquarters -sovelluksessa.
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
ms.openlocfilehash: b8d065dd104df616ba8f10f7813e74c900fdcf77
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018479"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a>Asiakastietueet eivät näy Commerce headquarters -sovelluksessa

[!include [banner](../../includes/banner.md)]

Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa silloin, kun asiakastietueet eivät näy heti Commerce headquarters -sovelluksessa.

## <a name="description"></a>kuvaus

Kun luot uuden asiakastietueen käyttämällä sähköisen kaupan myymälän kirjautumistyönkulkua, vastaava asiakastietue ei näy heti Commerce headquarters -sovelluksessa.

## <a name="resolution"></a>Ratkaisu

### <a name="disable-customer-creation-in-async-mode"></a>Poista käytöstä asiakkaan luonti asynkronisessa tilassa

> [!IMPORTANT]
> Jos poistat asynkronisen asiakkaan luonnin käytöstä, järjestelmän suorituskyky voi heiketä, koska kunkin tietueen luominen luo reaaliaikaisen pyynnön Commerce headquartersiin. Jos lisäksi Commerce headquarters ei ole käytössä (esimerkiksi huoltotyönkulkujen yhteydessä), uusien asiakkaiden luontivirroissa syntyy virheitä.

Voit poistaa asiakkaan asynkronisen luonnin käytöstä Commerce headquarters -ohjelmassa noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Verkkokaupan asetukset \> Toimintoprofiilit**.
1. Jos et vielä käytä online-kanavassasi toimintoprofiilia, luo sellainen.
1. Varmista, että **Luo asiakas asynkronisessa tilassa** -asetuksena on **Ei**.
1. Valitse **Retail ja Commerce \> Kanavat \> Verkkokaupat**.
1. Valitse online-myymälä, jossa asynkroninen asiakkaan luonti poistetaan käytöstä.
1. Varmista **Yleiset**-välilehdessä, että **Toimintoprofiili**-kentän arvoksi tulee online-kanavaa varten käytössä oleva toimintoprofiili.

## <a name="additional-resources"></a>Lisäresurssit

[Kuluttajakaupan vuokraajan määrittäminen Commercessa](../set-up-b2c-tenant.md)
