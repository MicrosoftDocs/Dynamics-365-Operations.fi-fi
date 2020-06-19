---
title: Toimittajan maksupidätysehtojen luominen ja käyttäminen
description: Tässä ohjeaiheessa on tietoja toimittajamaksuissa olevien säilytysehtojen määrittämisestä ja ylläpidosta.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 0e14050a79220b5d02763a025040edb934489d00
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410217"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Toimittajan maksupidätysehtojen luominen ja käyttäminen

[!include [banner](../includes/banner.md)] 

Toimittajamaksun pidätysehtojen määrittäminen projektille on hyödyllistä, kun organisaatio haluaa säilyttää osan toimittajalle tehdyistä maksuista. Jos esimerkiksi haluat pidättää maksuja toimittajalle, kunnes toimitetut tuotteet vastaavat odotuksiasi. Toimittajan maksuehtojen pidätysehdot voidaan määrittää, kun neuvottelet toimittajan kanssa.

## <a name="create-vendor-payment-retention-terms"></a>Toimittajan maksun pidättämisehtojen luominen

Voit syöttää toimittajamaksun prosenttiosuuden pidätettäväksi ja prosenttiosuuden aiemmin pidätetystä summasta vapautettavaksi. Summat säilytetään automaattisesti toimittajan laskuissa, kunnes sopimus saavuttaa tietyn täyttymistilan. Kun olet määrittänyt pidätysehdot, voit soveltaa niitä mihin tahansa projektiin tälle toimittajalle.

Käytä seuraavia vaiheita määrittääksesi ja ylläpitääksesi toimittajamaksujen ehtoja. 

1. Siirry kohtaan **Projektinhallinta ja kirjanpito** > **Pidättäminen** > **Toimittajamaksujen pidätysehdot**.
2. Valitse **Uusi** lisätäksesi uudet toimittajan pidätysehdot. **Säännön tunnus** -arvo uudelle termille lisätään automaattisesti. 
3. Kirjoita lyhyt kuvaus **Kuvaus**-kenttään ja valitse **Ehdot**-pikavälilehdessä **Lisää rivi**, niin voit määrittää termin arvot seuraaville:

   - **Toimitettujen yksiköiden prosenttiosuus**: Syötä termin valmistumisprosentti. Summat säilytetään automaattisesti toimittajalaskuissa, kunnes valmistumisprosentin vaihe vastaa määritettyä prosenttiosuutta. Esimerkiksi jos kirjoitat 50,00, määrät säilytetään, kunnes projektista 50 prosenttia on valmiina.
   - **Pidätettävä prosenttiosuus**: Syötä toimittajan laskutussumman pidätettävä prosenttiosuus. Esimerkiksi jos syötät arvon 10,00, 10 prosenttia toimittajalaskun summasta pidätetään, kunnes projekti saavuttaa valmistumisprosentin, jonka olet asettanut **Toimitettujen yksiköiden prosenttiosuus** -kenttään.
   - **Vapautettava prosenttiosuus**: Valitse **Lisää rivi** lisätäksesi prosenttiosuuden mistä tahansa aiemmin pidätetyistä summista vapautettavaksi projektin valmistumisen valitulla tasolla.

> [!NOTE]
> Jos sinulla on useita projektin eri tasojen valmistumisen välitavoitteita, syötä erillinen toimittajan pidätysehdon rivi kuhunkin pidätyssääntöön. Kullekin riville voidaan määrittää eri pidätysprosenttiosuus ja eri vapautusprosenttiosuus kullekin nimetylle projektin valmistumisasteen tasolle.

Kun olet luonut toimittajan pidätysehdot toimittajalle, voit soveltaa ehtoja projektiin.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Sovella toimittajan pidätysehtoja projektiin

1. Siirry kohtaan **Projektinhallinta ja kirjanpito** > **Projektit** > **Kaikki projektit** ja avaa projekti projektiluettelosivulla.
2. Valitse **Toimittajasopimukset** -pikavälilehdessä **Lisää rivi**.
3. Valitse **Tilikoodi**-kentästä jokin seuraavista vaihtoehdoista: 

   - **Taulukko**: Toimittajan pidätysehtoja sovelletaan yhteen toimittajaan.
   - **Ryhmä**: Toimittajan pidätysehtoja sovelletaan kaikkiin toimittajaryhmän toimittajiin.
   - **Kaikki**: Toimittajan pidätysehtoja sovelletaan kaikkiin toimittajiin.

4. Valitse **Toimittaja tai toimittajaryhmä** -kentässä toimittaja tai toimittajaryhmä, johon toimittajan pidätysehtoja sovelletaan. Jos olet valinnut **Kaikki** edellisessä vaiheessa, tämä kenttä ei ole käytettävissä.
5. Valitse **Toimittajan pidätysehdot** -kentästä pidätysehdot, jotka loit edellisessä menettelyssä.
6. Jos projektissa on toimittajalle myös määritetty Maksa, kun maksettu -ehdot (PWP), syötä kynnysprosenttiarvo projektille **PWP-kynnysprosenttiarvo**-kentässä.

Toimittajan pidätysehdot näkyvät myös ostotilauksissa, jotka luot toimittajalle.
