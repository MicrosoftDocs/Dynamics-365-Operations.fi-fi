---
title: Määritä veroryhmät
description: Tässä artikkelissa kuvataan, miten veroryhmät määritetään Veron laskenta -palvelussa.
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
ms.openlocfilehash: 89c5670ee7e78f2dc51f128c3ae8d284bb6b925b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862896"
---
# <a name="set-up-tax-groups"></a>Määritä veroryhmät

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan, miten veroryhmät määritetään Veron laskenta -palvelussa. Se myös kertoo, miten veroryhmän käytettävyyssäännön matriisi määritetään ja rivejä konfiguroidaan matriisissa.

Arvonlisäveron laskentapalvelun veroryhmien käsite muistuttaa arvonlisäveroryhmien käsitettä Microsoft Dynamics 365 Financessa. Ne ovat verokoodien ryhmiä. Veron laskentapalvelu määrittää verokoodit veroryhmän ja nimikkeen veroryhmän välityksen avulla.

Veron laskentapalvelun veroryhmät eroavat kuitenkin taloushallinnon arvonlisäveroryhmistä siinä, ettei niille ole lisäparametreja, kuten **Käyttövero** ja **Veroton vero**. Sen sijaan parametrit ovat käytettävissä verokooditasolla.

> [!IMPORTANT]
> Veroryhmien määrittäminen Veron laskentapalvelussa on yrityksestä riippumaton. Nämä asetukset voi tehdä Regulatory Configuration Service (RCS) -palvelussa vain kerran. Kun otat veron laskentapalvelun käyttöön taloushallinnon palvelussa, veroryhmät synkronoidaan automaattisesti valitun yrityksen osalta.

## <a name="set-up-a-tax-group"></a>Veroryhmän määrittäminen

Määritä veroryhmä noudattamalla seuraavia ohjeita.

1. Kirjaudu [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/) -palveluun.
2. Siirry kohtaan **Työtilat** \> **Globalisointiominaisuudet** \> **Veronlaskenta**.
3. Valitse määritettävä ominaisuus ja versio ja valitse sitten **Muokkaa**.
4. Valitse **Yleiset**-välilehdestä **Konfiguraatioversio**.
5. Valitse **Veroryhmä**-välilehdessä **Hallitse saraketta**. Jos määrität veroryhmää ensimmäistä kertaa, **Sarakkeen hallinta** -valintaikkunan kentät määritetään automaattisesti.
6. Laajenna vasemmanpuoleisen luettelon **Rivit**-solmu ja valitse **Veroryhmä**-valintaruutu.

    ![Sarakkeiden hallinta -valintaikkunan Rivit-solmusta valittu veroryhmä.](media/select-tax-group.png)

7. Lisää **Veroryhmä** oikealla olevaan **Valitut sarakkeet** -luetteloon valitsemalla oikea nuolipainike.

    ![Valittuun sarakeluetteloon lisätty veroryhmä.](media/add-tax-group.png)

8. Valitse **OK**.

## <a name="configure-a-tax-group"></a>Veroryhmän määrittäminen

Kun veroryhmä on määritetty, veroryhmäjärjestelmä luo käytettävyyssäännön matriisin. Voit konfiguroida veroryhmän lisäämällä matriisiin rivejä.

1. Valitse **Veroryhmä**-välilehdellä **Lisää**.
2. Syötä **Veroryhmä**-kenttään veroryhmän nimi.

    > [!IMPORTANT]
    > On suositeltavaa rajoittaa veroryhmän nimeä niin, että siinä on enintään 10 merkkiä. Tämä nimi synkronoidaan taloushallinnon kanssa, ja sen arvonlisäveroryhmien nimissä on enintään 10 merkkiä.

3. Valitse **Verokoodit**-kentästä niiden verokoodien valintaruudut, jotka haluat sisällyttää veroryhmään. Voit sisällyttää yhteen veroryhmään useita verokoodeja.

    ![Useita Verokoodit-kentässä valittuja verokoodeja.](media/multiple-tax-codes-selection.png)

4. Voit lisätä veroryhmiä toistamalla kohtien 1–3 toimet.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
