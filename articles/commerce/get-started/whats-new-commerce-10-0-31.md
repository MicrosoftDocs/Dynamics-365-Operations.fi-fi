---
title: Dynamics 365 Commercein esiversio 10.0.31 (helmikuu 2023)
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Commercein 10.0.31 uusia tai muuttuneita toimintoja.
author: josaw1
ms.date: 10/18/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-10-01
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: ed4325095163415d05a56128cb1f0334440fe0e5
ms.sourcegitcommit: c364f50ea0ad50bac5c30724b6ce301d9574b653
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/18/2022
ms.locfileid: "9787523"
---
# <a name="preview-of-dynamics-365-commerce-10031-february-2023"></a>Dynamics 365 Commercein esiversio 10.0.31 (helmikuu 2023)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä artikkelissa käsitellään Microsoft Dynamics 365 Commerce -esiversion 10.0.31 uusia tai muuttuneita ominaisuuksia. Tämän version koontinumero on 10.0.1406. Se on käytettävissä seuraavan aikataulun mukaisesti:

- **Esiversio:** lokakuu 2022
- **Version yleinen saatavuus (oma päivitys):** tammikuu 2023
- **Version yleinen saatavuus (automaattinen päivitys):** helmikuu 2023

## <a name="features-included-in-this-release"></a>Tähän julkaisuun sisältyvät toiminnot

Seuraavassa taulukossa on tämän julkaisun sisältämät toiminnot. Tämän artikkelin päivitys saattaa sisältää ominaisuuksia, jotka on lisätty koontiversioon tämän artikkelin alkuperäisen julkaisun jälkeen.

| Ominaisuusalue | Ominaisuus | Lisätietoja | Käyttöönottaja:   |
|---|---|---|---|
| Virhekoodit | Commercessa on otettu käyttöön standardoidut viitekoodit, jotka voidaan sisällyttää online-ostajille näytettäviin online-kanavan kassavirheisiin.| [Kassamoduulin virhekoodit](../checkout-module-error-codes.md)  | Käytössä oletusarvoisesti |
| Maksut | [Apple Payn ottaminen käyttöön Dynamics 365 Payment Connector Adyenia varten -ratkaisussa](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-apple-pay-dynamics-365-payment-connector-adyen)  | Sähköisen kaupankäynnin asiakkaat voivat käyttää Apple Pay -ratkaisua ostoskori- ja kassasivuilla tuettujen laitteiden ja selainten käytön yhteydessä. | Kehittäjän suostumus |
| Maksut  |  Commerce lisäsi ominaisuuden, joka rajoittaa tapaa, jolla asiakkaat käyttävät toistuvia maksutunnuksia Commerce headquartersin käyttöliittymässä. Maksulomakkeet, kuten **Puhelinkeskuksen myyntitilaukset**-sivu, eivät enää näytä asiakkaan aiemmin käyttämää toistuvaa maksutunnusta uudessa tapahtumassa käytettäväksi. Puhelinkeskuksen tai Commerce headquartersin käyttäjille näytetään vain määritetty tallennetun kortin syöte Commercen **Asiakasmaksut**-näytössä tai asiakkaan sovelluksessa myyntitilauksen kautta maksettaessa uuden tapahtuman maksun käsittelyn yhteydessä. | [Maksutunnuksen käytön rajoittaminen](../dev-itpro/limit-token-usage.md)  |  Toimintojen hallinta<p>*Rajoita maksutunnuksen käyttö tilauksen kontekstiin*  |
| Myyntipiste | [Ostotilausten luominen myyntipisteessä](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/create-purchase-orders-pos)  |  Parannettu saapuva varastotoiminto myyntipisteen sovelluksessa antaa käyttäjille mahdollisuuden luoda, muokata ja vahvistaa ostotilauspyyntöjä. |  Toimintojen hallinta<p>*Mahdollisuus luoda ostotilauspyyntö myyntipisteessä*   |
| Lisäkieliä saatavilla | Neljä lisäkieltä saatavilla | Ensisijaisten kielten luettelossa on neljä uutta kieltä käyttäjän valittaviksi: korea, portugali (Portugali), vietnam ja kiina (perinteinen). Valitse tämä vaihtoehto siirtymällä kohtaan **Käyttäjän asetukset \> Asetukset \> Kieli- ja maa/alue**. | Paikalliset asetukset |  



## <a name="additional-resources"></a>Lisäresurssit

### <a name="platform-updates-for-finance-and-operations-apps"></a>Taloushallinnon ja toimintojen sovellusten ympäristöpäivitykset

Microsoft Dynamics 365 Commerce 10.0.31 sisältää alustan päivitykset. Lisätietoja on kohdassa [Talous- ja toimintosovellusten (helmikuu 2023) käyttöympäristön päivitysversio 10.0.31](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-31.md). 
  

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Saat lisätietoja version 10.0.31 virheenkorjauksista eri päivityksissä kirjautumalla sisään Microsoft Dynamics Lifecycle Servicesiin ja tarkastelemalla [tietokanta-artikkelia](https://fix.lcs.dynamics.com/Issue/Details?bugId=758525).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365:n ja toimialan pilvipalvelu: 2022 julkaisuaalto 2 -suunnitelma

Haluatko tietoja tulevien ja juuri julkaistujen yrityssovellustemme tai -ympäristöjemme ominaisuuksista?

Katso [Dynamics 365:n ja toimialan pilvipalvelu: 2022 julkaisuaalto 2 -suunnitelma](/dynamics365-release-plan/2022wave2/). Olemme koonneet kaikki tarvittavat tiedot yhteen asiakirjaan, jota voit käyttää suunnittelun apuna.

### <a name="removed-and-deprecated-commerce-features"></a>Commercen poistetut ja vanhentuneet ominaisuudet

Poistetut ja vanhentuneet Commerce-ominaisuudet on kuvattu artikkelissa [Poistetut tai vanhentuneet Dynamics 365 Commerce -ominaisuudet](removed-deprecated-features-commerce.md).

- *Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.
- *Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Ennen kuin toiminto poistetaan tuotteesta, siitä annetaan vanhentumisilmoitus [Dynamics 365 Commercein poistetut tai vanhentuneet toiminnot](removed-deprecated-features-commerce.md) -artikkelissa 12 kuukautta ennen poistoa.


Jos muutokset vaikuttavat vain käännösaikaan, mutta ne ovat binaarisesti yhteensopivia Sandbox- ja tuotantoympäristön kanssa, vanhentumisaika on lyhyempi kuin 12 kuukautta. Yleensä nämä toiminnalliset päivitykset on tehtävä kääntäjään.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
