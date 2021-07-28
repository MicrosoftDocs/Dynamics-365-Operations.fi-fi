---
title: Kanavan määrittäminen kanavan siirtymishierarkian käyttämistä varten
description: Tässä aiheessa kuvataan, miten kanava määritetään kanavahierarkian käyttöä varten Microsoft Dynamics 365 Commercessa.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 79054573fa6f86bea5c4fe014233d71c01020348
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6352587"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a>Kanavan määrittäminen kanavan siirtymishierarkian käyttämistä varten


[!include [banner](includes/banner.md)]

Tässä aiheessa kuvataan, miten kanava määritetään kanavahierarkian käyttöä varten Microsoft Dynamics 365 Commercessa.

## <a name="overview"></a>Yleiskuvaus

Kanavien siirtymishierarkiat järjestävät tuotteet luokkiin, jotta tuotteita voi selata verkkokauppasivustolla tai myyntipisteissä. Vähittäismyynti- ja verkkokanavat on määritettävä kanavan siirtymishierarkioilla.

## <a name="configure-the-channel"></a>Kanavan määritys

Voit määrittää kanavan kanavan siirtymishierarkian käyttöä varten noudattamalla seuraavia ohjeita.

1. Siirry siirtymisruudussa kohtaan **Moduulit \> Vähittäismyynti ja kauppa \> Kanavan määritys \> Kanavaluokat ja tuotemääritteet**.
1. Valitse määritettävä kanava.
1. Valitse toimintoruudussa **Määritä määritteen metatiedot**.
1. Valitse avattavassa **Luokkahierarkia**-luettelossa asianmukainen kanavan siirtymishierarkia.
1. Valitse toimintoruudussa **Tallenna**.
1. Lisää **Määriteryhmä**-kohtaan määriteryhmiä, joita käytetään yleisinä määritteinä kaikille solmuille.

Seuraavassa kuvassa esitetään, miten kanava määritetään kanavan siirtymishierarkian käyttöä varten.

![Kanavan esimerkkimääritys.](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a>Määritä määritteen metatiedot

Määritteen metatietojen määrittäminen mahdollistaa kunkin solmun määritteiden määrittämisen.

Määritä määritteen metatiedot seuraavien ohjeiden mukaisesti.

1. Valitse toimintoruudussa **Määritä määritteen metatiedot**.
1. Valitse kullekin solmulle **Kanavan tuotemääritteet**.
1. Asta **Näytä määrite kanavassa**-asetuksen arvoksi **Kyllä** ja **Voidaan tarkistaa**-asetuksen arvoksi **Kyllä**, jotta kyseisessä kanavassa voidaan käyttää tarkentajia.
1. Kun olet määrittänyt kunkin solmun haluamallasi tavalla, tallenna määritykset valitsemalla **Toimintoruudussa** **Tallenna**-painike.
1. Poistu tästä ruudusta takaisin **Kanavaluokat ja tuotemääritteet** -sivulle valitsemalla oikean yläkulman **X**.

Seuraavassa kuvassa näkyy esimerkkijoukko kanavan tuotemääritteitä, jotka on määritetty kanavan luokkasolmussa.

![Kanavamääritteet kanavaluokkasolmussa.](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a>Julkaise muutokset

Sinun on julkaistava muutokset, jotta ne tulevat voimaan.

Julkaise muutokset seuraavien ohjeiden avulla.

1. Valitse toimintoruudussa **Julkaise kanavapäivitykset**.
1. Valitse **Julkaise kanavapäivitykset** -ruudussa **OK**.

Seuraavassa kuvassa näkyy, miten kanavapäivitykset julkaistaan.

![Julkaise kanavan päivitykset.](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a>Lisäresurssit

[Vähittäismyyntikanavan siirtymishierarkian luominen](create-channel-hierarchy.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]