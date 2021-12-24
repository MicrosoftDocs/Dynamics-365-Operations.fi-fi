---
title: Määritä nimikkeiden veroryhmät
description: Tässä aiheessa kuvataan, miten nimikkeen veroryhmät määritetään Veron laskenta -palvelussa.
author: wangchen
ms.date: 11/30/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 88dd8e2fd9d4d4e5172dcc7b1bd27a70a2f59f03
ms.sourcegitcommit: 62ca651c94e61aaa69cfa59e861f263f89d01c4a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2021
ms.locfileid: "7883854"
---
# <a name="set-up-item-tax-groups"></a>Määritä nimikkeiden veroryhmät

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, miten nimikkeen veroryhmät määritetään Veron laskenta -palvelussa. Se myös kertoo, miten nimikkeen veroryhmän käytettävyyssäännön matriisi määritetään ja rivejä konfiguroidaan matriisissa.

Arvonlisäveron laskentapalvelun nimikkeen veroryhmien käsite muistuttaa nimikkeen arvonlisäveroryhmien käsitettä Microsoft Dynamics 365 Financessa. Ne ovat verokoodien ryhmiä. Veron laskentapalvelu määrittää verokoodit veroryhmän ja nimikkeen veroryhmän välityksen avulla.

> [!IMPORTANT]
> Nimikkeen veroryhmien määrittäminen Veron laskentapalvelussa on yrityksestä riippumaton. Nämä asetukset voi tehdä Regulatory Configuration Service (RCS) -palvelussa vain kerran. Kun otat veron laskentapalvelun käyttöön taloushallinnon palvelussa, nimikkeen veroryhmät synkronoidaan automaattisesti valitun yrityksen osalta.

## <a name="set-up-an-item-tax-group"></a>Määritä nimikkeiden veroryhmä 

Määritä nimikkeen veroryhmä noudattamalla seuraavia ohjeita.

1. Kirjaudu [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/) -palveluun.
2. Siirry kohtaan **Työtilat** \> **Globalisointiominaisuudet** \> **Veronlaskenta**.
3. Valitse määritettävä ominaisuus ja versio ja valitse sitten **Muokkaa**.
4. Valitse **Yleiset**-välilehdestä **Konfiguraatioversio**.
5. Valitse **Nimikkeen veroryhmä** -välilehdessä **Hallitse saraketta**. Jos määrität nimikkeen veroryhmää ensimmäistä kertaa, **Sarakkeen hallinta** -valintaikkunan kentät määritetään automaattisesti.
6. Laajenna vasemmanpuoleisen luettelon **Rivit**-solmu ja valitse **Nimikkeen veroryhmä** -valintaruutu.

    ![Sarakkeiden hallinta -valintaikkunan Rivit-solmusta valittu nimikkeen veroryhmä.](media/select-item-tax-group.png)

7. Lisää **Nimikeveroryhmä** oikealla olevaan **Valitut sarakkeet** -luetteloon valitsemalla oikea nuolipainike.

    ![Valittuun sarakeluetteloon lisätty nimikkeen veroryhmä.](media/add-item-tax-group.png)

8. Valitse **OK**.

## <a name="configure-an-item-tax-group"></a>Määritä nimikkeiden veroryhmä

Kun nimikkeen veroryhmä on määritetty, järjestelmä luo käytettävyyssäännön matriisin. Voit konfiguroida nimikkeen veroryhmän lisäämällä matriisiin rivejä.

1. Valitse **Nimikkeen veroryhmä** -välilehdessä **Lisää**.
2. Syötä **Nimikkeen veroryhmä** -kenttään nimikkeen veroryhmän nimi.

    > [!IMPORTANT]
    > On suositeltavaa rajoittaa nimikkeen veroryhmän nimeä niin, että siinä on enintään 10 merkkiä. Tämä nimi synkronoidaan taloushallinnon kanssa, ja sen arvonlisäveroryhmien nimissä on enintään 10 merkkiä.

3. Valitse **Verokoodit**-kentästä niiden verokoodien valintaruudut, jotka haluat sisällyttää nimikkeen veroryhmään. Voit sisällyttää yhteen nimikkeen veroryhmään useita verokoodeja.

    ![Useita Verokoodit-kentässä valittuja verokoodeja.](media/multiple-tax-codes-selection.png)

4. Toista kohtien 1–3 toimet lisätäksesi nimikkeitä veroryhmiin.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
