---
title: Commerce-keskustelu ja Power Virtual Agents -moduuli
description: Tässä artikkelissa kerrotaan Commerce-keskustelu ja Power Virtual Agents -moduulista, joka integroi Microsoft Power Virtual Agentsin ja Dynamics 365 Commercen sivustot.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-09-07
ms.openlocfilehash: 838990cb638479c9c90ba0e38794ecedd55e95b3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691060"
---
# <a name="commerce-chat-with-power-virtual-agents-module"></a>Commerce-keskustelu ja Power Virtual Agents -moduuli

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan Commerce-keskustelu ja Power Virtual Agents -moduulista, joka integroi Microsoft Power Virtual Agentsin ja Dynamics 365 Commercen sivustot.

Commerce-keskustelu ja Power Virtual Agents -ominaisuuden avulla Dynamics 365:n sähköisen kaupankäynnin asiakkaat saavat kaiken irti Power Virtual Agents -keskustelubotin ominaisuuksien käyttämisessä kyselyissä. Dynamics 365 Commerce 10.0.30 -version julkaisemisen jälkeen tämä ominaisuus on ollut mukana sähköisen kaupankäynnin sivustoissa Commerce-keskustelu ja Power Virtual Agents -moduulin avulla. Moduuli on Commerce-moduulikirjaston osa.

Commerce-keskustelu ja Power Virtual Agents -ominaisuus auttaa yrityksiä saavuttamaan seuraavia tavoitteita:

- henkilökohtaisen yhteydenpidon lisääminen asiakkaiden kanssa ja asiakasuskollisuuden parantamiseksi
- asiakaspalvelun parantaminen itsepalvelun keskustelubottien integroinnin avulla
- yleisen asiakastyytyväisyyden parantaminen ja myynnin kasvattaminen.

> [!NOTE]
> Lisätietoja Dynamics 365 Omnichannel for Customer Service- ja Power Virtual Agents -sovellusten eroista on kohdassa [Commerce-keskustelumoduulien yleiskatsaus](/commerce-chat-modules-overview.md).

## <a name="prerequisites-for-using-power-virtual-agents"></a><a id="prereq"></a>Power Virtual Agentsin käytön edellytykset

Jos haluat käyttää Commerce-keskustelu ja Power Virtual Agents -ominaisuutta, luo ensin Power Virtual Agents -keskustelubotti sähköisen kaupankäynnin sivustolle. Lisätietoja on kohdassa [Power Virtual Agent -botin luominen](/power-virtual-agents/authoring-first-bot).

Kun keskustelubotti on määritetty, kopioidaan **Botin tunnus**- ja **Vuokraajan tunnus** -parametrit Commerce-keskustelun käyttökokemukseen määritystä varten. Lisätietoja näiden arvojen kopioimisesta on kohdassa [Power Virtual Agents -botin parametrien noutaminen](/power-virtual-agents/publication-connect-bot-to-custom-application#retrieve-your-power-virtual-agents-bot-parameters).

## <a name="configure-your-e-commerce-site"></a>Sähköisen kaupankäynnin sivuston määrittäminen 

Eräs suositeltava tapa ottaa käyttöön keskustelukokemus sähköisen kaupankäynnin sivustossa on lisätä Commerce-keskustelu ja Power Virtual Agents -moduuli sivuston sivujen jaettuun ylätunnistekatkelmaan.

Voit lisätä keskustelumoduulin sivuston ylätunnistekatkelmaan Commercen sivustonmuodostimessa seuraavasti.

1. Siirry Commerce-sivuston sivuston muodostimessa **Katkelmat**-kohtaan.
1. Valitse **Uusi**.
1. Valitse **Valitse katkelma** -valintaikkunassa **Commerce-keskustelu ja Power Virtual Agents** -moduulissa, syötä osan nimi ja valitse sitten **OK**.
1. Valitse ääriviivanäkymässä **Msdyn365 pva -keskustelun yhdistin** -paikka.
1. Noudata oikeanpuoleisessa ominaisuuksien ruudussa seuraavia ohjeita:

    1. Jätä **Bottiparametrit**-kohdan **Bot Framework Webchat -keskustelun CDN:n URL-osoite** -kenttään oletusarvo (esimerkiksi`https://cdn.botframework.com/botframework-webchat/latest/webchat.js`).
    1. Jätä **Bot Framework Direct Linen todennuksen URL-osoite** -kenttään oletusarvo (esimerkiksi `https://powerva.microsoft.com/api/botmanagement/v1/directline/directlinetoken`).
    1. Syötä **Botin tunnus** -kenttään Power Virtual Agentsin **botin tunnuksen** arvo, joka kopioitiin [Power Virtual Agentsin käytön edellytykset](#prereq) -osassa.
    1. Syötä **Vuokraajan tunnus** -kenttään kopioitu **vuokraajan tunnuksen** arvo.

1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi osan, ja julkaise se valitsemalla **Julkaise**.
1. Siirry **Katkelmat**-kohtaan ja avaa ylätunnistekatkelma sivustossa.
1. Valitse **Oletussäilö**-paikassa kolme pistettä (**...**) ja valitse sitten **Lisää katkelma**.
1. Valitse **Valitse moduulit** -valintaikkunassa keskustelukatkelma, jonka loit aiemmin, ja valitse sitten **OK**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi osan, ja julkaise se valitsemalla **Julkaise**.

## <a name="proactive-chat-parameters"></a>Ennakoivat keskustelun parametrit

Ennakoivien keskustelun määritysparametrien täydellinen luettelo on kohdassa [Commerce-keskustelun moduulin ennakoivat keskustelun parametrit](chat-proactive-chat-parameters.md).

> [!NOTE]
> Tällä hetkellä Power Virtual Agents ei tue Azure Active Directoryn kuluttajakaupan (Azure AD:n kuluttajakauppa) todennusta. Se tukee vain Retail Cloud Scale Unit (RCSU) -puheluja anonyymisti, jotta saavutetaan tuotteiden käytettävyys tai jotta voidaan olla vuorovaikutuksessa muiden anonyymien ohjelmointirajapintojen kanssa. Puhelut todennettuihin ohjelmointirajapintoihin Power Virtual Agents -keskustelubottien kautta vaativat eksplisiittisen asiakaskirjautumisen.

## <a name="additional-resources"></a>Lisäresurssit

[Commerce-keskusteluominaisuuksien yleiskatsaus](commerce-chat-overview.md)

[Commerce-keskustelu ja Customer Servicen monikanava -moduuli](commerce-chat-module.md)

[Commerce-keskustelumoduulin ennakoivan keskustelun parametrit](chat-proactive-chat-parameters.md)
