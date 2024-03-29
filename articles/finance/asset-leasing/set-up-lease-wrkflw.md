---
title: Vuokrasopimuksen hyväksyntätyönkulkujen määrittäminen
description: Tässä artikkelissa kerrotaan, miten uuden vuokrasopimuksen luomisen yhteydessä suoritettava hyväksynnän työnkulku määritetään.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0162e559f8aaec248cfb9042b0152788536c9fc9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870275"
---
# <a name="set-up-lease-approval-workflows"></a>Vuokrasopimuksen hyväksyntätyönkulkujen määrittäminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten uuden vuokrasopimuksen luomisen yhteydessä suoritettava hyväksynnän työnkulku määritetään. Lisätietoja työnkulun käyttämisestä on kohdassa [Vuokrasopimuksen hyväksyntätyönkulkujen käyttäminen](use-create-lease-wrkflw.md). 

1. Siirry kohtaan **Resurssin vuokraus \> Asetukset \> Vuokrauksen työnkulku**.
2. Valitse **Vuokrauksen työnkulku** -sivulla **Uusi**.
3. Valitse näkyviin tulevasta valintaikkunasta **Työnkulun tyyppi** -kohdassa **Vuokrauksen työnkulku** -linkki.

    Sovellus avataan. Kun se on suoritettu, kirjaudu sisään Azure Active Directoryyn (Azure AD). Sinut ohjataan työnkulun sovellukseen.

4. Vedä **Vuokrauksen työnkulun hyväksyntä** -elementti työkulkuun.
5. Yhdistä yksi solmu **alusta** **vuokrauksen työnkulun hyväksyntään**. Yhdistä sitten **vuokrauksen työnkulun hyväksyntä** **loppuun**.
6. Kaksoisnapsauta **Vuokrauksen työnkulun hyväksyntä** -kohtaa.
7. Valitse **Ominaisuudet** ja anna **Perustiedot**-kohdassa työnkulun nimi.

    Tällä sivulla voit myös määrittää lisäparametreja työnkulkua varten. Jos olet ottanut **automaattiset toiminnot** käyttöön, järjestelmä tekee automaattisesti tietyn toimenpiteen. Ilmoitukset voidaan lähettää, jos ne on määritetty **Ilmoitukset**-välilehdessä. **Lisäasetukset**-välilehdessä voit määrittää lopullisen hyväksyjän, asettaa aikarajan ja määrittää tietyt toimenpiteet, jotka on suoritettava.

8. Kun olet määrittänyt työnkulun parametrit, valitse **Sulje**.
9. Valitse **Vaihe 1** ja valitse sitten **Ominaisuudet**.
10. Anna **Perusasetukset**-kohdassa vaiheen nimi, luo hyväksyttävä aiherivi ja määritä hyväksynnän ohjeet.
11. Valitse **Määritys**-sivulla määrityksen tyyppi.
12. Jos haluat määrittää hyväksyntään tiettyjä käyttäjiä, valitse **Käyttäjä**, valitse sitten vuokrasopimukset hyväksyvät käyttäjät. Valitse lopuksi **Sulje**.
13. Luo työnkulku valitsemalla **Tallenna ja sulje**. Valitse pyydettäessä **OK**.
14. Valitse **Luo työnkulku** -sivulla **Sulje**.
14. Valitse uusi työnkulku ja valitse sitten **Versiot**. Varmista sitten, että työnkulku on aktiivinen, valitsemalla **Aktivoi**.
15. Valitse **Sulje**. Uusi aktiivinen versio tulee näkyviin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
