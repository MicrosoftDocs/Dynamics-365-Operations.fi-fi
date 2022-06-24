---
title: Resurssien hallinnan mobiilityötilan määrittäminen
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Supply Chain Managementin ja Finance and Operations (Dynamics 365) -mobiilisovelluksen määrittämistä suorittamaan Resurssien hallinta -mobiilityötila, jota työntekijät voivat käyttää resurssien hallintatehtävien suorittamiseen.
author: johanhoffmann
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-22
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ee92ed2c0e2a59adaebe20ed3d426ac03c056dac
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870839"
---
# <a name="set-up-the-asset-management-mobile-workspace"></a>Resurssien hallinnan mobiilityötilan määrittäminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään Microsoft Dynamics 365 Supply Chain Managementin ja Finance and Operations (Dynamics 365) -mobiilisovelluksen määrittämistä suorittamaan **Resurssien hallinta** -mobiilityötila, jota työntekijät voivat käyttää resurssien hallintatehtävien suorittamiseen.

## <a name="set-up-maintenance-worker-users-in-supply-chain-management"></a>Ylläpitotyöntekijäkäyttäjien määrittäminen Supply Chain Managementissa

**Resurssien hallinta** -työtilan käyttöoikeus määritetään sitä tarvitseville käyttäjille seuraavasti:

1. Valitse Supply Chain Managementissa **Henkilöstöhallinto \> Työntekijät** ja varmista, että määritettävällä käyttäjällä on työntekijätietue. Luo tarvittaessa uusi työntekijätietue.
1. Valitse **Resurssien hallinta \> Asetukset \> Työntekijät \> Työntekijät** ja varmista, että edellisessä vaiheessa määritetty (tai luotu) työntekijätietue on yhdistetty ylläpitotyöntekijätietueeseen. Luo tarvittaessa uusi ylläpitotyöntekijätietue ja määritä **Työntekijä**-kenttään edellisen vaiheen työntekijätietue.
1. Valitse **Resurssien hallinta \> Asetukset \> Työntekijät \> Ylläpitotyöntekijäryhmät** ja varmista, että edellisessä vaiheessa määritetty (tai luotu) ylläpitotyöntekijätietue on kuuluu ylläpitotyöntekijäryhmään.
1. Valitse **Järjestelmänhallinta \> Käyttäjät**.
1. Valitse sopiva käyttäjä ruudukossa.
1. Määritä **Käyttäjän tiedot** -pikavälilehdessä **Henkilö**-kenttään työtekijätietue, joka halutaan liittää nykyiseen käyttäjätiliin. Tämän työntekijätietueen on oltava vaiheessa yksi määritetty (tai luotu) työntekijätietue, joka yhdistetiin ylläpitotyöntekijätietueeseen vaiheessa 2.

> [!NOTE]
> Käyttöoikeudet ja käyttöoikeusroolit koskevat **Resurssien hallinta** -mobiilityötilan toimintoja samalla tavoin kuin ne koskevat Supply Chain Management -käyttöliittymän toimintoja. Niinpä jokaisella käyttäjällä, jolle määritetään **Resurssien hallinta** -työtilan käyttöoikeus, on oltava käyttöoikeusroolit, joita tarvitaan samanlaisten toimintojen suorittamiseen suoraan Supply Chain Managementissa.

## <a name="publish-the-asset-management-mobile-workspace"></a>Resurssien hallinnan mobiilityötilan julkaiseminen

Resurssien hallinnan toimintojen käyttöönottaminen Finance and Operations (Dynamics 365) -mobiilisovelluksessa edellyttää **Resurssien hallinta** -mobiilityötilan julkaisemista.

1. Valitse Supply Chain Managementissa **Asetukset**-painike (rataskuvake oikeassa yläkulmassa) ja valitse sitten valikossa **Mobiilisovellus**.
1. Etsi **Mobiilisovelluksen hallinta** -valintaikkunassa **Resurssien hallinta** -ruutu. Jos siinä on teksti Metatiedoissa – ei julkaistu, työtilaa ei ole vielä julkaistu. Jos siinä on teksti Metatiedoissa – julkaistu, työtila on jo julkaistu ja tämän menettelyn muut vaiheet voidaan ohittaa.

    ![Mobiilisovelluksen hallinta -valintaikkuna.](media/mobile-workspaces.png "Mobiilisovelluksen hallinta -valintaikkuna")

1. Valitse ensin **Resurssien hallinta** -ruutu ja sitten työkalurivillä **Julkaise**. Muutaman sekunnin kuluttua pitäisi avautua ilmoitus, jonka mukaan työtilan julkaisu on onnistunut. Lisäksi ruudussa olevan tekstin pitäisi olla nyt Metatiedoissa – julkaistu.

## <a name="install-and-set-up-the-finance-and-operations-dynamics-365-mobile-app"></a>Finance and Operations (Dynamics 365) -mobiilisovelluksen asentaminen ja määrittäminen

1. Asenna **Microsoft Finance and Operations (Dynamics 365)** -sovellus mobiililaitteeseen siirtymällä johonkin seuraavista sovelluskaupoista:

    - [Google Android -laitteet](https://go.microsoft.com/fwlink/?linkid=850662)
    - [Apple iOS -laitteet](https://go.microsoft.com/fwlink/?linkid=850663)

1. Avaa talous- ja toimintosovellus (Dynamics 365). Kirjautumissivun pitäisi avautua. Anna **Kirjaudu sisään** -kentässä Supply Chain Managementin URL-osoite tai valitse viimeaikainen URL-osoite **Viimeisimmät ympäristöt** -luettelo ja valitse sitten **Yhdistä**.

    ![Kirjautumissivu.](media/mobile-app-sign-in.png "Kirjautumissivu")

1. Jos yhteys pyydetään vahvistamaan, valitse **Ymmärrän**-valintaruutu ja valitse sitten **Yhdistä**.
1. Kirjaudu mobiilisovellukseen käyttämällä **Valitse tili** -sivulla Microsoft-tiliä.

    **Työtilat**-sivu avautuu. Siinä on luettelo kaikista mobiilityötiloista, jotka Supply Chain Management -esiintymä on julkaissut.

    ![Työtilojen luettelo.](media/mobile-app-workspaces.png "Työtilojen luettelo")

1. Jos yritystä (yhtiötä) on vaihdettava, napauta vasemmassa yläkulmassa Valikko-painiketta (siinä useita allekkaisia viivoja) ja valitse sitten **Vaihda yritys**.

    ![Yrityksen vaihtaminen.](media/mobile-app-change-comp.png "Yrityksen vaihtaminen")

1. Avaa **Työtilat**-sivulla työtila, jota haluat käyttää, valitsemalla se.

    ![Resurssien hallinnan mobiilityötila.](media/mobile-app-asset-workspace.png "Resurssien hallinnan mobiilityötila")

## <a name="work-with-the-asset-management-mobile-workspace"></a>Resurssien hallinnan mobiilityötilan käyttäminen

Lisätietoja **Resurssien hallinta** -mobiilityötilan käyttämisestä on kohdassa [Resurssien hallinnan mobiilityötilan käyttäminen](asset-management-mobile-workspace.md).

Lisätietoja Finance and Operations (Dynamics 365) -mobiilisovelluksesta on kohdassa [Mobiilisovelluksen aloitussivu](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]