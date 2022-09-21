---
title: Dynamics 365 Supply Chain Managementin esiversio 10.0.30 (Marraskuu 2022)
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Supply Chain Managementin 10.0.30 uusia tai muuttuneita toimintoja.
author: kamaybac
ms.date: 09/08/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-09-08
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 477b27bf77d2a3ef91a5c2d39f2dfb06d8ad4e59
ms.sourcegitcommit: 562ea02e1f7409f18ee1cc4750a838bff4381e91
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/08/2022
ms.locfileid: "9429120"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10030-november-2022"></a>Dynamics 365 Supply Chain Managementin esiversio 10.0.30 (Marraskuu 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä artikkelissa käsitellään Microsoft Dynamics 365 Supply Chain Managementin esikatseluversion 10.0.30 uusia tai muuttuneita ominaisuuksia. Tämän version koontinumero on 10.0.1362. Se on käytettävissä seuraavan aikataulun mukaisesti:

- **Julkaisun esiversio:** Syyskuu 2022
- **Version yleinen saatavuus (oma päivitys):** lokakuu 2022
- **Version yleinen saatavuus (automaattinen päivitys):** marraskuu 2022

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnot

Seuraavassa taulukossa on tämän julkaisun sisältämät toiminnot. Tämän artikkelin päivitys saattaa sisältää ominaisuuksia, jotka on lisätty koontiversioon tämän artikkelin alkuperäisen julkaisun jälkeen.

| Ominaisuusalue | Ominaisuus | Lisätietoja | Käyttöönottaja:   |
|---|---|---|---|
| Valmistus | [Laitteiston valvominen Sensor Data Intelligencen avulla](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/monitor-equipment-sensor-data-intelligence) | [Sensor Data Intelligencen aloitussivu](../sensor-data-intelligence/sdi-home-page.md) | Toimintojen hallinta:<br>*(Esiversio) Anturitietojen analyysi* |
| Varastonhallinta   | Monitasoiset kiertotiet Warehouse Management ‑mobiilisovelluksessa <!-- KFM: Add link when RP updates --> | [Mobiililaitteen valikkokohteiden vaiheiden kiertämisen määrittäminen](../warehousing/warehouse-app-detours.md) | Toimintojen hallinta:<br>*Monitasoiset kiertotiet Warehouse Management ‑mobiilisovelluksessa* |

## <a name="feature-enhancements-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnon parannukset

Seuraavassa taulukossa on tämän julkaisun sisältämät ominaisuuksien parannukset. Jokainen näistä parannuksista parantaa aiemmin luotua toimintoa lisäysten avulla. Koska ne ovat vain parannuksia, niitä ei ole lueteltu [vapautussuunnitelmassa](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Jos kuitenkin haluat varmistaa, että nämä parannukset eivät ole ristiriidassa aiemmin luotujen mukautuksiesi tai asetuksesi kanssa, kaikki muutokset ovat oletusarvon mukaan pois käytöstä (ellei toisin ilmoiteta).

Jos haluat ottaa jonkin näistä ominaisuuksista käyttöön tai poistaa ne käytöstä, sinun on tehtävä se [ominaisuuksienhallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Moduuli | Ominaisuuden nimi ominaisuuksienhallinnassa | Lisätietoja |
|---|---|---|
| Tuotannonhallinta | Käytössä olevat tiedot tuotantotilauksissa julkaisusivulle | Lisää rivinimikkeen käytettävissä olevan varaston määrän sarakkeen vapautussivun rivinimikkeelle **Julkaistavat tuotantotilaukset** -sivulla. |
| Kuljetustenhallinta | Määritä lähetykset liittyviin reittisegmentteihin | Tämän ominaisuuden avulla järjestelmä voi määrittää lähetyksen rahtikustannukset tarkemmin esimerkiksi useille lähetyksille, jotka toimitetaan eri segmenttikohteisiin yhdellä reitillä. Se liittää kunkin lähetyksen sopivimman reitityssegmentin lähetykseen käyttämällä lähetyksen ja segmentin kohdeosoitteita. Tämän jälkeen se laskee kunkin lähetyksen rahtikustannukset kuormauksen kokonaisrahtikustannusten osana lähetyksen suhteellisen painon, tilavuuden, määrän ja kuljetun matkan perusteella. Tämä toiminto koskee vain Kuljetustenhallinta-moduulin (TMS) avulla hallittuja lähetyksiä. |

## <a name="additional-resources"></a>Lisäresurssit

### <a name="platform-updates-for-finance-and-operations-apps"></a>Taloushallinnon ja toimintojen sovellusten ympäristöpäivitykset

Microsoft Dynamics 365 Supply Chain Management 10.0.30 sisältää Platform updateja. Lisätietoja on kohdassa [rahoitus- ja toiminta -sovellusten (marraskuu 2022) käyttöympäristön päivitysversio 10.0.30.](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md). <!--KFM: Confirm link -->

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Saat lisätietoja version 10.0.29 virheenkorjauksista eri päivityksissä kirjautumalla sisään Lifecycle Services (LCS) -sovellukseen ja lukemalla [Knowledge Base -artikkelin](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365:n ja toimialan pilvipalvelu: 2022 julkaisuaalto 1 -suunnitelma

Haluatko tietoja tulevien ja juuri julkaistujen yrityssovellustemme tai -ympäristöjemme ominaisuuksista?

Katso [Dynamics 365:n ja toimialan pilvipalvelu: 2022 julkaisuaalto 2 -suunnitelma](/dynamics365-release-plan/2022wave2/). Olemme koonneet kaikki tarvittavat tiedot yhteen asiakirjaan, jota voit käyttää suunnittelun apuna.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Poistetut ja vanhentuneet Supply Chain Management -toiminnot

[Dynamics 365 Supply Chain Managementin poistetut tai vanhentuneet toiminnot](removed-deprecated-features-scm-updates.md) -artikkelissa kerrotaan toiminnoista, jotka on ajoitettu poistettaviksi tai vanhentuviksi tai jotka on poistettu Supply Chain Managementissa.

- *Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.
- *Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Ennen kuin toiminto poistetaan tuotteesta, siitä annetaan vanhentumisilmoitus [Dynamics 365 Supply Chain Managementin poistetut tai vanhentuneet toiminnot](removed-deprecated-features-scm-updates.md) -artikkelissa 12 kuukautta ennen poistoa.

Jos muutokset vaikuttavat vain käännösaikaan, mutta ne ovat binaarisesti yhteensopivia Sandbox- ja tuotantoympäristön kanssa, vanhentumisaika on lyhyempi kuin 12 kuukautta. Yleensä nämä toiminnalliset päivitykset on tehtävä kääntäjään.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
