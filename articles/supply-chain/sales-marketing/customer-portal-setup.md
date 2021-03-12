---
title: Asiakasportaalin asentaminen, määrittäminen ja päivittäminen
description: Tässä ohjeaiheessa on asiakasportaalin käyttöoikeustiedot ja asennusohjeet.
author: dasani-madipalli
manager: tfehr
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 2153bbca2be7c72e48b9dc51b1f7fdbe2ab89903
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977735"
---
# <a name="install-set-up-and-update-the-customer-portal"></a>Asiakasportaalin asentaminen, määrittäminen ja päivittäminen

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="licensing-requirements"></a>Käyttöoikeusvaatimukset

Asiakasportaalin käyttöönotto edellyttää, että sinulla on seuraavat käyttöoikeudet:

- **Power Apps -portaalit** – Asiakasportaalin isännöintiin tarvitaan tämä käyttöoikeus. Portaalien käyttöoikeus perustuu käyttöön. Lisätietoja on kohdassa [Power Apps -portaalien käyttöoikeussopimuksen vaatimukset](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).
- **Kaksoiskirjoitus** – Sinulla on oltava tarvittavat käyttöoikeudet, jotta voit ottaa käyttöön Supply Chain Management -taulukoiden kaksoiskirjoituksen. Lisätietoja on kohdassa [kaksoiskirjoituksen järjestelmävaatimukset](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a>Kaksoiskirjoituksen riippuvaisuudet ja Power Apps -portaalit

Asiakasportaali on riippuvainen Power Apps -portaaleista ja kaksoiskirjoittamisesta, kuten seuraavasta kuvasta näkyy.

![Asiakasportaalin riippuvuudet](media/customer-portal-elements.png "Asiakasportaalin riippuvuudet")

Toisin kuin muut Supply Chain Managementin ominaisuudet, asiakasportaalimalli sijaitsee Power Apps -portaaleissa. Tämän vuoksi Power Apps -portaalien ja kaksoiskirjoitustaulukoiden sisältämät toiminnot ja ominaisuudet rajoittavat asiakasportaalia.

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a>Asiakasportaalin käyttöön tarvittavat määritykset

Kun olet varma, että sinulla on tarvittavat käyttöoikeudet, voit määrittää kaksoiskirjoitustiedot, jotka on kuvattu kohdassa [kaksoiskirjoituksen alkuperäiset synkronointiohjeet](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).

Muista ottaa seuraavat taulukon yhdistämismääritykset käyttöön kaksoiskirjoitustilanteissa:

- Myyntitilauksen otsikko
- Myyntitilauksen tiedot
- Tilit
- Yhteyshenkilöt
- Tuotteet

Kun nämä määritykset on tehty, voit määrittää asiakasportaalin mallipohjan.

## <a name="provision-the-customer-portal"></a>Asiakasportaalin valmistelu

Varmista ennen aloittamista, että olet jo määrittänyt [tarvittavat määritykset](#required-setup). Valmistele sitten asiakasportaali noudattamalla näitä ohjeita.

1. Siirry kohtaan [make.powerapps.com](https://make.powerapps.com/).
2. Varmista, että käytät ympäristöä, jossa kaksoiskirjoitus on käytössä.
3. Vieritä **Luo**-välilehdessä alas **Aloita mallista** -osaan ja valitse malli, jonka nimi on **Asiakasportaali**.
4. Noudata näytön ohjeita.

Kun valmistelu on tehty, voit käyttää asiakas portaalia **Koti**-sivun **Sovellukset**-osiossa.

> [!NOTE]
> Jos kaksoiskirjoitusratkaisua ei asenneta ympäristössä, jossa työskentelet, näyttöön tulee virhesanoma eikä asiakasportaalia valmistella.

## <a name="update-the-customer-portal"></a>Asiakasportaalin päivitys

Asiakasportaaliin voidaan lisätä toimintoja myöhemmin. Kaikki Microsoftin pohjana olevan ratkaisun komponentteihin tekemät muutokset tulevat automaattisesti näkyviin ympäristössäsi. Ympäristössäsi valmisteltu verkkosivusto ei kuitenkaan automaattisesti vastaa määritystietoihin tehtyjä muutoksia. Sinun on sovellettava näitä muutoksia manuaalisesti, jotta saat uuden mallin koodin ja voit yhdistää sen valmistellulla verkkosivustolla.

## <a name="additional-resources"></a>Lisäresurssit

Jos haluat tietää, miten asiakasportaali voidaan määrittää ja mukauttaa, aloita tarkastelemalla seuraavia tekniikoita koskevia ohjeita:

- [Power Apps -portaalit -dokumentaatio](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [Kaksoiskirjoituksen dokumentointi](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

Portaalien tehokas hallinta edellyttää, että ymmärrät Power Apps -portaaleja ja Microsoft Dataverse -elinkaarta. Lisätietoja on seuraavissa resursseissa:

- [Tietoja portaalin elinkaaresta](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [Portaalin päivittäminen](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [Portaalin konfiguraation siirtäminen](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [Ratkaisun elinkaaren hallinta: Dynamics 365 for Customer Engagement -sovellukset](https://www.microsoft.com/download/details.aspx?id=57777)
