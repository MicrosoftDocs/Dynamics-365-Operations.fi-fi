---
title: Tuotteiden omistajat
description: Tässä artikkelissa on tietoja tuotteiden omistajista. Tuotteen omistaja on käyttäjäryhmä, joka vastaa tietyistä tuotteista. Vain ryhmän jäsenet voivat vapauttaa kyseisiä tuotteita. Tuotteen omistajaa voidaan käyttää myös hyväksynnän työnkulussa.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductOwner
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 5e09fdbbe14aa5a5ffbc5f07ae90b5d307a9e155
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907519"
---
# <a name="product-owners"></a>Tuotteiden omistajat

[!include [banner](../includes/banner.md)]

Tuotteen omistaja on käyttäjäryhmä, joka vastaa tietyistä tuotteista. Kun tuotteelle määritetään tuotteen omistajaryhmä, vain kyseisen ryhmän jäsenet voivat vapauttaa tuotteen. Tuotteen omistajaa voidaan käyttää myös hyväksynnän työnkulussa suunnittelun muutostenhallinnassa.

Tuotteen omistajat ovat yleisiä asetuksia. Niinpä ne ovat käytettävissä kaikissa yrityksissä.

## <a name="create-a-product-owner-group"></a>Tuotteen omistajaryhmän luominen

Tuotteen omistajaryhmä luodaan ja siihen lisätään jäseniä seuraavasti:

1. Valitse **Suunnittelun muutostenhallinta \> Määritys \> Tuotteen omistajat**.
2. Valitse toimintoruudussa **Uusi**.
3. Anna **Tuotteen omistaja** -kentässä ryhmän nimi.
4. Anna **Nimi**-kentässä ryhmän kuvaus.
5. Lisää **Jäsenet**-pikavälilehdessä työntekijöitä ryhmän jäseniksi.

## <a name="assign-a-product-owner-to-a-product"></a>Tuotteen omistajan määrittäminen tuotteen omistajalle

Tuotteen omistaja määritetään tuotteelle seuraavasti:

1. Avaa liittyvän tuotteen tai päätuotteen **Tuotetiedot**-sivu.
1. Määritä **Yleinen**-välilehden **Tuotteen omistaja** -kentässä kyseisen tuotteen omistajaryhmän nimi.

Kun tuotteen omistajaa määritetään tuotteelle, vain tuotteen omistajaryhmän jäsenet voivat muokata **Tuotteen omistaja** -asetusta.

Tuotteen omistaja näkyy myös **Vapautetut tuotteet** -sivulla.

## <a name="product-owners-and-product-releases"></a>Tuotteen omistajat ja tuotteen vapautukset

Vain tuotteen tuotteen omistajaryhmän jäsenet voivat vapauttaa kyseisen tuotteen. Poikkeuksena on kuitenkin tilanne, jossa tuote on alinimike ja sen päätuotteen omistaja julkaisee päätuotteen. Jos tuote on siis toisen tuotteen tuoterakenteen osa, järjestelmä ei tarkista kunkin tuoterakenteen nimikkeen tuotteen omistajaa. Se tarkistaa vain päänimikkeen tuotteen omistajan.

Tuote X on esimerkiksi määritetty *Design-kaiuttimet*-tuotteen omistajaryhmään. Tuote X on myös tuotteen Y tuoterakenteen osa, ja tuote Y on määritetty *Design-kaiuttimet*-tuotteen omistajaryhmään. Jos *Design-kaiuttimet*-tuotteen omistajaryhmä vapauttaa tuotteen Y ja sen tuoterakenteen, tuote X vapautetaan yhdessä tuotteen Y kanssa.

## <a name="product-owners-and-approvals"></a>Tuotteen omistajat ja hyväksynnät

Koska tuotteen omistajat tietävät, onko tietystä suunnittelun muutoksesta hyötyä tuotteille, heidät kannattaa usein sisällyttää suunnittelun muutostenhallinnan hyväksyntäprosessiin. Se voidaan toteuttaa määrittämällä tuotteen omistajat osallistujiksi työnkuluissa, joita käytetään suunnittelun muutostenhallinnassa. Järjestelmä määrittää sitten hyväksyntätehtäviä työnkuluissa suunnittelun muutospyyntöjen ja muutostilausten tuotteiden perusteella. Lisätietoja on kohdassa [Suunnittelutuotteiden muutosten hallinta](engineering-change-management.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]