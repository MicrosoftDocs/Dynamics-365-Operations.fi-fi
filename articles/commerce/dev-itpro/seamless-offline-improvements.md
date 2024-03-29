---
title: Lahjakortti- ja hyvityslaskutoimintojen saumaton offline-tilaan vaihtaminen
description: Tässä artikkelissa on yleiskatsaus parannuksiin, jotka tarjoavat saumattoman offline-kytkimen tietyille maksutyypeille.
author: BrianShook
ms.date: 02/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 20120-02-28
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: e0416a61bd5fd3b875b427ad8a6313d0e9936f0d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869158"
---
# <a name="seamless-offline-switch-for-gift-card-and-credit-memo-operations"></a>Lahjakortti- ja hyvityslaskutoimintojen saumaton offline-tilaan vaihtaminen

[!include [banner](../includes/banner.md)]

Jos myyntipisteen laite menettää yhteyden kanavan tietokantaan, suurinta osa meneillään olevista myyntipistetoiminnoista ja -tapahtumista voidaan jatkaa sen jälkeen, kun kassanhoitaja vastaanottaa varoitussanoman yhteyden menettämisestä. Joissakin tapauksissa tapahtumilla on elementtejä, jotka edellyttävät reaaliaikaista palvelua. Näitä elementtejä ei tueta, jos myyntipiste on offline-tilassa. Tässä artikkelissa kuvataan joitakin toimintoja, jotka auttavat vähentämään menetetyn yhteyden vaikutusta näissä skenaarioissa.

## <a name="completing-gift-card-transactions-in-offline-mode"></a>Lahjakorttitapahtumien päättäminen offline-tilassa

Sisäiset lahja kortit vaativat reaaliaikaisen palvelun, koska lahjakorttien saldoa on ylläpidettävä keskitetysti Microsoft Dynamics 365 Commerce Headquarters -sovelluksessa. Voit estää petokset tai synkronointiongelmat, jos lahjakortit lukitaan heti tapahtumaan lisäämisen jälkeen. Lukitustoiminnon avulla voidaan varmistaa, että lahjakorttia ei voi käyttää useilla päätteillä samanaikaisesti. Kun tapahtuma on valmis, lahjakortti päivitetään ja sen lukitus poistetaan automaattisesti.

Jos myyntipiste kuitenkin menettää yhteyden sen jälkeen, kun lahjakortti on lisätty tapahtumaan, lahjakorttia ei ehkä voi käyttää. Voit estää tämän tilanteen Dynamics 365 Commercen parametrin avulla. Se mahdollistaa lahjakortin sisältämien tapahtumien suorittamisen myyntipisteen ollessa offline-tilassa. Kun tämä parametri on otettu käyttöön, lahjakorttitapahtumat, jotka ovat offline-tilassa, voidaan tallentaa yhdessä offline-tapahtumien kanssa. Ne synkronoidaan Commerce Headquarters -sovellukseen offline-tapahtumien synkronoinnin yhteydessä. Synkronointi poistaa myös lahjakortin lukituksen, jotta sitä voidaan käyttää toisessa päätteessä.

Jos haluat, että toiminto voi tehdä lahjakorttitapahtumat offline-tilaan siirtymisen jälkeen, siirry **Kirjaus**-välilehteen **Commerce-parametrit**-sivulla. Etsi tässä välilehdessä **Lahjakortti**-pikavälilehti ja määritä **Salli lahjakorttitapahtumien päättäminen offline-tilassa** -kohdan arvoksi **Kyllä**.

![Offline-lahjakortin asetus.](../media/gift.png)

Commerce-parametrit ovat yleensä välimuistissa. Siksi tämän parametrin päivittämisen ja jakeluaikataulun kanavaan synkronoinnin aloittamisen jälkeen muutoksen voimaantulo voi kestää jopa 24 tuntia. Jos haluat, että muutos tulee voimaan heti, nollaa Microsoft Internet Information Services (IIS).

## <a name="completing-credit-memo-transactions-in-offline-mode"></a>Hyvitystapahtumien päättäminen offline-tilassa

Hyvityslaskuja ylläpidetään keskitetysti Commerce Headquarters -sovelluksessa sisäisten lahjakorttien tapaan. Commerce sisältää parametrin, jonka avulla hyvityslaskutapahtumat voidaan tehdä valmiiksi myyntipisteen ollessa offline-tilassa. Tämä parametri toimii kuten edellisessä osassa mainittu lahjakorttiparametri. Kun parametri on otettu käyttöön, offline-tilassa käytössä olevat hyvityslaskutapahtumat synkronoidaan takaisin kanavan tietokantaan yhdessä niiden tapahtumien kanssa, jotka suoritettiin myyntipisteen ollessa offline-tilassa.

Jos haluat, että toiminto voi tehdä hyvityslaskutapahtumat offline-tilaan siirtymisen jälkeen, siirry **Kirjaus**-välilehteen **Commerce-parametrit**-sivulla. Etsi tässä välilehdessä **Hyvityslasku**-pikavälilehti ja määritä **Salli hyvityslaskutapahtumien päättäminen offline-tilassa** -kohdan arvoksi **Kyllä**.

![Offline-hyvityslaskun asetus.](../media/creditmemo.png)

Commerce-parametrit ovat yleensä välimuistissa. Siksi tämän parametrin päivittämisen ja jakeluaikataulun kanavaan synkronoinnin aloittamisen jälkeen muutoksen voimaantulo voi kestää jopa 24 tuntia. Jos haluat, että muutos on voimassa heti, nollaa IIS.

## <a name="related-articles"></a>Liittyvät artikkelit

- [Myyntipistetoiminto offline-tilassa](../pos-offline-functionality.md)
- [Myyntipisteen toiminnot (POS) verkossa ja paikallisesti](../pos-operations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]