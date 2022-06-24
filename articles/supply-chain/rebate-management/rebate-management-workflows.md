---
title: Ostohyvitysten hallintasopimuksen työnkulut
description: Tässä artikkelissa on tietoja sopimusten hyväksymis- ja aktivointityönkulun määrittäminen ostohyvitysten hallintasopimuksia varten.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2b1611ff7877efc4a2f98b8f84a1ef91971902ab
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869514"
---
# <a name="rebate-management-deal-workflows"></a>Ostohyvitysten hallintasopimuksen työnkulut

[!include [banner](../includes/banner.md)]

Ostohyvitysten hallinnassa voit hyväksyä ostohyvityssopimuksia samalla työnkulkuympäristöllä kuin muut talous- ja toimintosovellukset. Jokaiseen työnkulkuun liittyy kaksi työprosessia:

- Yksi työnkulun elementeistä hyväksyy sopimuksen.
- Yksi työnkulun elementti aktivoi sopimuksen, jotta käyttäjä tai työnkulkuprosessi voi hyväksyä tapahtumat.

Ennen ostohyvityssopimuksen käyttöä sen on oltava aktiivinen **Ostohyvityksen hallinta** -moduulissa. Voit aktivoida sopimuksen luomalla ja konfiguroimalla *ostohyvityksen hallintasopimuksen työnkulun*.

Käyttäjät eivät voi hyväksyä tarjouksia manuaalisesti. Työnkulkua on käytettävä aina.

## <a name="create-and-manage-rebate-management-deal-workflows"></a>Ostohyvitysten hallintasopimuksen työnkulkujen luonti ja hallinta

Voit käyttää ostohyvityksen hallintasopimuksen työnkulkuja kohdassa **Ostohyvitysten hallinta \> Asetukset \> Ostohyvitysten hallinnan työnkulut**. Siinä voit tarkastella, luoda ja päivittää työnkulkuja tarpeen mukaan. Vain yksi tämän tyyppinen työnkulku voi olla aktiivinen kerrallaan. Lisätietoja työnkuluista, **Ostohyvityksen hallinnan työnkulut** -sivun käyttämisestä ja työnkulkujen luomisesta on [työnkulkujärjestelmän yhteenvedossa](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) sekä siihen liittyvissä artikkeleissa.

## <a name="use-a-workflow-to-activate-a-deal"></a>Työnkulun käyttäminen sopimuksen aktivoimiseen

Voit aktivoida sopimuksen työnkulun kautta avaamalla sopimuksen (esimerkiksi **Kaikki ostohyvityksen hallintasopimukset** -sivulla). Valitse siten toimintoruudussa **Työnkulku \> Lähetä**. Kun uusi sopimus on käsitelty ja hyväksytty työnkulun kautta, se on aktiivinen ja valmis käytettäväksi.

Kun sopimus on aktivoitu, et voi muuttaa useimpia sen asetuksista. Jos haluat muuttaa aktiivista sopimusta, poista se ensin käytöstä ja luo sitten uusi sopimus. Jos uusi sopimus muistuttaa vanhaa sopimusta, voit luoda sen kopioimalla vanhan sopimuksen.

Voit muuttaa seuraavia sopimuksen asetuksia sen aktivoinnin jälkeen:

- Täsmäytä
- Kumulatiivinen takuu
- Kirjausprofiili
- Takuun kirjausprofiili
- Tiedoston huomautukset
- Valuutta
- Päivämäärästä
- Päivämäärään

Lisäksi ostohyvitysrivit voidaan poistaa.
