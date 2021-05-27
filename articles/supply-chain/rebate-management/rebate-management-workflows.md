---
title: Ostohyvitysten hallintasopimuksen työnkulut
description: Tässä ohjeaiheessa on tietoja sopimusten hyväksymis- ja aktivointityönkulun määrittäminen ostohyvitysten hallintasopimuksia varten.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: ee342de6d069131e230120c5d65aef58da8e632a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020383"
---
# <a name="rebate-management-deal-workflows"></a>Ostohyvitysten hallintasopimuksen työnkulut

[!include [banner](../includes/banner.md)]

Ostohyvitysten hallinnassa voit hyväksyä ostohyvityssopimuksia samalla työnkulkuympäristöllä kuin muut Finance and Operations -sovellukset. Jokaiseen työnkulkuun liittyy kaksi työprosessia:

- Yksi työnkulun elementti aktivoi sopimuksen, jotta käyttäjä tai työnkulkuprosessi voi hyväksyä tapahtumat.
- Yksi työnkulun elementeistä hyväksyy sopimuksen.

Ennen ostohyvityssopimuksen käyttöä sen on oltava aktiivinen **Ostohyvityksen hallinta** -moduulissa. Voit aktivoida sopimuksen luomalla ja konfiguroimalla *ostohyvityksen hallintasopimuksen työnkulun*.

Kun työnkulku on aktivoitu ostohyvitysten hallinnassa, käyttäjät eivät voi hyväksyä tarjouksia manuaalisesti. Työnkulkua on käytettävä aina.

## <a name="create-and-manage-rebate-management-deal-workflows"></a>Ostohyvitysten hallintasopimuksen työnkulkujen luonti ja hallinta

Voit käyttää ostohyvityksen hallintasopimuksen työnkulkuja kohdassa **Ostohyvitysten hallinta \> Asetukset \> Ostohyvitysten hallinnan työnkulut**. Siinä voit tarkastella, luoda ja päivittää työnkulkuja tarpeen mukaan. Vain yksi tämän tyyppinen työnkulku voi olla aktiivinen kerrallaan. Lisätietoja työnkuluista, **Ostohyvityksen hallinnan työnkulut** -sivun käyttämisestä ja työnkulkujen luomisesta on [työnkulkujärjestelmän yhteenvedossa](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) sekä siihen liittyvissä ohjeaiheissa.

## <a name="use-a-workflow-to-activate-a-deal"></a>Työnkulun käyttäminen sopimuksen aktivoimiseen

Voit aktivoida sopimuksen työnkulun kautta avaamalla sopimuksen (esimerkiksi **Kaikki ostohyvityksen hallintasopimukset** -sivulla). Valitse siten toimintoruudussa **Työnkulku \> Lähetä**. Kun uusi sopimus on käsitelty ja hyväksytty työnkulun kautta, se on aktiivinen ja valmis käytettäväksi.

Kun sopimus on aktivoitu, et voi muuttaa sen asetuksia. Jos haluat muuttaa aktiivista sopimusta, poista se käytöstä ja luo sitten uusi sopimus. Jos uusi sopimus muistuttaa vanhaa sopimusta, voit luoda sen kopioimalla vanhan sopimuksen.
